# 低レベルSPI(spi)

この関数群を通常使うことはありません。[SPIClass](../../Class/ESP32/SPIClass/)クラスを利用して呼び出してください。

## 利用例

- [Peripherals/SPI Master](../../Peripherals/SPI_Master/)
- [Peripherals/SPI Slave](../../Peripherals/SPI_Slave/)

## メンバー



### spiStartBus()



```c
spi_t* spiStartBus(uint8_t spi_num, uint32_t freq, uint8_t dataMode, uint8_t bitOrder)
```

!!! summary "引数"
	- uint8_t `spi_num` 
	- uint32_t `freq` 
	- uint8_t `dataMode` 
	- uint8_t `bitOrder` 

!!! note "戻り値"
	spi_t*



### spiStopBus()



```c
void spiStopBus(spi_t *spi)
```

!!! summary "引数"
	- spi_t* `spi` 

!!! note "戻り値"
	void



### spiAttachSCK()



```c
void spiAttachSCK(spi_t *spi, int8_t sck)
```

!!! summary "引数"
	- spi_t* `spi` 
	- int8_t `sck` 

!!! note "戻り値"
	void



### spiAttachMISO()



```c
void spiAttachMISO(spi_t *spi, int8_t miso)
```

!!! summary "引数"
	- spi_t* `spi` 
	- int8_t `miso` 

!!! note "戻り値"
	void



### spiAttachMOSI()



```c
void spiAttachMOSI(spi_t *spi, int8_t mosi)
```

!!! summary "引数"
	- spi_t* `spi` 
	- int8_t `mosi` 

!!! note "戻り値"
	void



### spiDetachSCK()



```c
void spiDetachSCK(spi_t *spi, int8_t sck)
```

!!! summary "引数"
	- spi_t* `spi` 
	- int8_t `sck` 

!!! note "戻り値"
	void



### spiDetachMISO()



```c
void spiDetachMISO(spi_t *spi, int8_t miso)
```

!!! summary "引数"
	- spi_t* `spi` 
	- int8_t `miso` 

!!! note "戻り値"
	void



### spiDetachMOSI()



```c
void spiDetachMOSI(spi_t *spi, int8_t mosi)
```

!!! summary "引数"
	- spi_t* `spi` 
	- int8_t `mosi` 

!!! note "戻り値"
	void



### spiAttachSS()



```c
void spiAttachSS(spi_t *spi, uint8_t cs_num, int8_t ss)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint8_t `cs_num` 
	- int8_t `ss` 

!!! note "戻り値"
	void



### spiDetachSS()



```c
void spiDetachSS(spi_t *spi, int8_t ss)
```

!!! summary "引数"
	- spi_t* `spi` 
	- int8_t `ss` 

!!! note "戻り値"
	void



### spiEnableSSPins()



```c
void spiEnableSSPins(spi_t *spi, uint8_t cs_mask)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint8_t `cs_mask` 

!!! note "戻り値"
	void



### spiDisableSSPins()



```c
void spiDisableSSPins(spi_t *spi, uint8_t cs_mask)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint8_t `cs_mask` 

!!! note "戻り値"
	void



### spiSSEnable()



```c
void spiSSEnable(spi_t *spi)
```

!!! summary "引数"
	- spi_t* `spi` 

!!! note "戻り値"
	void



### spiSSDisable()



```c
void spiSSDisable(spi_t *spi)
```

!!! summary "引数"
	- spi_t* `spi` 

!!! note "戻り値"
	void



### spiSSSet()



```c
void spiSSSet(spi_t *spi)
```

!!! summary "引数"
	- spi_t* `spi` 

!!! note "戻り値"
	void



### spiSSClear()



```c
void spiSSClear(spi_t *spi)
```

!!! summary "引数"
	- spi_t* `spi` 

!!! note "戻り値"
	void



### spiWaitReady()



```c
void spiWaitReady(spi_t *spi)
```

!!! summary "引数"
	- spi_t* `spi` 

!!! note "戻り値"
	void



### spiGetClockDiv()



```c
uint32_t spiGetClockDiv(spi_t *spi)
```

!!! summary "引数"
	- spi_t* `spi` 

!!! note "戻り値"
	uint32_t



### spiGetDataMode()



```c
uint8_t spiGetDataMode(spi_t *spi)
```

!!! summary "引数"
	- spi_t* `spi` 

!!! note "戻り値"
	uint8_t



### spiGetBitOrder()



```c
uint8_t spiGetBitOrder(spi_t *spi)
```

!!! summary "引数"
	- spi_t* `spi` 

!!! note "戻り値"
	uint8_t



### spiSetClockDiv()



```c
void spiSetClockDiv(spi_t *spi, uint32_t clockDiv)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint32_t `clockDiv` 

!!! note "戻り値"
	void



### spiSetDataMode()



```c
void spiSetDataMode(spi_t *spi, uint8_t dataMode)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint8_t `dataMode` 

!!! note "戻り値"
	void



### spiSetBitOrder()



```c
void spiSetBitOrder(spi_t *spi, uint8_t bitOrder)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint8_t `bitOrder` 

!!! note "戻り値"
	void



### spiWrite()



