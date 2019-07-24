# デジタル入出力(GPIO)

一般的なデジタル入力系の関数群です。

## 利用例

- [Peripherals/GPIO(その他汎用機能)](../../Peripherals/GPIO/)

## メンバー

### pinMode()



```c
void pinMode(uint8_t pin, uint8_t mode)
```

!!! summary "引数"
	- uint8_t `pin` 
	- uint8_t `mode` 

!!! note "戻り値"
	void



### digitalWrite()



```c
void digitalWrite(uint8_t pin, uint8_t val)
```

!!! summary "引数"
	- uint8_t `pin` 
	- uint8_t `val` 

!!! note "戻り値"
	void



### digitalRead()



```c
int digitalRead(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 

!!! note "戻り値"
	int



### attachInterrupt()



```c
void attachInterrupt(uint8_t pin, void(*)(void), int mode)
```

!!! summary "引数"
	- uint8_t `pin` 
	- void(*)(void) `` 
	- int `mode` 

!!! note "戻り値"
	void



### attachInterruptArg()



```c
void attachInterruptArg(uint8_t pin, void(*)(void *), void *arg, int mode)
```

!!! summary "引数"
	- uint8_t `pin` 
	- void(*)(void *) `` 
	- void * `arg` 
	- int `mode` 

!!! note "戻り値"
	void



### detachInterrupt()



```c
void detachInterrupt(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 

!!! note "戻り値"
	void



