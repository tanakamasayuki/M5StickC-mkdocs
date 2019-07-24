# TwoWire



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_two_wire.html)

## メンバー

### TwoWire()



```c
TwoWire::TwoWire()
```



### begin()



```c
void TwoWire::begin()
```



### begin()



```c
void TwoWire::begin(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 



### begin()



```c
void TwoWire::begin(int)
```

!!! summary "引数"
	- int `` 



### end()



```c
void TwoWire::end()
```



### setClock()



```c
void TwoWire::setClock(uint32_t)
```

!!! summary "引数"
	- uint32_t `` 



### beginTransmission()



```c
void TwoWire::beginTransmission(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 



### beginTransmission()



```c
void TwoWire::beginTransmission(int)
```

!!! summary "引数"
	- int `` 



### endTransmission()



```c
uint8_t TwoWire::endTransmission(void)
```

!!! note "戻り値"
	uint8_t



### endTransmission()



```c
uint8_t TwoWire::endTransmission(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	uint8_t



### requestFrom()



```c
uint8_t TwoWire::requestFrom(uint8_t, uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	uint8_t



### requestFrom()



```c
uint8_t TwoWire::requestFrom(uint8_t, uint8_t, uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	uint8_t



### requestFrom()



```c
uint8_t TwoWire::requestFrom(uint8_t, uint8_t, uint32_t, uint8_t, uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	uint8_t



### requestFrom()



```c
uint8_t TwoWire::requestFrom(int, int)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	uint8_t



### requestFrom()



```c
uint8_t TwoWire::requestFrom(int, int, int)
```

!!! summary "引数"
	- int `` 

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



### write()



```c
virtual size_t Print::write(uint8_t)=0
```

!!! note "戻り値"
	size_t



### write()



```c
size_t Print::write(const char *str)
```

!!! note "戻り値"
	size_t



### write()



```c
size_t Print::write(const uint8_t *buffer, size_t size)
```

!!! note "戻り値"
	size_t



### write()



```c
size_t Print::write(const char *buffer, size_t size)
```

!!! note "戻り値"
	size_t



