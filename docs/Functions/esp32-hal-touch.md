# タッチセンサー(touch)

タッチセンサーの関数群です。

## 利用例

- [Peripherals/タッチセンサー](../../Peripherals/TouchSensor/)

## メンバー

### 読み取りサイクル設定 touchSetCycles()
タッチセンサーの読み取りサイクルを設定する。デフォルトではtouchRead()に0.5msかかります。

```c
void touchSetCycles(uint16_t measure, uint16_t sleep)
```

!!! summary "引数"
	- uint16_t `measure` 測定サイクル(デフォルト0x1000)
	- uint16_t `sleep` スリープサイクル(デフォルト0x1000)

### タッチセンサー取得 touchRead()
タッチセンサーの値を取得する。

```c
uint16_t touchRead(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` pin番号

!!! note "戻り値"
	uint16_t 結果(0に近いほどタッチ)

### タッチ割り込み設定 touchAttachInterrupt()
タッチしたときに割り込み関数を起動する設定を行う。タッチのしきい値は環境によって異なるので、あらかじめtouchRead()などで測定して最適な値を設定する。

```c
void touchAttachInterrupt(uint8_t pin, void(*userFunc)(void), uint16_t threshold)
```

!!! summary "引数"
	- uint8_t `pin` pin番号
	- void(*)(void) `userFunc` 割り込み関数
	- uint16_t `threshold` しきい値

