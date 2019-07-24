# アナログ入力(ADC)

一般的なアナログ入力系の関数群です。

## 利用例

- [Peripherals/ADC](../../Peripherals/ADC/)

## メンバー



### analogRead()



```c
uint16_t analogRead(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 

!!! note "戻り値"
	uint16_t



### analogReadResolution()



```c
void analogReadResolution(uint8_t bits)
```

!!! summary "引数"
	- uint8_t `bits` 



### analogSetWidth()



```c
void analogSetWidth(uint8_t bits)
```

!!! summary "引数"
	- uint8_t `bits` 


### analogSetCycles()



```c
void analogSetCycles(uint8_t cycles)
```

!!! summary "引数"
	- uint8_t `cycles` 



### analogSetSamples()



```c
void analogSetSamples(uint8_t samples)
```

!!! summary "引数"
	- uint8_t `samples` 

### analogSetClockDiv()



```c
void analogSetClockDiv(uint8_t clockDiv)
```

!!! summary "引数"
	- uint8_t `clockDiv` 



### analogSetAttenuation()



```c
void analogSetAttenuation(adc_attenuation_t attenuation)
```

!!! summary "引数"
	- adc_attenuation_t `attenuation` 




### analogSetPinAttenuation()



```c
void analogSetPinAttenuation(uint8_t pin, adc_attenuation_t attenuation)
```

!!! summary "引数"
	- uint8_t `pin` 
	- adc_attenuation_t `attenuation` 




### hallRead()



```c
int hallRead()
```

!!! note "戻り値"
	int



### adcAttachPin()



```c
bool adcAttachPin(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 

!!! note "戻り値"
	bool



### adcStart()



```c
bool adcStart(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 

!!! note "戻り値"
	bool



### adcBusy()



```c
bool adcBusy(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 

!!! note "戻り値"
	bool



### adcEnd()



```c
uint16_t adcEnd(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 

!!! note "戻り値"
	uint16_t



