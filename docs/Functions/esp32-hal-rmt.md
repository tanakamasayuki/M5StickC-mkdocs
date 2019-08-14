# 赤外線送受信(RMT)

M5StickCは赤外線送信は標準で可能です。受信をするためには別途受信用センサーを接続する必要があります。

一般的には[IRremote ESP8266 Library](https://github.com/crankyoldgit/IRremoteESP8266)などを利用したほうが楽だと思います。

- [Functions/driver/rmt](../../Functions/driver/rmt/)

また、上記の関数群を利用しても実現できます。一般的な作例はすべてdriver/rmt.hを利用したもので、本関数群を利用している例はほぼないので、使わないほうが無難な関数群です。

## 利用例

- [Peripherals/赤外線送受信(Remote Control)](../../Peripherals/RMT/)

## メンバー

### RMT初期化 rmtInit()
rmt_obj_t構造体を簡単に設定することができます。

memsizeには送信時はRMT_MEM_64、受信時はRMT_MEM_192程度を指定する。

```c
rmt_obj_t* rmtInit(int pin, bool tx_not_rx, rmt_reserve_memsize_t memsize)
```

!!! summary "引数"
	- int `pin` PIN
	- bool `tx_not_rx` 送受信指定(true:送信, false:受信)
	- rmt_reserve_memsize_t `memsize` バッファサイズ(RMT_MEM_64, RMT_MEM_128, RMT_MEM_192, RMT_MEM_256, RMT_MEM_320, RMT_MEM_284, RMT_MEM_448, RMT_MEM_512)

!!! note "戻り値"
	rmt_obj_t* RMTオブジェクト

### クロック分周指定 rmtSetTick()
クロック分周を指定します。クロックではなく、ns単位での時間を指定します。

手元のM5StickCでは80000以外を指定すると安定しませんでした。

```c
float rmtSetTick(rmt_obj_t *rmt, float tick)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` RMTオブジェクト
	- float `tick` 1Tickの時間(ns)

!!! note "戻り値"
	float 設定された1Tickの時間(ns)

### RMT送信 rmtWrite()
非同期で送信します。

```c
bool rmtWrite(rmt_obj_t *rmt, rmt_data_t *data, size_t size)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` RMTオブジェクト
	- rmt_data_t* `data` 
	- size_t `size` 

!!! note "戻り値"
	bool 実行結果



### RMT非同期受信 rmtReadAsync()
非同期でデータを読み出します。

ただし、受信したデータ長がわからないのでこの関数は非推奨です。

```c
bool rmtReadAsync(rmt_obj_t *rmt, rmt_data_t *data, size_t size, void *eventFlag, bool waitForData, uint32_t timeout)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` RMTオブジェクト
	- rmt_data_t* `data` バッファ
	- size_t `size` バッファサイズ
	- void * `eventFlag` イベントハンドラ
	- bool `waitForData` 受信待ちをするか(false:しない, true:する)
	- uint32_t `timeout` 受信待ちのタイムアウト

!!! note "戻り値"
	bool 実行結果

!!! Tip "利用例"
	```c
	rmt_obj_t* rmt_recv = NULL;
	rmt_data_t data[192];
	int realTick;
	static EventGroupHandle_t events;
	int mode;

	void setup() {
	  Serial.begin(115200);

	  // 初期化
	  if ((rmt_recv = rmtInit(GPIO_NUM_26, false, RMT_MEM_192)) != NULL) {
	    Serial.println("Init Receiver");
	  }

	  // 1Tickを80usに設定
	  realTick = rmtSetTick(rmt_recv, 80000) / 1000;
	  Serial.printf("real tick set to: %dus\n", realTick);

	  // フィルターしきい値(この設定より短いパルスを除外)
	  rmtSetFilter(rmt_recv, true, 255);

	  // フィルターしきい値(この設定より長いパルスを除外)
	  rmtSetRxThreshold(rmt_recv, 10000);

	  // モードを初期状態にする
	  mode = 0;
	}

	void loop() {
	  if( mode == 0 ){
	    // 受信開始    
	    // データ初期化
	    memset(data,0,sizeof(data));
	    
	    // 受信開始
	    rmtReadAsync(rmt_recv, data, 192, events, false, 0);

	    // 受信待ち状態
	    mode = 1;
	  }

	  // 受信待ち
	  if( mode == 1 && rmtReceiveCompleted(rmt_recv) ) {
	    // 受信データを出力
	    for ( int i = 0; i < 192; i++) {
	      Serial.printf(" %d %d %d %d\n", data[i].duration0*realTick, data[i].level0, data[i].duration1*realTick, data[i].level1 );
	    }
	    Serial.println("\n");

	    // モードを初期状態に戻す
	    mode = 0;
	  }

	  delay(100);
	}
	```


### RMTコールバック受信 rmtRead()
自動バッファリングとコールバックを利用して、非同期受信を開始します。

```c
bool rmtRead(rmt_obj_t *rmt, rmt_rx_data_cb_t cb)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` RMTオブジェクト
	- rmt_rx_data_cb_t `cb` コールバック

!!! note "戻り値"
	bool 実行結果

!!! Tip "利用例"
	```c
	rmt_obj_t* rmt_recv = NULL;
	int realTick;

	// 受信コールバック関数
	void receive_data(uint32_t *data, size_t len) {
	  rmt_data_t* it = (rmt_data_t*)data;

	  // 長さ0は処理しない
	  if ( len == 0 ) {
	    return;
	  }

	  // 受信した生データを出力
	  Serial.printf("receive_data(size:%d) :\n", len);
	  for (int i = 0 ; i < len ; i++) {
	    Serial.printf(" %d %d %d %d\n", it[i].duration0 * realTick, it[i].level0, it[i].duration1 * realTick, it[i].level1 );
	  }
	  Serial.println();
	}

	void setup() {
	  Serial.begin(115200);

	  // 初期化
	  if ((rmt_recv = rmtInit(GPIO_NUM_26, false, RMT_MEM_192)) != NULL) {
	    Serial.println("Init Receiver");
	  }

	  // 1Tickを80usに設定
	  realTick = rmtSetTick(rmt_recv, 80000) / 1000;
	  Serial.printf("real tick set to: %dus\n", realTick);

	  // フィルターしきい値(この設定より短いパルスを除外)
	  rmtSetFilter(rmt_recv, true, 255);

	  // フィルターしきい値(この設定より長いパルスを除外)
	  rmtSetRxThreshold(rmt_recv, 10000 / realTick );

	  // 受信開始
	  rmtRead(rmt_recv, receive_data);
	}

	void loop() {
	  delay(500);
	}
	```

### RMT受信開始 rmtBeginReceive()
受信を開始します。

ただし、受信したデータ長がわからないのでこの関数は非推奨です。

```c
bool rmtBeginReceive(rmt_obj_t *rmt)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` RMTオブジェクト

!!! note "戻り値"
	bool 実行結果

### RMT受信完了確認 rmtReceiveCompleted()
受信が完了しかた確認します。

```c
bool rmtReceiveCompleted(rmt_obj_t *rmt)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` RMTオブジェクト

!!! note "戻り値"
	bool 受信結果

### RMT受信読み出し rmtReadData()
特定のチャンネルを読み出す。

ただし、受信したデータ長がわからないのでこの関数は非推奨です。

```c
bool rmtReadData(rmt_obj_t *rmt, uint32_t *data, size_t size)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` RMTオブジェクト
	- uint32_t * `data` データ
	- size_t `size` サイズ

!!! note "戻り値"
	bool 実行結果



### RMT受信しきい値設定 rmtSetRxThreshold()
受信しきい値を設定する。この設定より長いパルスを除外します。

```c
bool rmtSetRxThreshold(rmt_obj_t *rmt, uint32_t value)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` RMTオブジェクト
	- uint32_t `value` しきい値

!!! note "戻り値"
	bool 実行結果



### RMT送信キャリア設定 rmtSetCarrier()
送信キャリアを設定する。

```c
bool rmtSetCarrier(rmt_obj_t *rmt, bool carrier_en, bool carrier_level, uint32_t low, uint32_t high)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` RMTオブジェクト
	- bool `carrier_en` 
	- bool `carrier_level` 
	- uint32_t `low` 
	- uint32_t `high` 

!!! note "戻り値"
	bool 実行結果



### RMT受信フィルター設定 rmtSetFilter()
受信フィルターを設定。この設定より短いパルスを除外します。

```c
bool rmtSetFilter(rmt_obj_t *rmt, bool filter_en, uint32_t filter_level)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` RMTオブジェクト
	- bool `filter_en` 有効フラグ(false:無効, true:有効)
	- uint32_t `filter_level` フィルタレベル

!!! note "戻り値"
	bool 実行結果



### RMT初期化解除 rmtDeinit()
RMTの初期化を解除する


```c
bool rmtDeinit(rmt_obj_t *rmt)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` RMTオブジェクト

!!! note "戻り値"
	bool 実行結果

