# HardwareSerial



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_hardware_serial.html)

## メンバー

### HardwareSerial()



```c
HardwareSerial::HardwareSerial(volatile uint8_t *ubrrh, volatile uint8_t *ubrrl, volatile uint8_t *ucsra, volatile uint8_t *ucsrb, volatile uint8_t *ucsrc, volatile uint8_t *udr)
```

!!! summary "引数"
	- volatileuint8_t * `ubrrh` 
	- volatileuint8_t * `ubrrl` 
	- volatileuint8_t * `ucsra` 
	- volatileuint8_t * `ucsrb` 
	- volatileuint8_t * `ucsrc` 
	- volatileuint8_t * `udr` 



### begin()



```c
void HardwareSerial::begin(unsigned long baud)
```

!!! summary "引数"
	- unsigned long `baud` 



### begin()



```c
void HardwareSerial::begin(unsigned long, uint8_t)
```

!!! summary "引数"
	- uint8_t `` 



### end()



```c
void HardwareSerial::end()
```



### available()



```c
virtual int HardwareSerial::available(void)
```

!!! note "戻り値"
	int



### peek()



```c
virtual int HardwareSerial::peek(void)
```

!!! note "戻り値"
	int



### read()



```c
virtual int HardwareSerial::read(void)
```

!!! note "戻り値"
	int



### availableForWrite()



```c
virtual int HardwareSerial::availableForWrite(void)
```

!!! note "戻り値"
	int



### flush()



```c
virtual void HardwareSerial::flush(void)
```



### write()



```c
virtual size_t HardwareSerial::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

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



### operator bool()



```c
HardwareSerial::operator bool()
```



### _rx_complete_irq()



```c
void HardwareSerial::_rx_complete_irq(void)
```



### _tx_udr_empty_irq()



```c
void HardwareSerial::_tx_udr_empty_irq(void)
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



