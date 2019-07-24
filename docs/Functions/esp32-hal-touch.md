# タッチセンサー(touch)

タッチセンサーの関数群です。

## 利用例

- [Peripherals/タッチセンサー](../../Peripherals/TouchSensor/)

## メンバー

### touchSetCycles()



```c
void touchSetCycles(uint16_t measure, uint16_t sleep)
```

!!! summary "引数"
	- uint16_t `measure` 
	- uint16_t `sleep` 

!!! note "戻り値"
	void



### touchRead()



```c
uint16_t touchRead(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 

!!! note "戻り値"
	uint16_t



### touchAttachInterrupt()



```c
void touchAttachInterrupt(uint8_t pin, void(*userFunc)(void), uint16_t threshold)
```

!!! summary "引数"
	- uint8_t `pin` 
	- void(*)(void) `userFunc` 
	- uint16_t `threshold` 

!!! note "戻り値"
	void



