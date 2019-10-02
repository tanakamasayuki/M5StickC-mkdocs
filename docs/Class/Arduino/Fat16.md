# Fat16

 implements a minimal Arduino FAT16 Library 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_fat16.html)

## メンバー

###  writeError
is set to true if an error occurs during a . Set  to false before calling  and/or  and check for true after calls to  and/or .
```c
bool Fat16::writeError
```


### Fat16()


create with file closed 
```c
Fat16::Fat16(void)
```



### curCluster()




```c
fat_t Fat16::curCluster(void) const
```

!!! note "戻り値"
	fat_t The current cluster number. 



### close()




```c
uint8_t Fat16::close(void)
```

!!! note "戻り値"
	uint8_t



### curPosition()




```c
uint32_t Fat16::curPosition(void) const
```

!!! note "戻り値"
	uint32_t The current file position. 



### dirEntry()


Return a files directory entry
```c
uint8_t Fat16::dirEntry(dir_t *dir)
```

!!! summary "引数"
	- dir_t* `dir` Location for return of the files directory entry.

!!! note "戻り値"
	uint8_t



### fileSize()




```c
uint32_t Fat16::fileSize(void) const
```

!!! note "戻り値"
	uint32_t The file's size in bytes. 



### isOpen()


Checks the file's open/closed status for this instance of . 

```c
uint8_t Fat16::isOpen(void) const
```

!!! note "戻り値"
	uint8_t The value true if a file is open otherwise false; 



### open()




```c
uint8_t Fat16::open(const char *fileName, uint8_t oflag)
```

!!! summary "引数"
	- constchar * `fileName` A valid 8.3 DOS name for a file in the root directory.
	- uint8_t `oflag` Values for  are constructed by a bitwise-inclusive OR of flags from the following list

!!! note "戻り値"
	uint8_t



### open()


Open a file by file index.
```c
uint8_t Fat16::open(uint16_t entry, uint8_t oflag)
```

!!! summary "引数"
	- uint16_t `entry` 
	- uint8_t `oflag` See .

!!! note "戻り値"
	uint8_t



### read()




```c
int16_t Fat16::read(void)
```

!!! note "戻り値"
	int16_t



### read()


Read data from a file at starting at the current file position.
```c
int16_t Fat16::read(void *buf, uint16_t nbyte)
```

!!! summary "引数"
	- void * `buf` Pointer to the location that will receive the data.
	- uint16_t `nbyte` Maximum number of bytes to read.

!!! note "戻り値"
	int16_t



### remove()





```c
uint8_t Fat16::remove(void)
```

!!! note "戻り値"
	uint8_t



### rewind()


Sets the file's current position to zero. 
```c
void Fat16::rewind(void)
```



### seekCur()


Seek to current position plus  bytes. See . 
```c
uint8_t Fat16::seekCur(uint32_t pos)
```

!!! summary "引数"
	- uint32_t `pos` 

!!! note "戻り値"
	uint8_t



### seekEnd()


Seek to end of file. See . 
```c
uint8_t Fat16::seekEnd(void)
```

!!! note "戻り値"
	uint8_t



### seekSet()


Sets the file's read/write position.
```c
uint8_t Fat16::seekSet(uint32_t pos)
```

!!! summary "引数"
	- uint32_t `pos` The new position in bytes from the beginning of the file.

!!! note "戻り値"
	uint8_t



### sync()




```c
uint8_t Fat16::sync(void)
```

!!! note "戻り値"
	uint8_t



### timestamp()


T_WRITE - Set the file's last write/modification date and time.
```c
uint8_t Fat16::timestamp(uint8_t flag, uint16_t year, uint8_t month, uint8_t day, uint8_t hour, uint8_t minute, uint8_t second)
```

!!! summary "引数"
	- uint8_t `flag` 
	- uint16_t `year` Valid range 1980 - 2107 inclusive.
	- uint8_t `month` Valid range 1 - 12 inclusive.
	- uint8_t `day` Valid range 1 - 31 inclusive.
	- uint8_t `hour` Valid range 0 - 23 inclusive.
	- uint8_t `minute` Valid range 0 - 59 inclusive.
	- uint8_t `second` Valid range 0 - 59 inclusive

!!! note "戻り値"
	uint8_t



### truncate()


Truncate a file to a specified length. The current file position will be maintained if it is less than or equal to  otherwise it will be set to end of file.
```c
uint8_t Fat16::truncate(uint32_t size)
```

!!! summary "引数"
	- uint32_t `size` 

!!! note "戻り値"
	uint8_t



### write()


