# SdFile

Access FAT16 and FAT32 files on SD and SDHC cards. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_sd_file.html)

## メンバー

### SdFile()


Create an instance of . 
```c
SdFile::SdFile(void)
```



### clearUnbufferedRead()


writeError is set to true if an error occurs during a . Set writeError to false before calling  and/or  and check for true after calls to  and/or .Cancel unbuffered reads for this file. See  
```c
void SdFile::clearUnbufferedRead(void)
```



### close()




```c
uint8_t SdFile::close(void)
```

!!! note "戻り値"
	uint8_t



### contiguousRange()


Check for contiguous file and return its raw block range.
```c
uint8_t SdFile::contiguousRange(uint32_t *bgnBlock, uint32_t *endBlock)
```

!!! summary "引数"
	- uint32_t * `bgnBlock` the first block address for the file. 
	- uint32_t * `endBlock` the last block address for the file.

!!! note "戻り値"
	uint8_t



### createContiguous()


Create and open a new contiguous file of a specified size.
```c
uint8_t SdFile::createContiguous(SdFile *dirFile, const char *fileName, uint32_t size)
```

!!! summary "引数"
	- SdFile* `dirFile` The directory where the file will be created. 
	- constchar * `fileName` A valid DOS 8.3 file name. 
	- uint32_t `size` The desired file size.

!!! note "戻り値"
	uint8_t



### curCluster()




```c
uint32_t SdFile::curCluster(void) const
```

!!! note "戻り値"
	uint32_t The current cluster number for a file or directory. 



### curPosition()




```c
uint32_t SdFile::curPosition(void) const
```

!!! note "戻り値"
	uint32_t The current position for a file or directory. 



### dirBlock()




```c
uint32_t SdFile::dirBlock(void) const
```

!!! note "戻り値"
	uint32_t Address of the block that contains this file's directory. 



### dirEntry()


Return a files directory entry
```c
uint8_t SdFile::dirEntry(dir_t *dir)
```

!!! summary "引数"
	- dir_t* `dir` Location for return of the files directory entry.

!!! note "戻り値"
	uint8_t



### dirIndex()




```c
uint8_t SdFile::dirIndex(void) const
```

!!! note "戻り値"
	uint8_t Index of this file's directory in the block dirBlock. 



### fileSize()




```c
uint32_t SdFile::fileSize(void) const
```

!!! note "戻り値"
	uint32_t The total number of bytes in a file or directory. 



### firstCluster()




```c
uint32_t SdFile::firstCluster(void) const
```

!!! note "戻り値"
	uint32_t The first cluster number for a file or directory. 



### isDir()




```c
uint8_t SdFile::isDir(void) const
```

!!! note "戻り値"
	uint8_t True if this is a  for a directory else false. 



### isFile()




```c
uint8_t SdFile::isFile(void) const
```

!!! note "戻り値"
	uint8_t True if this is a  for a file else false. 



### isOpen()




```c
uint8_t SdFile::isOpen(void) const
```

!!! note "戻り値"
	uint8_t True if this is a  for an open file/directory else false. 



### isSubDir()




```c
uint8_t SdFile::isSubDir(void) const
```

!!! note "戻り値"
	uint8_t True if this is a  for a subdirectory else false. 



### isRoot()




```c
uint8_t SdFile::isRoot(void) const
```

!!! note "戻り値"
	uint8_t True if this is a  for the root directory. 



### ls()


LS_R - Recursive list of subdirectories.
```c
void SdFile::ls(uint8_t flags=0, uint8_t indent=0)
```

!!! summary "引数"
	- uint8_t `flags` The inclusive OR of
	- uint8_t `indent` Amount of space before file name. Used for recursive list to indicate subdirectory level. 



### makeDir()


Make a new directory.
```c
uint8_t SdFile::makeDir(SdFile *dir, const char *dirName)
```

!!! summary "引数"
	- SdFile* `dir` An open SdFat instance for the directory that will containing the new directory.
	- constchar * `dirName` A valid 8.3 DOS name for the new directory.

!!! note "戻り値"
	uint8_t



### open()


Open a file by index.
```c
uint8_t SdFile::open(SdFile *dirFile, uint16_t index, uint8_t oflag)
```

!!! summary "引数"
	- SdFile* `dirFile` An open SdFat instance for the directory.
	- uint16_t `index` The  of the directory entry for the file to be opened. The value for  is (directory file position)/32.
	- uint8_t `oflag` Values for  are constructed by a bitwise-inclusive OR of flags O_READ, O_WRITE, O_TRUNC, and O_SYNC.

!!! note "戻り値"
	uint8_t



