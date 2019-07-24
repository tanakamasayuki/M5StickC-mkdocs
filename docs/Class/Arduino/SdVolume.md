# SdVolume

Access FAT16 and FAT32 volumes on SD and SDHC cards. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_sd_volume.html)

## メンバー

### SdVolume()


Create an instance of  
```c
SdVolume::SdVolume(void)
```



### init()


Initialize a FAT volume. Try partition one first then try super floppy format.
```c
uint8_t SdVolume::init(Sd2Card *dev)
```

!!! summary "引数"
	- Sd2Card* `dev` The  where the volume is located.

!!! note "戻り値"
	uint8_t



### init()


Initialize a FAT volume.
```c
uint8_t SdVolume::init(Sd2Card *dev, uint8_t part)
```

!!! summary "引数"
	- Sd2Card* `dev` The SD card where the volume is located.
	- uint8_t `part` The partition to be used. Legal values for  are 1-4 to use the corresponding partition on a device formatted with a MBR, Master Boot Record, or zero if the device is formatted as a super floppy with the FAT boot sector in block zero.

!!! note "戻り値"
	uint8_t



### blocksPerCluster()




```c
uint8_t SdVolume::blocksPerCluster(void) const
```

!!! note "戻り値"
	uint8_t The volume's cluster size in blocks. 



### blocksPerFat()




```c
uint32_t SdVolume::blocksPerFat(void) const
```

!!! note "戻り値"
	uint32_t The number of blocks in one FAT. 



### clusterCount()




```c
uint32_t SdVolume::clusterCount(void) const
```

!!! note "戻り値"
	uint32_t The total number of clusters in the volume. 



### clusterSizeShift()




```c
uint8_t SdVolume::clusterSizeShift(void) const
```

!!! note "戻り値"
	uint8_t The shift count required to multiply by blocksPerCluster. 



### dataStartBlock()




```c
uint32_t SdVolume::dataStartBlock(void) const
```

!!! note "戻り値"
	uint32_t The logical block number for the start of file data. 



### fatCount()




```c
uint8_t SdVolume::fatCount(void) const
```

!!! note "戻り値"
	uint8_t The number of FAT structures on the volume. 



### fatStartBlock()




```c
uint32_t SdVolume::fatStartBlock(void) const
```

!!! note "戻り値"
	uint32_t The logical block number for the start of the first FAT. 



### fatType()




```c
uint8_t SdVolume::fatType(void) const
```

!!! note "戻り値"
	uint8_t The FAT type of the volume. Values are 12, 16 or 32. 



### rootDirEntryCount()




```c
uint32_t SdVolume::rootDirEntryCount(void) const
```

!!! note "戻り値"
	uint32_t The number of entries in the root directory for FAT16 volumes. 



### rootDirStart()




```c
uint32_t SdVolume::rootDirStart(void) const
```

!!! note "戻り値"
	uint32_t The logical block number for the start of the root directory on FAT16 volumes or the first cluster number on FAT32 volumes. 



### init()



```c
uint8_t SdVolume::init(Sd2Card &dev)
```

!!! summary "引数"
	- Sd2Card& `dev` 

!!! note "戻り値"
	uint8_t



### init()



```c
uint8_t SdVolume::init(Sd2Card &dev, uint8_t part)
```

!!! summary "引数"
	- Sd2Card& `dev` 
	- uint8_t `part` 

!!! note "戻り値"
	uint8_t



### cacheClear()


Clear the cache and returns a pointer to the cache. Used by the WaveRP recorder to do raw write to the SD card. Not for normal apps. 
```c
static uint8_t* SdVolume::cacheClear(void)
```

!!! note "戻り値"
	uint8_t *



### sdCard()


return a pointer to the  object for this volume 
```c
static Sd2Card* SdVolume::sdCard(void)
```

!!! note "戻り値"
	Sd2Card*



