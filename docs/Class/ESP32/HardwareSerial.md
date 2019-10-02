# HardwareSerial



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_hardware_serial.html)

## メンバー

### HardwareSerial()



```c
HardwareSerial::HardwareSerial(int uart_nr)
```

!!! summary "引数"
	- int `uart_nr` 



### begin()



```c
void HardwareSerial::begin(unsigned long baud, uint32_t config=SERIAL_8N1, int8_t rxPin=-1, int8_t txPin=-1, bool invert=false, unsigned long timeout_ms=20000UL)
```

!!! summary "引数"
	- unsigned long `baud` 
	- uint32_t `config` 
	- int8_t `rxPin` 
	- int8_t `txPin` 
	- bool `invert` 
	- unsigned long `timeout_ms` 



### end()



```c
void HardwareSerial::end()
```



### updateBaudRate()



```c
void HardwareSerial::updateBaudRate(unsigned long baud)
```

!!! summary "引数"
	- unsigned long `baud` 



### available()



```c
int HardwareSerial::available(void)
```

!!! note "戻り値"
	int



### availableForWrite()



```c
int HardwareSerial::availableForWrite(void)
```

!!! note "戻り値"
	int



### peek()



```c
int HardwareSerial::peek(void)
```

!!! note "戻り値"
	int



### read()



```c
int HardwareSerial::read(void)
```

!!! note "戻り値"
	int



### flush()



```c
void HardwareSerial::flush(void)
```



### write()



```c
size_t HardwareSerial::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t HardwareSerial::write(const uint8_t *buffer, size_t size)
```

!!! summary "引数"
	- const* `buffer` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### write()



```c
size_t HardwareSerial::write(const char *s)
```

!!! summary "引数"
	- constchar * `s` 

!!! note "戻り値"
	size_t



### write()



```c
size_t HardwareSerial::write(unsigned long n)
```

!!! summary "引数"
	- unsigned long `n` 

!!! note "戻り値"
	size_t



### write()



```c
size_t HardwareSerial::write(long n)
```

!!! summary "引数"
	- long `n` 

!!! note "戻り値"
	size_t



### write()



```c
size_t HardwareSerial::write(unsigned int n)
```

!!! summary "引数"
	- unsigned int `n` 

!!! note "戻り値"
	size_t



### write()



```c
size_t HardwareSerial::write(int n)
```

!!! summary "引数"
	- int `n` 

!!! note "戻り値"
	size_t



### baudRate()



```c
uint32_t HardwareSerial::baudRate()
```

!!! note "戻り値"
	uint32_t



### operator bool()



```c
HardwareSerial::operator bool() const
```



### setRxBufferSize()



```c
size_t HardwareSerial::setRxBufferSize(size_t)
```

!!! summary "引数"
	- size_t `` 

!!! note "戻り値"
	size_t



### setDebugOutput()



```c
void HardwareSerial::setDebugOutput(bool)
```

!!! summary "引数"
	- bool `` 



