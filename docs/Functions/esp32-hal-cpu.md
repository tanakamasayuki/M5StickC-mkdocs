# CPU

CPUクロックなどの変更が可能です。

## 概要

M5StickCは周波数40MHzのクリスタルを搭載しており、CPUは10から240MHzで動作することが可能です。

SPIやフラッシュなどのペリフェラルは80MHzが最大で、CPU周波数が下がるとともに下がります。

PWMのようにペリフェラル周波数に依存して制御が必要な機能についてはコールバック関数を設定し、周波数変更した場合の処理を設定することが可能です。

| CPU周波数(MHz) | ペリフェラル周波数(Hz) | クリスタル周波数(MHz) |
|---------------:|-----------------------:|----------------------:|
| 240            | 80000000               | 40                    |
| 160            | 80000000               | 40                    |
| 80             | 80000000               | 40                    |
| 40             | 40000000               | 40                    |
| 20             | 20000000               | 40                    |
| 10             | 10000000               | 40                    |

## メンバー

### ペリフェラル周波数変更コールバック登録 addApbChangeCallback()
ペリフェラル周波数が変更した場合に呼び出されるコールバックを登録する。


```c
bool addApbChangeCallback(void *arg, apb_change_cb_t cb)
```

!!! summary "引数"
	- void * `arg` 引数として渡されるデータ
	- apb_change_cb_t `cb` コールバック関数

!!! note "戻り値"
	bool 実行結果



### ペリフェラル周波数変更コールバック削除 removeApbChangeCallback()
ペリフェラル周波数が変更した場合に呼び出されるコールバックを削除する。



```c
bool removeApbChangeCallback(void *arg, apb_change_cb_t cb)
```

!!! summary "引数"
	- void * `arg` 引数として渡されるデータ
	- apb_change_cb_t `cb` コールバック関数

!!! note "戻り値"
	bool 実行結果



### CPU周波数設定 setCpuFrequencyMhz()
CPUの動作周波数を設定する。

設定はMHz単位で指定し、240、160、80、クリスタル周波数、クリスタル周波数/2、クリスタル周波数/4が指定できる。

M5StickCのクリスタルは40MHzなので240、160、80、40、20、10が指定可能。

```c
bool setCpuFrequencyMhz(uint32_t cpu_freq_mhz)
```

!!! summary "引数"
	- uint32_t `cpu_freq_mhz` 周波数(240, 160, 80, 40, 20, 10)MHz

!!! note "戻り値"
	bool 実行結果

### CPU周波数取得 getCpuFrequencyMhz()
CPUの動作周波数を取得します。

標準は240です。

```c
uint32_t getCpuFrequencyMhz()
```

!!! note "戻り値"
	uint32_t 周波数(MHz)

### クリスタル周波数取得 getXtalFrequencyMhz()
搭載されているクリスタルの周波数を取得します。

ESP32は24MHz、26MHz、40MHzのクリスタルを搭載できます。

M5StickCは40MHzのクリスタルを搭載していますので、戻り値は40固定です。

```c
uint32_t getXtalFrequencyMhz()
```

!!! note "戻り値"
	uint32_t 周波数(MHz)



### ペリフェラル周波数取得 getApbFrequency()
周辺機器であるペリフェラルの動作周波数を取得します。

標準は80000000(80MHz)です。

最大周波数は80MHzで、CPU動作周波数に応じて追従します。

```c
uint32_t getApbFrequency()
```

!!! note "戻り値"
	uint32_t 周波数(Hz)

