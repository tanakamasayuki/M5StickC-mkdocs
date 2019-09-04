# デジタル入出力(GPIO)

一般的なデジタル入力系の関数群です。

## 利用例

- [Peripherals/GPIO(その他汎用機能)](../../Peripherals/GPIO/)

## メンバー

### ピンモード設定 pinMode()
指定したピンのモードを設定する。

```c
void pinMode(uint8_t pin, uint8_t mode)
```

!!! summary "引数"
	- uint8_t `pin` 指定するpin
	- uint8_t `mode` 設定するモード
		- INPUT : デジタル入力
		- INPUT_PULLUP : プルアップ入力
		- INPUT_PULLDOWN : プルアップ入力
		- OUTPUT : デジタル・アナログ出力
		- OUTPUT_OPEN_DRAIN : オープンドレイン出力
		- ANALOG : アナログ入力

!!! Tip "利用例"
	```c
	pinMode(0, OUTPUT);	// pin0を出力モードにする
	```

### デジタル出力 digitalWrite()
指定したピンの電圧を設定します。

```c
void digitalWrite(uint8_t pin, uint8_t val);
```

!!! summary "引数"
	- uint8_t `pin` 指定するpin
	- uint8_t `val` 設定するモード(HIGH, LOW)

!!! Tip "利用例"
	```c
	digitalWrite(0, HIGH);	// pin0を3.3V出力にする
	```

### デジタル入力 digitalRead()
指定したピンの電圧を取得します。

```c
int digitalRead(uint8_t pin);
```

!!! summary "引数"
	- uint8_t `pin` 指定するpin

!!! note "戻り値"
	HIGH:1.65V以上, LOW:1.65V未満


!!! Tip "利用例"
	```c
	int val = digitalRead(0);	// pin0の値を取得
	```

### 割り込みハンドラ設定 attachInterrupt()
指定したピンに割り込みハンドラを設定する。

```c
void attachInterrupt(uint8_t pin, void (*)(void), int mode);
```

!!! summary "引数"
	- uint8_t `pin` 指定するpin
	- void (*)(void) コールバック関数
	- int `mode` モード(DISABLED, RISING, FALLING, CHANGE, ONLOW, ONHIGH, ONLOW_WE, ONHIGH_WE)

!!! Tip "利用例"
	```c
	volatile byte state = LOW;
	
	void setup() {
	  pinMode(0, INPUT_PULLUP);
	  attachInterrupt(0, blink, CHANGE);
	}
	
	void loop() {
	}
	
	void blink() {
	  state = !state;
	}
	```

### 割り込みハンドラ設定(構造体) attachInterruptArg()
指定したピンに割り込みハンドラを設定する。
割り込み関数内部は通常と動作環境が違うので注意が必要です。

```c
void attachInterruptArg(uint8_t pin, void (*)(void*), void * arg, int mode);
```

!!! summary "引数"
	- uint8_t `pin` 指定するpin
	- void (*)(void) コールバック関数
	- void * `arg` 構造体
	- int `mode` モード(DISABLED, RISING, FALLING, CHANGE, ONLOW, ONHIGH, ONLOW_WE, ONHIGH_WE)

!!! Tip "利用例"
	```c
	struct StatusData {
	    byte state;
	};
	
	StatusData pin1 = {LOW};
	
	void setup() {
	  pinMode(0, INPUT_PULLUP);
	  attachInterrupt(0, blink, pin1, CHANGE);
	}
	
	void loop() {
	}
	
	void blink(void* arg) {
	  StatusData* s = static_cast<StatusData*>(arg);
	  s->state = !s->state;
	}
	```

### 割り込みハンドラ削除 detachInterrupt()
指定したピンの割り込みハンドラを削除する。

```c
void detachInterrupt(uint8_t pin);
```

!!! summary "引数"
	- uint8_t `pin` 指定するpin

!!! Tip "利用例"
	```c
	detachInterrupt(0);
	```



