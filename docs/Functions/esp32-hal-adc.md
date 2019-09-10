# アナログ入力(ADC)

一般的なアナログ入力系の関数群です。

## 利用例

- [Peripherals/ADC](../../Peripherals/ADC/)

## メンバー



### アナログ取得 analogRead()
指定したピンの電圧を取得します。
pinMode(PIN, ANALOG)で事前にピンの設定をアナログにしてください。
GPIO26と36は指定していないとアナログ値を取得できません。
GPIO0はプルアップされているので、正しい数値を取得することはできません。

```c
uint16_t analogRead(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 指定するpin

!!! note "戻り値"
	uint16_t ADCの値(標準は0-4095)

### ADC取得解像度設定 analogReadResolution()
analogRead関数の戻り値の解像度を設定。デフォルトは12ビット(0-4095)。
9から12の場合には、設定されているハードウエア解像度と等しくなり、それ以外の場合には値をシフトして返却します。

```c
void analogReadResolution(uint8_t bits)
```

!!! summary "引数"
	- uint8_t `bits` 解像度(1-9)

### ADCハードウエア解像度設定 analogSetWidth()
ADCのハードウエア解像度を設定。デフォルトは12ビット(0-4095)。

```c
void analogSetWidth(uint8_t bits)
```

!!! summary "引数"
	- uint8_t `bits` ハードウエア解像度(9-12)


### ADCサイクル数設定 analogSetCycles()
サンプリングのサイクル数を設定。デフォルト8。

```c
void analogSetCycles(uint8_t cycles)
```

!!! summary "引数"
	- uint8_t `cycles` サイクル数(1-255)

### ADCサンプリング数設定 analogSetSamples()
サンプリング数を設定。デフォルトは1。

```c
void analogSetSamples(uint8_t samples)
```

!!! summary "引数"
	- uint8_t `samples` サンプリング数(1-255)

### ADCクロック分周設定 analogSetClockDiv()
ADCのクロックの分周を設定。デフォルトは1。

```c
void analogSetClockDiv(uint8_t clockDiv)
```

!!! summary "引数"
	- uint8_t `clockDiv` クロック分周数(1-255)

### ADC減衰器全設定 analogSetAttenuation()
ADCの減衰器を設定。デフォルトはADC_11db。


```c
void analogSetAttenuation(adc_attenuation_t attenuation)
```

!!! summary "引数"
	- adc_attenuation_t `attenuation` 減衰器(ADC_0db, ADC_2_5db, ADC_6db, ADC_11db)

### ADC減衰器設定 analogSetPinAttenuation()
ADCの減衰器を設定。デフォルトはADC_11db。

```c
void analogSetPinAttenuation(uint8_t pin, adc_attenuation_t attenuation)
```

!!! summary "引数"
	- uint8_t `pin` 指定するpin
	- adc_attenuation_t `attenuation` 減衰器(ADC_0db, ADC_2_5db, ADC_6db, ADC_11db)

### ホールセンサー取得 hallRead()
磁気センサーである、ホールセンサーの値を取得。

```c
int hallRead()
```

!!! note "戻り値"
	int ホールセンサー値(小さいとN極, 大きいとS極)

### ADCピンアタッチ adcAttachPin()
ADCで利用するピンを指定します。

この関数はほぼノンブロックで実行が可能な内部関数です。ただし、同時に１ピンしかアタッチできません。
以下の関数群はanalogRead()関数の内部で実行している関数です。

```c
bool adcAttachPin(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 指定するpin

!!! note "戻り値"
	bool 実行結果

### ADC変換開始 adcStart()
アタッチされているピンのADC変換を開始。

```c
bool adcStart(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 指定するpin

!!! note "戻り値"
	bool 実行結果



### ADC変換状態取得 adcBusy()
指定したピンのADC変換が現在実行中か確認。

```c
bool adcBusy(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 指定するpin

!!! note "戻り値"
	bool 実行結果

### ADC結果取得 adcEnd()
ADCの変換結果を取得します。まだ完了していない場合には完了まで待ってから返却します。

```c
uint16_t adcEnd(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 指定するpin

!!! note "戻り値"
	uint16_t ADCの値(標準は0-4095)