### open()





```c
uint8_t SdFile::open(SdFile *dirFile, const char *fileName, uint8_t oflag)
```

!!! summary "引数"
	- SdFile* `dirFile` An open SdFat instance for the directory containing the file to be opened.
	- constchar * `fileName` A valid 8.3 DOS name for a file to be opened.
	- uint8_t `oflag` Values for  are constructed by a bitwise-inclusive OR of flags from the following list

!!! note "戻り値"
	uint8_t



### openRoot()


Open a volume's root directory.
```c
uint8_t SdFile::openRoot(SdVolume *vol)
```

!!! summary "引数"
	- SdVolume* `vol` The FAT volume containing the root directory to be opened.

!!! note "戻り値"
	uint8_t



### read()




```c
int16_t SdFile::read(void)
```

!!! note "戻り値"
	int16_t



### read()


Read data from a file starting at the current position.
```c
int16_t SdFile::read(void *buf, uint16_t nbyte)
```

!!! summary "引数"
	- void * `buf` Pointer to the location that will receive the data.
	- uint16_t `nbyte` Maximum number of bytes to read.

!!! note "戻り値"
	int16_t



### readDir()


Read the next directory entry from a directory file.
```c
int8_t SdFile::readDir(dir_t *dir)
```

!!! summary "引数"
	- dir_t* `dir` The dir_t struct that will receive the data.

!!! note "戻り値"
	int8_t



### remove()





```c
uint8_t SdFile::remove(void)
```

!!! note "戻り値"
	uint8_t



### rewind()


Set the file's current position to zero. 
```c
void SdFile::rewind(void)
```



### rmDir()





```c
uint8_t SdFile::rmDir(void)
```

!!! note "戻り値"
	uint8_t



### rmRfStar()





```c
uint8_t SdFile::rmRfStar(void)
```

!!! note "戻り値"
	uint8_t



### seekCur()


Set the files position to current position + . See . 
```c
uint8_t SdFile::seekCur(uint32_t pos)
```

!!! summary "引数"
	- uint32_t `pos` 

!!! note "戻り値"
	uint8_t



### seekEnd()


Set the files current position to end of file. Useful to position a file for append. See . 
```c
uint8_t SdFile::seekEnd(void)
```

!!! note "戻り値"
	uint8_t



### seekSet()


Sets a file's position.
```c
uint8_t SdFile::seekSet(uint32_t pos)
```

!!! summary "引数"
	- uint32_t `pos` The new position in bytes from the beginning of the file.

!!! note "戻り値"
	uint8_t



### setUnbufferedRead()


Not recommended for normal applications. 
```c
void SdFile::setUnbufferedRead(void)
```



### timestamp()


