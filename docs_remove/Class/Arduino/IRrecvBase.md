# IRrecvBase



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_i_rrecv_base.html)

## メンバー

###  markExcess

```c
uint16_t IRrecvBase::markExcess
```


### IRrecvBase()



```c
IRrecvBase::IRrecvBase(void)
```



### IRrecvBase()



```c
IRrecvBase::IRrecvBase(uint8_t recvPin)
```

!!! summary "引数"
	- uint8_t `recvPin` 



### getResults()



```c
bool IRrecvBase::getResults(const uint16_t timePerTicks=1)
```

!!! summary "引数"
	- constuint16_t `timePerTicks` 

!!! note "戻り値"
	bool



### enableIRIn()



```c
void IRrecvBase::enableIRIn(void)
```



### disableIRIn()



```c
void IRrecvBase::disableIRIn(void)
```



### enableAutoResume()



```c
void IRrecvBase::enableAutoResume(uint16_t *P)
```

!!! summary "引数"
	- uint16_t * `P` 



### setFrameTimeout()



```c
void IRrecvBase::setFrameTimeout(uint16_t frameTimeout)
```

!!! summary "引数"
	- uint16_t `frameTimeout` 



### blink13()



```c
void IRrecvBase::blink13(bool enableBlinkLED)
```

!!! summary "引数"
	- bool `enableBlinkLED` 



