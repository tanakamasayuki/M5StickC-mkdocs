# その他関数群

delay()やmillis()などのシステム系関数群です。

## メンバー

### 一時停止 vPortYield()
通常呼び出すことはありません。長い処理中にウォッチドッグでリブートされた場合にはdelay(1)を呼び出すか、ウォッチドッグをdisableCore0WDT()などで一時停止させます。

```c
void vPortYield(void)
```

### 一時停止 yield()
通常呼び出すことはありません。長い処理中にウォッチドッグでリブートされた場合にはdelay(1)を呼び出すか、ウォッチドッグをdisableCore0WDT()などで一時停止させます。

```c
void yield(void)
```

### 温度取得 temperatureRead()
チップ内部の温度を取得します。

```c
float temperatureRead()
```

!!! note "戻り値"
	float 温度

### Core0ウォッチドッグ有効 enableCore0WDT()
Core0のウォッチドッグを有効にします。起動直後はCore1のウォッチドッグは有効化されています。

```c
void enableCore0WDT()
```

### disableCore0WDT()
Core0のウォッチドッグを無効にします。起動直後はCore1のウォッチドッグは有効化されています。

```c
void disableCore0WDT()
```

### enableCore1WDT()
Core1のウォッチドッグを有効にします。起動直後はCore1のウォッチドッグは無効化されています。

```c
void enableCore1WDT()
```

### disableCore1WDT()
Core1のウォッチドッグを無効にします。起動直後はCore1のウォッチドッグは無効化されています。

```c
void disableCore1WDT()
```

### タスク作成 xTaskCreateUniversal()
タスクを作成します。内部的にはxTaskCreatePinnedToCore()とxTaskCreate()をラッピングしている関数です。
xCoreIDが0か1のときにはxTaskCreatePinnedToCore()が呼ばれ、それ以外の場合にはCore0に相当するxTaskCreate()が呼ばれる。

```c
BaseType_t xTaskCreateUniversal(TaskFunction_t pxTaskCode, const char *const pcName, const uint32_t usStackDepth, void *const pvParameters, UBaseType_t uxPriority, TaskHandle_t *const pxCreatedTask, const BaseType_t xCoreID)
```

!!! summary "引数"
	- TaskFunction_t `pxTaskCode` タスク関数
	- const char *const `pcName` タスク名
	- const uint32_t `usStackDepth` スタックメモリサイズ
	- void *const `pvParameters` タスク関数引数
	- UBaseType_t `uxPriority` 優先度(1-25,大きいほうが優先)
	- TaskHandle_t *const `pxCreatedTask` タスクハンドルポインタ
	- const BaseType_t `xCoreID` 利用するCPUコア(0:通常コア,1:無線などで利用するコア)

!!! note "戻り値"
	BaseType_t 実行結果(pdPASS=1:成功, pdFAIL=0:失敗)

### 経過マイクロ時間 micros()
プログラムの起動からの経過時間をミクロ秒で返す。

```c
unsigned long micros()
```

!!! note "戻り値"
	unsigned long 経過時間



### 経過ミリ時間 millis()
プログラムの起動からの経過時間をミリ秒で返す。

```c
unsigned long millis()
```

!!! note "戻り値"
	unsigned long 経過時間

### ミリ秒遅延 delay()
プログラムにウエイトを入れ、遅延させる。遅延中は別タスクが実行される。

loop()関数以外で長時間の処理を実行する場合にウォッチドッグでリブートされる場合には、delay(1)を入れる必要がある。

```c
void delay(uint32_t ms)
```

!!! summary "引数"
	- uint32_t `ms` 遅延時間

### マイクロ秒遅延 delayMicroseconds()
プログラムにウエイトを入れ、遅延させる。
delay()とは異なり、指定時間がくるまでwhileループして遅延させているだけである。

```c
void delayMicroseconds(uint32_t us)
```

!!! summary "引数"
	- uint32_t `us` 遅延時間

### 無線関連初期化 arduino_phy_init()
無線関連を初期化する。通常呼び出す必要はない。

```c
void arduino_phy_init()
```

### 初期化 initArduino()
初期化する。通常呼び出す必要はない。

```c
void initArduino()
```

