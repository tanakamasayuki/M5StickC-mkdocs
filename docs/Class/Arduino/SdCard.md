# SdCard

Hardware access class for SD flash cards 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_sd_card.html)

## メンバー

###  errorCode
Code for a SD error. See  for definitions.
```c
uint8_t SdCard::errorCode
```


###  errorData
Data that may be helpful in determining the cause of an error
```c
uint8_t SdCard::errorData
```


### cardSize()


Determine the size of a standard SD flash memory card 

```c
uint32_t SdCard::cardSize(void)
```

!!! note "戻り値"
	uint32_t The number of 512 byte data blocks in the card 



### init()


Initialize an SD flash memory card with default clock rate and chip select pin. See . 
```c
uint8_t SdCard::init(void)
```

!!! note "戻り値"
	uint8_t



### init()


Initialize an SD flash memory card with the selected SPI clock rate and the default SD chip select pin. See . 
```c
uint8_t SdCard::init(uint8_t speed)
```

!!! summary "引数"
	- uint8_t `speed` 

!!! note "戻り値"
	uint8_t



### init()


Initialize a SD flash memory card.
```c
uint8_t SdCard::init(uint8_t speed, uint8_t chipselectPin)
```

!!! summary "引数"
	- uint8_t `speed` Set SPI Frequency to F_CPU/2 if speed = 0 or F_CPU/4 if speed = 1. 
	- uint8_t `chipselectPin` 

!!! note "戻り値"
	uint8_t



### readBlock()


Reads a 512 byte block from a storage device.
```c
uint8_t SdCard::readBlock(uint32_t block, uint8_t *dst)
```

!!! summary "引数"
	- uint32_t `block` 
	- uint8_t * `dst` Pointer to the location that will receive the data. 

!!! note "戻り値"
	uint8_t



### readCID()


Read the  register which contains info about the card. This includes Manufacturer ID, OEM ID, product name, version, serial number, and manufacturing date. 
```c
uint8_t SdCard::readCID(cid_t *cid)
```

!!! summary "引数"
	- cid_t* `cid` 

!!! note "戻り値"
	uint8_t



### writeBlock()


Writes a 512 byte block to a storage device.
```c
uint8_t SdCard::writeBlock(uint32_t block, const uint8_t *src)
```

!!! summary "引数"
	- uint32_t `block` 
	- constuint8_t * `src` Pointer to the location of the data to be written. 

!!! note "戻り値"
	uint8_t