T_WRITE - Set the file's last write/modification date and time.
```c
uint8_t SdFile::timestamp(uint8_t flag, uint16_t year, uint8_t month, uint8_t day, uint8_t hour, uint8_t minute, uint8_t second)
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



### sync()




```c
uint8_t SdFile::sync(void)
```

!!! note "戻り値"
	uint8_t



### type()




```c
uint8_t SdFile::type(void) const
```

!!! note "戻り値"
	uint8_t



### truncate()


Truncate a file to a specified length. The current file position will be maintained if it is less than or equal to  otherwise it will be set to end of file.
```c
uint8_t SdFile::truncate(uint32_t size)
```

!!! summary "引数"
	- uint32_t `size` 

!!! note "戻り値"
	uint8_t



### unbufferedRead()




```c
uint8_t SdFile::unbufferedRead(void) const
```

!!! note "戻り値"
	uint8_t Unbuffered read flag. 



### volume()




```c
SdVolume* SdFile::volume(void) const
```

!!! note "戻り値"
	SdVolume*  that contains this file. 



### write()


Use SdFile::writeError to check for errors. 
```c
size_t SdFile::write(uint8_t b)
```

!!! summary "引数"
	- uint8_t `b` 

!!! note "戻り値"
	size_t



### write()


Write data to an open file.
```c
size_t SdFile::write(const void *buf, uint16_t nbyte)
```

!!! summary "引数"
	- constvoid * `buf` Pointer to the location of the data to be written.
	- uint16_t `nbyte` Number of bytes to write.

!!! note "戻り値"
	size_t



### write()


Use SdFile::writeError to check for errors. 
```c
size_t SdFile::write(const char *str)
```

!!! summary "引数"
	- constchar * `str` 

!!! note "戻り値"
	size_t



### contiguousRange()



```c
uint8_t SdFile::contiguousRange(uint32_t &bgnBlock, uint32_t &endBlock)
```

!!! summary "引数"
	- uint32_t & `bgnBlock` 
	- uint32_t & `endBlock` 

!!! note "戻り値"
	uint8_t



### createContiguous()



```c
uint8_t SdFile::createContiguous(SdFile &dirFile, const char *fileName, uint32_t size)
```

!!! summary "引数"
	- SdFile& `dirFile` 
	- constchar * `fileName` 
	- uint32_t `size` 

!!! note "戻り値"
	uint8_t



### dirEntry()



```c
uint8_t SdFile::dirEntry(dir_t &dir)
```

!!! summary "引数"
	- dir_t& `dir` 

!!! note "戻り値"
	uint8_t



### makeDir()



```c
uint8_t SdFile::makeDir(SdFile &dir, const char *dirName)
```

!!! summary "引数"
	- SdFile& `dir` 
	- constchar * `dirName` 

!!! note "戻り値"
	uint8_t



### open()



```c
uint8_t SdFile::open(SdFile &dirFile, const char *fileName, uint8_t oflag)
```

!!! summary "引数"
	- SdFile& `dirFile` 
	- constchar * `fileName` 
	- uint8_t `oflag` 

!!! note "戻り値"
	uint8_t



### open()



```c
uint8_t SdFile::open(SdFile &dirFile, const char *fileName)
```

!!! summary "引数"
	- SdFile& `dirFile` 
	- constchar * `fileName` 

!!! note "戻り値"
	uint8_t



### open()



```c
uint8_t SdFile::open(SdFile &dirFile, uint16_t index, uint8_t oflag)
```

!!! summary "引数"
	- SdFile& `dirFile` 
	- uint16_t `index` 
	- uint8_t `oflag` 

!!! note "戻り値"
	uint8_t



### openRoot()



```c
uint8_t SdFile::openRoot(SdVolume &vol)
```

!!! summary "引数"
	- SdVolume& `vol` 

!!! note "戻り値"
	uint8_t



### readDir()



```c
int8_t SdFile::readDir(dir_t &dir)
```

!!! summary "引数"
	- dir_t& `dir` 

!!! note "戻り値"
	int8_t



### dateTimeCallback()


See the  function. 
```c
static void SdFile::dateTimeCallback(void(*dateTime)(uint16_t *date, uint16_t *time))
```

!!! summary "引数"
	- timevoid(*)(uint16_t *date, uint16_t *) `dateTime` The user's call back function. The callback function is of the form:



### dateTimeCallbackCancel()


Cancel the date/time callback function. 
```c
static void SdFile::dateTimeCallbackCancel(void)
```



### dirName()


Format the name field of  into the 13 byte array  in standard 8.3 short name format.
```c
void SdFile::dirName(const dir_t &dir, char *name)
```

!!! summary "引数"
	- const& `dir` The directory structure containing the name. 
	- char * `name` A 13 byte char array for the formatted name. 



### printDirName()


Print the name field of a directory entry in 8.3 format to Serial.
```c
void SdFile::printDirName(const dir_t &dir, uint8_t width)
```

!!! summary "引数"
	- const& `dir` The directory structure containing the name. 
	- uint8_t `width` Blank fill name if length is less than . 



### printFatDate()


Format is yyyy-mm-dd.
```c
void SdFile::printFatDate(uint16_t fatDate)
```

!!! summary "引数"
	- uint16_t `fatDate` The date field from a directory entry. 



### printFatTime()


Format is hh:mm:ss.
```c
void SdFile::printFatTime(uint16_t fatTime)
```

!!! summary "引数"
	- uint16_t `fatTime` The time field from a directory entry. 



### printTwoDigits()


Print a value as two digits to Serial.
```c
void SdFile::printTwoDigits(uint8_t v)
```

!!! summary "引数"
	- uint8_t `v` Value to be printed, 0 <=  <= 99 



### remove()


The directory entry and all data for the file are deleted.
```c
uint8_t SdFile::remove(SdFile *dirFile, const char *fileName)
```

!!! summary "引数"
	- SdFile* `dirFile` The directory that contains the file. 
	- constchar * `fileName` The name of the file to be removed.

!!! note "戻り値"
	uint8_t



### dateTimeCallback()



```c
static void SdFile::dateTimeCallback(void(*dateTime)(uint16_t &date, uint16_t &time))
```

!!! summary "引数"
	- timevoid(*)(uint16_t &date, uint16_t &) `dateTime` 



### remove()



```c
static uint8_t SdFile::remove(SdFile &dirFile, const char *fileName)
```

!!! summary "引数"
	- SdFile& `dirFile` 
	- constchar * `fileName` 

!!! note "戻り値"
	uint8_t



