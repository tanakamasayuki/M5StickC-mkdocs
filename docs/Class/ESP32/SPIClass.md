# SPIClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_s_p_i_class.html)

## メンバー

### SPIClass()



```c
SPIClass::SPIClass(uint8_t spi_bus=HSPI)
```

!!! summary "引数"
	- uint8_t `spi_bus` 



### begin()



```c
void SPIClass::begin(int8_t sck=-1, int8_t miso=-1, int8_t mosi=-1, int8_t ss=-1)
```

!!! summary "引数"
	- int8_t `sck` 
	- int8_t `miso` 
	- int8_t `mosi` 
	- int8_t `ss` 



### end()



```c
void SPIClass::end()
```



### setHwCs()



```c
void SPIClass::setHwCs(bool use)
```

!!! summary "引数"
	- bool `use` 



### setBitOrder()



```c
void SPIClass::setBitOrder(uint8_t bitOrder)
```

!!! summary "引数"
	- uint8_t `bitOrder` 



### setDataMode()



```c
void SPIClass::setDataMode(uint8_t dataMode)
```

!!! summary "引数"
	- uint8_t `dataMode` 



### setFrequency()



```c
void SPIClass::setFrequency(uint32_t freq)
```

!!! summary "引数"
	- uint32_t `freq` 



### setClockDivider()



```c
void SPIClass::setClockDivider(uint32_t clockDiv)
```

!!! summary "引数"
	- uint32_t `clockDiv` 



### getClockDivider()



```c
uint32_t SPIClass::getClockDivider()
```

!!! note "戻り値"
	uint32_t



### beginTransaction()



```c
void SPIClass::beginTransaction(SPISettings settings)
```

!!! summary "引数"
	- SPISettings `settings` 



### endTransaction()



```c
void SPIClass::endTransaction(void)
```



### transfer()



```c
void SPIClass::transfer(uint8_t *data, uint32_t size)
```

!!! summary "引数"
	- uint8_t* `data` 
	- uint32_t `size` 



### transfer()



```c
uint8_t SPIClass::transfer(uint8_t data)
```

!!! summary "引数"
	- uint8_t `data` 

!!! note "戻り値"
	uint8_t



### transfer16()



```c
uint16_t SPIClass::transfer16(uint16_t data)
```

!!! summary "引数"
	- uint16_t `data` 

!!! note "戻り値"
	uint16_t



### transfer32()



```c
uint32_t SPIClass::transfer32(uint32_t data)
```

!!! summary "引数"
	- uint32_t `data` 

!!! note "戻り値"
	uint32_t



### transferBytes()



```c
void SPIClass::transferBytes(uint8_t *data, uint8_t *out, uint32_t size)
```

!!! summary "引数"
	- uint8_t* `data` uint8_t * data buffer. can be NULL for Read Only operation 
	- uint8_t* `out` uint8_t * output buffer. can be NULL for Write Only operation 
	- uint32_t `size` uint32_t 



### transferBits()



```c
void SPIClass::transferBits(uint32_t data, uint32_t *out, uint8_t bits)
```

!!! summary "引数"
	- uint32_t `data` 
	- uint32_t* `out` 
	- uint8_t `bits` 



### write()



```c
void SPIClass::write(uint8_t data)
```

!!! summary "引数"
	- uint8_t `data` 



### write16()



```c
void SPIClass::write16(uint16_t data)
```

!!! summary "引数"
	- uint16_t `data` 



### write32()



```c
void SPIClass::write32(uint32_t data)
```

!!! summary "引数"
	- uint32_t `data` 



### writeBytes()



```c
void SPIClass::writeBytes(uint8_t *data, uint32_t size)
```

!!! summary "引数"
	- uint8_t* `data` uint8_t * 
	- uint32_t `size` uint32_t 



### writePixels()



```c
void SPIClass::writePixels(const void *data, uint32_t size)
```

!!! summary "引数"
	- constvoid * `data` void * 
	- uint32_t `size` uint32_t 



### writePattern()



```c
void SPIClass::writePattern(uint8_t *data, uint8_t size, uint32_t repeat)
```

!!! summary "引数"
	- uint8_t* `data` uint8_t * 
	- uint8_t `size` uint8_t max for size is 64Byte 
	- uint32_t `repeat` uint32_t 



### bus()



```c
spi_t* SPIClass::bus()
```

!!! note "戻り値"
	spi_t*



