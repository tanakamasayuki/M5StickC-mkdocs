# SPIClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_s_p_i_class.html)

## メンバー

### begin()



```c
void SPIClass::begin()
```



### usingInterrupt()



```c
void SPIClass::usingInterrupt(uint8_t interruptNumber)
```

!!! summary "引数"
	- uint8_t `interruptNumber` 



### notUsingInterrupt()



```c
void SPIClass::notUsingInterrupt(uint8_t interruptNumber)
```

!!! summary "引数"
	- uint8_t `interruptNumber` 



### beginTransaction()



```c
static void SPIClass::beginTransaction(SPISettings settings)
```

!!! summary "引数"
	- SPISettings `settings` 



### transfer()



```c
static uint8_t SPIClass::transfer(uint8_t data)
```

!!! summary "引数"
	- uint8_t `data` 

!!! note "戻り値"
	uint8_t



### transfer16()



```c
static uint16_t SPIClass::transfer16(uint16_t data)
```

!!! summary "引数"
	- uint16_t `data` 

!!! note "戻り値"
	uint16_t



### transfer()



```c
static void SPIClass::transfer(void *buf, size_t count)
```

!!! summary "引数"
	- void * `buf` 
	- size_t `count` 



### endTransaction()



```c
static void SPIClass::endTransaction(void)
```



### end()



```c
void SPIClass::end()
```



### setBitOrder()



```c
static void SPIClass::setBitOrder(uint8_t bitOrder)
```

!!! summary "引数"
	- uint8_t `bitOrder` 



### setDataMode()



```c
static void SPIClass::setDataMode(uint8_t dataMode)
```

!!! summary "引数"
	- uint8_t `dataMode` 



### setClockDivider()



```c
static void SPIClass::setClockDivider(uint8_t clockDiv)
```

!!! summary "引数"
	- uint8_t `clockDiv` 



### attachInterrupt()



```c
static void SPIClass::attachInterrupt()
```



### detachInterrupt()



```c
static void SPIClass::detachInterrupt()
```



