# SoftwareSerial



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_software_serial.html)

## メンバー

### SoftwareSerial()



```c
SoftwareSerial::SoftwareSerial(uint8_t receivePin, uint8_t transmitPin, bool inverse_logic=false)
```

!!! summary "引数"
	- uint8_t `receivePin` 
	- uint8_t `transmitPin` 
	- bool `inverse_logic` 



### ~SoftwareSerial()



```c
SoftwareSerial::~SoftwareSerial()
```



### begin()



```c
void SoftwareSerial::begin(long speed)
```

!!! summary "引数"
	- long `speed` 



### listen()



```c
bool SoftwareSerial::listen()
```

!!! note "戻り値"
	bool



### end()



```c
void SoftwareSerial::end()
```



### isListening()



```c
bool SoftwareSerial::isListening()
```

!!! note "戻り値"
	bool



### stopListening()



```c
bool SoftwareSerial::stopListening()
```

!!! note "戻り値"
	bool



### overflow()



```c
bool SoftwareSerial::overflow()
```

!!! note "戻り値"
	bool



### peek()



```c
int SoftwareSerial::peek()
```

!!! note "戻り値"
	int



### write()



```c
size_t SoftwareSerial::write(uint8_t byte)
```

!!! summary "引数"
	- uint8_t `byte` 

!!! note "戻り値"
	size_t



### read()



```c
int SoftwareSerial::read()
```

!!! note "戻り値"
	int



### available()



```c
int SoftwareSerial::available()
```

!!! note "戻り値"
	int



### flush()



```c
void SoftwareSerial::flush()
```



### operator bool()



```c
SoftwareSerial::operator bool()
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



### handle_interrupt()



```c
void SoftwareSerial::handle_interrupt() __attribute__((__always_inline__))
```