Write data at the current position of an open file.
```c
int16_t Fat16::write(const void *buf, uint16_t nbyte)
```

!!! summary "引数"
	- constvoid * `buf` Pointer to the location of the data to be written.
	- uint16_t `nbyte` Number of bytes to write.

!!! note "戻り値"
	int16_t



### write()


Use  to check for errors. 
```c
void Fat16::write(uint8_t b)
```

!!! summary "引数"
	- uint8_t `b` 



### write()


Use  to check for errors. 
```c
void Fat16::write(const char *str)
```

!!! summary "引数"
	- constchar * `str` 



### write_P()


Use  to check for errors. 
```c
void Fat16::write_P(PGM_P str)
```

!!! summary "引数"
	- PGM_P `str` 



### writeln_P()


Use  to check for errors. 
```c
void Fat16::writeln_P(PGM_P str)
```

!!! summary "引数"
	- PGM_P `str` 



### clusterCount()




```c
static fat_t Fat16::clusterCount(void)
```

!!! note "戻り値"
	fat_t The count of clusters in the FAT16 volume. 



### clusterSize()




```c
static uint8_t Fat16::clusterSize(void)
```

!!! note "戻り値"
	uint8_t The number of 512 byte blocks in a cluster 



### dateTimeCallback()


See the  function. 
```c
static void Fat16::dateTimeCallback(void(*dateTime)(uint16_t *date, uint16_t *time))
```

!!! summary "引数"
	- timevoid(*)(uint16_t *date, uint16_t *) `dateTime` The user's callback function. The callback function is of the form:



### dateTimeCallbackCancel()


Cancel the date/time callback function. 
```c
static void Fat16::dateTimeCallbackCancel(void)
```



### init()


Initialize a FAT16 volume.
```c
uint8_t Fat16::init(SdCard *dev, uint8_t part)
```

!!! summary "引数"
	- SdCard* `dev` The  where the volume is located.
	- uint8_t `part` The partition to be used. Legal values for  are 1-4 to use the corresponding partition on a device formatted with a MBR, Master Boot Record, or zero if the device is formatted as a super floppy with the FAT boot sector in block zero.

!!! note "戻り値"
	uint8_t



### init()


First try partition 1 then try super floppy format.
```c
static uint8_t Fat16::init(SdCard *dev)
```

!!! summary "引数"
	- SdCard* `dev` The  where the volume is located.

!!! note "戻り値"
	uint8_t



### ls()


LS_SIZE - Print file size. 
```c
void Fat16::ls(uint8_t flags=0)
```

!!! summary "引数"
	- uint8_t `flags` The inclusive OR of



### printDirName()


Print the name field of a directory entry in 8.3 format to Serial.
```c
void Fat16::printDirName(const dir_t &dir, uint8_t width)
```

!!! summary "引数"
	- const& `dir` The directory structure containing the name. 
	- uint8_t `width` Blank fill name if length is less than . 



### printFatDate()


Format is yyyy-mm-dd.
```c
void Fat16::printFatDate(uint16_t fatDate)
```

!!! summary "引数"
	- uint16_t `fatDate` The date field from a directory entry. 



### printFatTime()


Format is hh:mm:ss.
```c
void Fat16::printFatTime(uint16_t fatTime)
```

!!! summary "引数"
	- uint16_t `fatTime` The time field from a directory entry. 



### printTwoDigits()


Print a value as two digits to Serial.
```c
void Fat16::printTwoDigits(uint8_t v)
```

!!! summary "引数"
	- uint8_t `v` Value to be printed, 0 <=  <= 99 



### readDir()


Unused entries and entries for long names are skipped.
```c
uint8_t Fat16::readDir(dir_t *dir, uint16_t *index, uint8_t skip=(DIR_ATT_VOLUME_ID|DIR_ATT_DIRECTORY))
```

!!! summary "引数"
	- dir_t* `dir` Location that will receive the entry.
	- uint16_t * `index` The search starts at  and  is updated with the root directory index of the found directory entry. If the entry is a file, it may be opened by calling .
	- uint8_t `skip` Skip entries that have these attributes. If  is not specified, the default is to skip the volume label and directories.

!!! note "戻り値"
	uint8_t



### remove()


The directory entry and all data for the file are deleted.
```c
uint8_t Fat16::remove(const char *fileName)
```

!!! summary "引数"
	- constchar * `fileName` The name of the file to be removed.

!!! note "戻り値"
	uint8_t



### rootDirEntryCount()




```c
static uint16_t Fat16::rootDirEntryCount(void)
```

!!! note "戻り値"
	uint16_t The number of entries in the root directory. 



