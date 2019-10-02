# Sd2Card

Raw access to SD and SDHC flash memory cards. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_sd2_card.html)

## メンバー

### Sd2Card()


Construct an instance of . 
```c
Sd2Card::Sd2Card(void)
```



### cardSize()




```c
uint32_t Sd2Card::cardSize(void)
```

!!! note "戻り値"
	uint32_t



### erase()


Erase a range of blocks.
```c
uint8_t Sd2Card::erase(uint32_t firstBlock, uint32_t lastBlock)
```

!!! summary "引数"
	- uint32_t `firstBlock` The address of the first block in the range. 
	- uint32_t `lastBlock` The address of the last block in the range.

!!! note "戻り値"
	uint8_t



### eraseSingleBlockEnable()




```c
uint8_t Sd2Card::eraseSingleBlockEnable(void)
```

!!! note "戻り値"
	uint8_t



### errorCode()




```c
uint8_t Sd2Card::errorCode(void) const
```

!!! note "戻り値"
	uint8_t error code for last error. See  for a list of error codes. 



### errorData()




```c
uint8_t Sd2Card::errorData(void) const
```

!!! note "戻り値"
	uint8_t error data for last error. 



### init()


Initialize an SD flash memory card with default clock rate and chip select pin. See sd2Card::init(uint8_t sckRateID, uint8_t chipSelectPin). 
```c
uint8_t Sd2Card::init(void)
```

!!! note "戻り値"
	uint8_t



### init()


Initialize an SD flash memory card with the selected SPI clock rate and the default SD chip select pin. See sd2Card::init(uint8_t sckRateID, uint8_t chipSelectPin). 
```c
uint8_t Sd2Card::init(uint8_t sckRateID)
```

!!! summary "引数"
	- uint8_t `sckRateID` 

!!! note "戻り値"
	uint8_t



### init()


Initialize an SD flash memory card.
```c
uint8_t Sd2Card::init(uint8_t sckRateID, uint8_t chipSelectPin)
```

!!! summary "引数"
	- uint8_t `sckRateID` SPI clock rate selector. See . 
	- uint8_t `chipSelectPin` SD chip select pin number.

!!! note "戻り値"
	uint8_t



### partialBlockRead()


Use this for applications like the Adafruit Wave Shield.
```c
void Sd2Card::partialBlockRead(uint8_t value)
```

!!! summary "引数"
	- uint8_t `value` The value TRUE (non-zero) or FALSE (zero).) 



### partialBlockRead()


Returns the current value, true or false, for partial block read. 
```c
uint8_t Sd2Card::partialBlockRead(void) const
```

!!! note "戻り値"
	uint8_t



### readBlock()


Read a 512 byte block from an SD card device.
```c
uint8_t Sd2Card::readBlock(uint32_t block, uint8_t *dst)
```

!!! summary "引数"
	- uint32_t `block` Logical block to be read. 
	- uint8_t * `dst` Pointer to the location that will receive the data.

!!! note "戻り値"
	uint8_t



### readData()


Read part of a 512 byte block from an SD card.
```c
uint8_t Sd2Card::readData(uint32_t block, uint16_t offset, uint16_t count, uint8_t *dst)
```

!!! summary "引数"
	- uint32_t `block` Logical block to be read. 
	- uint16_t `offset` Number of bytes to skip at start of block 
	- uint16_t `count` Number of bytes to read 
	- uint8_t * `dst` Pointer to the location that will receive the data. 

!!! note "戻り値"
	uint8_t



### readCID()


Read a cards  register. The  contains card identification information such as Manufacturer ID, Product name, Product serial number and Manufacturing date. 
```c
uint8_t Sd2Card::readCID(cid_t *cid)
```

!!! summary "引数"
	- cid_t* `cid` 

!!! note "戻り値"
	uint8_t



### readCSD()


Read a cards  register. The  contains Card-Specific Data that provides information regarding access to the card's contents. 
```c
uint8_t Sd2Card::readCSD(csd_t *csd)
```

!!! summary "引数"
	- csd_t* `csd` 

!!! note "戻り値"
	uint8_t



### readEnd()


Skip remaining data in a block when in partial block read mode. 
```c
void Sd2Card::readEnd(void)
```



### setSckRate()




```c
uint8_t Sd2Card::setSckRate(uint8_t sckRateID)
```

!!! summary "引数"
	- uint8_t `sckRateID` A value in the range [0, 6].

!!! note "戻り値"
	uint8_t



### setSpiClock()



```c
uint8_t Sd2Card::setSpiClock(uint32_t clock)
```

!!! summary "引数"
	- uint32_t `clock` 

!!! note "戻り値"
	uint8_t



### type()


Return the card type: SD V1, SD V2 or SDHC 
```c
uint8_t Sd2Card::type(void) const
```

!!! note "戻り値"
	uint8_t



### writeBlock()


Writes a 512 byte block to an SD card.
```c
uint8_t Sd2Card::writeBlock(uint32_t blockNumber, const uint8_t *src)
```

!!! summary "引数"
	- uint32_t `blockNumber` Logical block to be written. 
	- constuint8_t * `src` Pointer to the location of the data to be written. 

!!! note "戻り値"
	uint8_t



### writeData()


Write one data block in a multiple block write sequence 
```c
uint8_t Sd2Card::writeData(const uint8_t *src)
```

!!! summary "引数"
	- constuint8_t * `src` 

!!! note "戻り値"
	uint8_t



### writeStart()


Start a write multiple blocks sequence.
```c
uint8_t Sd2Card::writeStart(uint32_t blockNumber, uint32_t eraseCount)
```

!!! summary "引数"
	- uint32_t `blockNumber` Address of first block in sequence. 
	- uint32_t `eraseCount` The number of blocks to be pre-erased.

!!! note "戻り値"
	uint8_t



### writeStop()




```c
uint8_t Sd2Card::writeStop(void)
```

!!! note "戻り値"
	uint8_t