## サンプルスケッチ
```c
volatile int g_ev_cnt = 0;
volatile apb_change_ev_t b_ev_type;
volatile apb_change_ev_t a_ev_type;
volatile uint32_t b_old_apb;
volatile uint32_t b_new_apb;
volatile uint32_t a_old_apb;
volatile uint32_t a_new_apb;

static void _on_apb_change(void * arg, apb_change_ev_t ev_type, uint32_t old_apb, uint32_t new_apb) {
  g_ev_cnt++;
  if ( ev_type == APB_BEFORE_CHANGE ) {
    b_ev_type = ev_type;
    b_old_apb = old_apb;
    b_new_apb = new_apb;
  } else if ( APB_AFTER_CHANGE ) {
    a_ev_type = ev_type;
    a_old_apb = old_apb;
    a_new_apb = new_apb;
  }
}

uint32_t iarg = 1;

void setup() {
  Serial.begin(115200);

  Serial.printf( "getXtalFrequencyMhz() : %d\n", getXtalFrequencyMhz() );
  Serial.printf( "getCpuFrequencyMhz() : %d\n", getCpuFrequencyMhz() );
  Serial.printf( "getApbFrequency() : %d\n", getApbFrequency() );

  Serial.printf( "\n" );

  Serial.printf( "addApbChangeCallback() : %d\n", addApbChangeCallback((void*)iarg, _on_apb_change) );

  Serial.printf( "g_ev_cnt : %d, b_ev_type : %d, b_old_apb : %d, b_new_apb : %d\n", g_ev_cnt, b_ev_type, b_old_apb, b_new_apb );
  Serial.printf( "g_ev_cnt : %d, a_ev_type : %d, a_old_apb : %d, a_new_apb : %d\n", g_ev_cnt, a_ev_type, a_old_apb, a_new_apb );

  Serial.printf( "\n" );

  for ( int i = 0 ; i <= 500 ; i++ ) {
    int ret = setCpuFrequencyMhz(i);
    if ( ret ) {
      Serial.printf( "setCpuFrequencyMhz(%d) : %d\n", i, ret );
      Serial.printf( "getCpuFrequencyMhz() : %d\n", getCpuFrequencyMhz() );
      Serial.printf( "getApbFrequency() : %d\n", getApbFrequency() );
      Serial.printf( "getXtalFrequencyMhz() : %d\n", getXtalFrequencyMhz() );
      Serial.printf( "g_ev_cnt : %d, b_ev_type : %d, b_old_apb : %d, b_new_apb : %d\n", g_ev_cnt, b_ev_type, b_old_apb, b_new_apb );
      Serial.printf( "g_ev_cnt : %d, a_ev_type : %d, a_old_apb : %d, a_new_apb : %d\n", g_ev_cnt, a_ev_type, a_old_apb, a_new_apb );
      Serial.printf( "\n" );
    }
  }

  Serial.printf( "removeApbChangeCallback() : %d\n", removeApbChangeCallback((void*)iarg, _on_apb_change) );
}

void loop() {
}
```

## 実行結果
```
getXtalFrequencyMhz() : 40
getCpuFrequencyMhz() : 240
getApbFrequency() : 80000000

addApbChangeCallback() : 1
g_ev_cnt : 0, b_ev_type : 0, b_old_apb : 0, b_new_apb : 0
g_ev_cnt : 0, a_ev_type : 0, a_old_apb : 0, a_new_apb : 0

setCpuFrequencyMhz(10) : 1
getCpuFrequencyMhz() : 10
getApbFrequency() : 10000000
getXtalFrequencyMhz() : 40
g_ev_cnt : 2, b_ev_type : 0, b_old_apb : 80000000, b_new_apb : 10000000
g_ev_cnt : 2, a_ev_type : 1, a_old_apb : 80000000, a_new_apb : 10000000

setCpuFrequencyMhz(20) : 1
getCpuFrequencyMhz() : 20
getApbFrequency() : 20000000
getXtalFrequencyMhz() : 40
g_ev_cnt : 4, b_ev_type : 0, b_old_apb : 10000000, b_new_apb : 20000000
g_ev_cnt : 4, a_ev_type : 1, a_old_apb : 10000000, a_new_apb : 20000000

setCpuFrequencyMhz(40) : 1
getCpuFrequencyMhz() : 40
getApbFrequency() : 40000000
getXtalFrequencyMhz() : 40
g_ev_cnt : 6, b_ev_type : 0, b_old_apb : 20000000, b_new_apb : 40000000
g_ev_cnt : 6, a_ev_type : 1, a_old_apb : 20000000, a_new_apb : 40000000

setCpuFrequencyMhz(80) : 1
getCpuFrequencyMhz() : 80
getApbFrequency() : 80000000
getXtalFrequencyMhz() : 40
g_ev_cnt : 8, b_ev_type : 0, b_old_apb : 40000000, b_new_apb : 80000000
g_ev_cnt : 8, a_ev_type : 1, a_old_apb : 40000000, a_new_apb : 80000000

setCpuFrequencyMhz(160) : 1
getCpuFrequencyMhz() : 160
getApbFrequency() : 80000000
getXtalFrequencyMhz() : 40
g_ev_cnt : 10, b_ev_type : 0, b_old_apb : 80000000, b_new_apb : 80000000
g_ev_cnt : 10, a_ev_type : 1, a_old_apb : 80000000, a_new_apb : 80000000

setCpuFrequencyMhz(240) : 1
getCpuFrequencyMhz() : 240
getApbFrequency() : 80000000
getXtalFrequencyMhz() : 40
g_ev_cnt : 12, b_ev_type : 0, b_old_apb : 80000000, b_new_apb : 80000000
g_ev_cnt : 12, a_ev_type : 1, a_old_apb : 80000000, a_new_apb : 80000000

removeApbChangeCallback() : 1
```