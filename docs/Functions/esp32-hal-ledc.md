# PWM(LEDC)

一般的なPWM系の関数群です。

## 利用例

- [Peripherals/PWM(LED Control)](../../Peripherals/LED_Control/)


## メンバー



### ledcSetup()



```c
double ledcSetup(uint8_t channel, double freq, uint8_t resolution_bits)
```

!!! summary "引数"
	- uint8_t `channel` 
	- double `freq` 
	- uint8_t `resolution_bits` 

!!! note "戻り値"
	double



### ledcWrite()



```c
void ledcWrite(uint8_t channel, uint32_t duty)
```

!!! summary "引数"
	- uint8_t `channel` 
	- uint32_t `duty` 

!!! note "戻り値"
	void



### ledcWriteTone()



```c
double ledcWriteTone(uint8_t channel, double freq)
```

!!! summary "引数"
	- uint8_t `channel` 
	- double `freq` 

!!! note "戻り値"
	double



### ledcWriteNote()



```c
double ledcWriteNote(uint8_t channel, note_t note, uint8_t octave)
```

!!! summary "引数"
	- uint8_t `channel` 
	- note_t `note` 
	- uint8_t `octave` 

!!! note "戻り値"
	double



### ledcRead()



```c
uint32_t ledcRead(uint8_t channel)
```

!!! summary "引数"
	- uint8_t `channel` 

!!! note "戻り値"
	uint32_t



### ledcReadFreq()



```c
double ledcReadFreq(uint8_t channel)
```

!!! summary "引数"
	- uint8_t `channel` 

!!! note "戻り値"
	double



### ledcAttachPin()



```c
void ledcAttachPin(uint8_t pin, uint8_t channel)
```

!!! summary "引数"
	- uint8_t `pin` 
	- uint8_t `channel` 

!!! note "戻り値"
	void



### ledcDetachPin()



```c
void ledcDetachPin(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 

!!! note "戻り値"
	void



