# BLEStream



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_b_l_e_stream.html)

## メンバー

### BLEStream()



```c
BLEStream::BLEStream(unsigned char req=0, unsigned char rdy=0, unsigned char rst=0)
```

!!! summary "引数"
	- unsigned char `req` 
	- unsigned char `rdy` 
	- unsigned char `rst` 



### begin()



```c
void BLEStream::begin(...)
```

!!! summary "引数"
	- ... `` 



### poll()



```c
bool BLEStream::poll()
```

!!! note "戻り値"
	bool



### end()



```c
void BLEStream::end()
```



### setFlushInterval()



```c
void BLEStream::setFlushInterval(int)
```

!!! summary "引数"
	- int `` 



### available()



```c
int BLEStream::available(void)
```

!!! note "戻り値"
	int



### peek()



```c
int BLEStream::peek(void)
```

!!! note "戻り値"
	int



### read()



```c
int BLEStream::read(void)
```

!!! note "戻り値"
	int



### flush()



```c
void BLEStream::flush(void)
```



### write()



```c
size_t BLEStream::write(uint8_t byte)
```

!!! summary "引数"
	- uint8_t `byte` 

!!! note "戻り値"
	size_t



### operator bool()



```c
BLEStream::operator bool()
```



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



