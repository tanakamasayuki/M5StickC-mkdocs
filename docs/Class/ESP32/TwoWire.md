# TwoWire



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_two_wire.html)

## メンバー

### TwoWire()



```c
TwoWire::TwoWire(uint8_t bus_num)
```

!!! summary "引数"
	- uint8_t `bus_num` 



### ~TwoWire()



```c
TwoWire::~TwoWire()
```



### begin()



```c
bool TwoWire::begin(int sda=-1, int scl=-1, uint32_t frequency=0)
```

!!! summary "引数"
	- int `sda` 
	- int `scl` 
	- uint32_t `frequency` 

!!! note "戻り値"
	bool



### setClock()



```c
void TwoWire::setClock(uint32_t frequency)
```

!!! summary "引数"
	- uint32_t `frequency` 



### getClock()



```c
size_t TwoWire::getClock()
```

!!! note "戻り値"
	size_t



### setTimeOut()



```c
void TwoWire::setTimeOut(uint16_t timeOutMillis)
```

!!! summary "引数"
	- uint16_t `timeOutMillis` 



### getTimeOut()



```c
uint16_t TwoWire::getTimeOut()
```

!!! note "戻り値"
	uint16_t



### lastError()



```c
uint8_t TwoWire::lastError()
```

!!! note "戻り値"
	uint8_t



### getErrorText()



```c
char * TwoWire::getErrorText(uint8_t err)
```

!!! summary "引数"
	- uint8_t `err` 

!!! note "戻り値"
	char *



### writeTransmission()



```c
i2c_err_t TwoWire::writeTransmission(uint16_t address, uint8_t *buff, uint16_t size, bool sendStop=true)
```

!!! summary "引数"
	- uint16_t `address` 
	- uint8_t* `buff` 
	- uint16_t `size` 
	- bool `sendStop` 

!!! note "戻り値"
	i2c_err_t



### readTransmission()



```c
i2c_err_t TwoWire::readTransmission(uint16_t address, uint8_t *buff, uint16_t size, bool sendStop=true, uint32_t *readCount=NULL)
```

!!! summary "引数"
	- uint16_t `address` 
	- uint8_t* `buff` 
	- uint16_t `size` 
	- bool `sendStop` 
	- uint32_t* `readCount` 

!!! note "戻り値"
	i2c_err_t



### beginTransmission()



```c
void TwoWire::beginTransmission(uint16_t address)
```

!!! summary "引数"
	- uint16_t `address` 



### beginTransmission()



```c
void TwoWire::beginTransmission(uint8_t address)
```

!!! summary "引数"
	- uint8_t `address` 



### beginTransmission()



```c
void TwoWire::beginTransmission(int address)
```

!!! summary "引数"
	- int `address` 



### endTransmission()



```c
uint8_t TwoWire::endTransmission(bool sendStop)
```

!!! summary "引数"
	- bool `sendStop` 

!!! note "戻り値"
	uint8_t



### endTransmission()



```c
uint8_t TwoWire::endTransmission(void)
```

!!! note "戻り値"
	uint8_t



### requestFrom()



```c
uint8_t TwoWire::requestFrom(uint16_t address, uint8_t size, bool sendStop)
```

!!! summary "引数"
	- uint16_t `address` 
	- uint8_t `size` 
	- bool `sendStop` 

!!! note "戻り値"
	uint8_t



### requestFrom()



```c
uint8_t TwoWire::requestFrom(uint16_t address, uint8_t size, uint8_t sendStop)
```

!!! summary "引数"
	- uint16_t `address` 
	- uint8_t `size` 
	- uint8_t `sendStop` 

!!! note "戻り値"
	uint8_t



### requestFrom()



```c
uint8_t TwoWire::requestFrom(uint16_t address, uint8_t size)
```

!!! summary "引数"
	- uint16_t `address` 
	- uint8_t `size` 

!!! note "戻り値"
	uint8_t



### requestFrom()



```c
uint8_t TwoWire::requestFrom(uint8_t address, uint8_t size, uint8_t sendStop)
```

!!! summary "引数"
	- uint8_t `address` 
	- uint8_t `size` 
	- uint8_t `sendStop` 

!!! note "戻り値"
	uint8_t



### requestFrom()



```c
uint8_t TwoWire::requestFrom(uint8_t address, uint8_t size)
```

!!! summary "引数"
	- uint8_t `address` 
	- uint8_t `size` 

!!! note "戻り値"
	uint8_t



### requestFrom()



```c
uint8_t TwoWire::requestFrom(int address, int size, int sendStop)
```

!!! summary "引数"
	- int `address` 
	- int `size` 
	- int `sendStop` 

!!! note "戻り値"
	uint8_t



### requestFrom()



```c
uint8_t TwoWire::requestFrom(int address, int size)
```

!!! summary "引数"
	- int `address` 
	- int `size` 

!!! note "戻り値"
	uint8_t



### write()



```c
size_t TwoWire::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t TwoWire::write(const uint8_t *, size_t)
```

!!! summary "引数"
	- size_t `` 

!!! note "戻り値"
	size_t



### available()



```c
int TwoWire::available(void)
```

!!! note "戻り値"
	int



### read()



```c
int TwoWire::read(void)
```

!!! note "戻り値"
	int



### peek()



```c
int TwoWire::peek(void)
```

!!! note "戻り値"
	int



### flush()



```c
void TwoWire::flush(void)
```



### write()



```c
size_t TwoWire::write(const char *s)
```

!!! summary "引数"
	- constchar * `s` 

!!! note "戻り値"
	size_t



### write()



```c
size_t TwoWire::write(unsigned long n)
```

!!! summary "引数"
	- unsigned long `n` 

!!! note "戻り値"
	size_t



### write()



```c
size_t TwoWire::write(long n)
```

!!! summary "引数"
	- long `n` 

!!! note "戻り値"
	size_t



### write()



```c
size_t TwoWire::write(unsigned int n)
```

!!! summary "引数"
	- unsigned int `n` 

!!! note "戻り値"
	size_t



### write()



```c
size_t TwoWire::write(int n)
```

!!! summary "引数"
	- int `n` 

!!! note "戻り値"
	size_t



### onReceive()



```c
void TwoWire::onReceive(void(*)(int))
```

!!! summary "引数"
	- void(*)(int) `` 



### onRequest()



```c
void TwoWire::onRequest(void(*)(void))
```

!!! summary "引数"
	- void(*)(void) `` 



### setDebugFlags()



```c
uint32_t TwoWire::setDebugFlags(uint32_t setBits, uint32_t resetBits)
```

!!! summary "引数"
	- uint32_t `setBits` 
	- uint32_t `resetBits` 

!!! note "戻り値"
	uint32_t



### busy()



```c
bool TwoWire::busy()
```

!!! note "戻り値"
	bool