```c
void spiWrite(spi_t *spi, uint32_t *data, uint8_t len)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint32_t * `data` 
	- uint8_t `len` 

!!! note "戻り値"
	void



### spiWriteByte()



```c
void spiWriteByte(spi_t *spi, uint8_t data)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint8_t `data` 

!!! note "戻り値"
	void



### spiWriteWord()



```c
void spiWriteWord(spi_t *spi, uint16_t data)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint16_t `data` 

!!! note "戻り値"
	void



### spiWriteLong()



```c
void spiWriteLong(spi_t *spi, uint32_t data)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint32_t `data` 

!!! note "戻り値"
	void



### spiTransfer()



```c
void spiTransfer(spi_t *spi, uint32_t *out, uint8_t len)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint32_t * `out` 
	- uint8_t `len` 

!!! note "戻り値"
	void



### spiTransferByte()



```c
uint8_t spiTransferByte(spi_t *spi, uint8_t data)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint8_t `data` 

!!! note "戻り値"
	uint8_t



### spiTransferWord()



```c
uint16_t spiTransferWord(spi_t *spi, uint16_t data)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint16_t `data` 

!!! note "戻り値"
	uint16_t



### spiTransferLong()



```c
uint32_t spiTransferLong(spi_t *spi, uint32_t data)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint32_t `data` 

!!! note "戻り値"
	uint32_t



### spiTransferBytes()



```c
void spiTransferBytes(spi_t *spi, uint8_t *data, uint8_t *out, uint32_t size)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint8_t * `data` 
	- uint8_t * `out` 
	- uint32_t `size` 

!!! note "戻り値"
	void



### spiTransferBits()



```c
void spiTransferBits(spi_t *spi, uint32_t data, uint32_t *out, uint8_t bits)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint32_t `data` 
	- uint32_t * `out` 
	- uint8_t `bits` 

!!! note "戻り値"
	void



### spiTransaction()



```c
void spiTransaction(spi_t *spi, uint32_t clockDiv, uint8_t dataMode, uint8_t bitOrder)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint32_t `clockDiv` 
	- uint8_t `dataMode` 
	- uint8_t `bitOrder` 

!!! note "戻り値"
	void



### spiSimpleTransaction()



```c
void spiSimpleTransaction(spi_t *spi)
```

!!! summary "引数"
	- spi_t* `spi` 

!!! note "戻り値"
	void



### spiEndTransaction()



```c
void spiEndTransaction(spi_t *spi)
```

!!! summary "引数"
	- spi_t* `spi` 

!!! note "戻り値"
	void



### spiWriteNL()



```c
void spiWriteNL(spi_t *spi, const void *data, uint32_t len)
```

!!! summary "引数"
	- spi_t* `spi` 
	- const void * `data` 
	- uint32_t `len` 

!!! note "戻り値"
	void



### spiWriteByteNL()



```c
void spiWriteByteNL(spi_t *spi, uint8_t data)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint8_t `data` 

!!! note "戻り値"
	void



### spiWriteShortNL()



```c
void spiWriteShortNL(spi_t *spi, uint16_t data)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint16_t `data` 

!!! note "戻り値"
	void



### spiWriteLongNL()



```c
void spiWriteLongNL(spi_t *spi, uint32_t data)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint32_t `data` 

!!! note "戻り値"
	void



### spiWritePixelsNL()



```c
void spiWritePixelsNL(spi_t *spi, const void *data, uint32_t len)
```

!!! summary "引数"
	- spi_t* `spi` 
	- const void * `data` 
	- uint32_t `len` 

!!! note "戻り値"
	void



### spiTransferByteNL()



```c
uint8_t spiTransferByteNL(spi_t *spi, uint8_t data)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint8_t `data` 

!!! note "戻り値"
	uint8_t



### spiTransferShortNL()



```c
uint16_t spiTransferShortNL(spi_t *spi, uint16_t data)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint16_t `data` 

!!! note "戻り値"
	uint16_t



### spiTransferLongNL()



```c
uint32_t spiTransferLongNL(spi_t *spi, uint32_t data)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint32_t `data` 

!!! note "戻り値"
	uint32_t



### spiTransferBytesNL()



```c
void spiTransferBytesNL(spi_t *spi, const void *data_in, uint8_t *data_out, uint32_t len)
```

!!! summary "引数"
	- spi_t* `spi` 
	- const void * `data_in` 
	- uint8_t * `data_out` 
	- uint32_t `len` 

!!! note "戻り値"
	void



### spiTransferBitsNL()



```c
void spiTransferBitsNL(spi_t *spi, uint32_t data_in, uint32_t *data_out, uint8_t bits)
```

!!! summary "引数"
	- spi_t* `spi` 
	- uint32_t `data_in` 
	- uint32_t * `data_out` 
	- uint8_t `bits` 

!!! note "戻り値"
	void



### spiFrequencyToClockDiv()



```c
uint32_t spiFrequencyToClockDiv(uint32_t freq)
```

!!! summary "引数"
	- uint32_t `freq` 

!!! note "戻り値"
	uint32_t



### spiClockDivToFrequency()



```c
uint32_t spiClockDivToFrequency(uint32_t freq)
```

!!! summary "引数"
	- uint32_t `freq` 

!!! note "戻り値"
	uint32_t



