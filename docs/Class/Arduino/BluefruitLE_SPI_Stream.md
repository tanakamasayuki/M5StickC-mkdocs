# BluefruitLE_SPI_Stream



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_bluefruit_l_e___s_p_i___stream.html)

## メンバー

### BluefruitLE_SPI_Stream()



```c
BluefruitLE_SPI_Stream::BluefruitLE_SPI_Stream(int8_t csPin, int8_t irqPin, int8_t rstPin)
```

!!! summary "引数"
	- int8_t `csPin` 
	- int8_t `irqPin` 
	- int8_t `rstPin` 



### setLocalName()



```c
void BluefruitLE_SPI_Stream::setLocalName(const char *localName)
```

!!! summary "引数"
	- constchar * `localName` 



### setConnectionInterval()



```c
void BluefruitLE_SPI_Stream::setConnectionInterval(unsigned short minConnInterval, unsigned short maxConnInterval)
```

!!! summary "引数"
	- unsigned short `minConnInterval` 
	- unsigned short `maxConnInterval` 



### setFlushInterval()



```c
void BluefruitLE_SPI_Stream::setFlushInterval(int flushInterval)
```

!!! summary "引数"
	- int `flushInterval` 



### begin()



```c
void BluefruitLE_SPI_Stream::begin()
```



### poll()



```c
bool BluefruitLE_SPI_Stream::poll()
```

!!! note "戻り値"
	bool



### end()



```c
void BluefruitLE_SPI_Stream::end()
```



### write()



```c
size_t BluefruitLE_SPI_Stream::write(uint8_t byte)
```

!!! summary "引数"
	- uint8_t `byte` 

!!! note "戻り値"
	size_t



### available()



```c
int BluefruitLE_SPI_Stream::available()
```

!!! note "戻り値"
	int



### read()



```c
int BluefruitLE_SPI_Stream::read()
```

!!! note "戻り値"
	int



### peek()



```c
int BluefruitLE_SPI_Stream::peek()
```

!!! note "戻り値"
	int



### flush()



```c
void BluefruitLE_SPI_Stream::flush()
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



