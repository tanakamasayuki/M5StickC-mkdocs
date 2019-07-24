# タイマー(timer)

低レベルのタイマー関数群です。

[Ticker](../../Class/ESP32/Ticker/)クラスを利用して呼び出すことも可能です。

## 利用例

- [Peripherals/タイマー](../../Peripherals/Timer/)

## メンバー



### timerBegin()



```c
hw_timer_t* timerBegin(uint8_t timer, uint16_t divider, bool countUp)
```

!!! summary "引数"
	- uint8_t `timer` 
	- uint16_t `divider` 
	- bool `countUp` 

!!! note "戻り値"
	hw_timer_t*



### timerEnd()



```c
void timerEnd(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	void



### timerSetConfig()



```c
void timerSetConfig(hw_timer_t *timer, uint32_t config)
```

!!! summary "引数"
	- hw_timer_t* `timer` 
	- uint32_t `config` 

!!! note "戻り値"
	void



### timerGetConfig()



```c
uint32_t timerGetConfig(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	uint32_t



### timerAttachInterrupt()



```c
void timerAttachInterrupt(hw_timer_t *timer, void(*fn)(void), bool edge)
```

!!! summary "引数"
	- hw_timer_t* `timer` 
	- void(*)(void) `fn` 
	- bool `edge` 

!!! note "戻り値"
	void



### timerDetachInterrupt()



```c
void timerDetachInterrupt(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	void



### timerStart()



```c
void timerStart(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	void



### timerStop()



```c
void timerStop(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	void



### timerRestart()



```c
void timerRestart(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	void



### timerWrite()



```c
void timerWrite(hw_timer_t *timer, uint64_t val)
```

!!! summary "引数"
	- hw_timer_t* `timer` 
	- uint64_t `val` 

!!! note "戻り値"
	void



### timerSetDivider()



```c
void timerSetDivider(hw_timer_t *timer, uint16_t divider)
```

!!! summary "引数"
	- hw_timer_t* `timer` 
	- uint16_t `divider` 

!!! note "戻り値"
	void



### timerSetCountUp()



```c
void timerSetCountUp(hw_timer_t *timer, bool countUp)
```

!!! summary "引数"
	- hw_timer_t* `timer` 
	- bool `countUp` 

!!! note "戻り値"
	void



### timerSetAutoReload()



```c
void timerSetAutoReload(hw_timer_t *timer, bool autoreload)
```

!!! summary "引数"
	- hw_timer_t* `timer` 
	- bool `autoreload` 

!!! note "戻り値"
	void



### timerStarted()



```c
bool timerStarted(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	bool



### timerRead()



```c
uint64_t timerRead(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	uint64_t



### timerReadMicros()



```c
uint64_t timerReadMicros(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	uint64_t



### timerReadSeconds()



```c
double timerReadSeconds(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	double



### timerGetDivider()



```c
uint16_t timerGetDivider(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	uint16_t



### timerGetCountUp()



```c
bool timerGetCountUp(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	bool



### timerGetAutoReload()



```c
bool timerGetAutoReload(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	bool



### timerAlarmEnable()



```c
void timerAlarmEnable(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	void



### timerAlarmDisable()



```c
void timerAlarmDisable(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	void



### timerAlarmWrite()



```c
void timerAlarmWrite(hw_timer_t *timer, uint64_t interruptAt, bool autoreload)
```

!!! summary "引数"
	- hw_timer_t* `timer` 
	- uint64_t `interruptAt` 
	- bool `autoreload` 

!!! note "戻り値"
	void



### timerAlarmEnabled()



```c
bool timerAlarmEnabled(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	bool



### timerAlarmRead()



```c
uint64_t timerAlarmRead(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	uint64_t



### timerAlarmReadMicros()



```c
uint64_t timerAlarmReadMicros(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	uint64_t



### timerAlarmReadSeconds()



```c
double timerAlarmReadSeconds(hw_timer_t *timer)
```

!!! summary "引数"
	- hw_timer_t* `timer` 

!!! note "戻り値"
	double



