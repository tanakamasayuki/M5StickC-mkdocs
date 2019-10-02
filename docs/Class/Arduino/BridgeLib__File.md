# BridgeLib::File



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_bridge_lib_1_1_file.html)

## メンバー

### File()



```c
BridgeLib::File::File(BridgeClass &b=Bridge)
```

!!! summary "引数"
	- BridgeClass& `b` 



### File()



```c
BridgeLib::File::File(const char *_filename, uint8_t _mode, BridgeClass &b=Bridge)
```

!!! summary "引数"
	- constchar * `_filename` 
	- uint8_t `_mode` 
	- BridgeClass& `b` 



### ~File()



```c
BridgeLib::File::~File()
```



### write()



```c
size_t BridgeLib::File::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t BridgeLib::File::write(const uint8_t *buf, size_t size)
```

!!! summary "引数"
	- constuint8_t * `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### read()



```c
int BridgeLib::File::read()
```

!!! note "戻り値"
	int



### peek()



```c
int BridgeLib::File::peek()
```

!!! note "戻り値"
	int



### available()



```c
int BridgeLib::File::available()
```

!!! note "戻り値"
	int



### flush()



```c
void BridgeLib::File::flush()
```



### read()



```c
int BridgeLib::File::read(void *buf, uint16_t nbyte)
```

!!! summary "引数"
	- void * `buf` 
	- uint16_t `nbyte` 

!!! note "戻り値"
	int



### seek()



```c
boolean BridgeLib::File::seek(uint32_t pos)
```

!!! summary "引数"
	- uint32_t `pos` 

!!! note "戻り値"
	boolean



### position()



```c
uint32_t BridgeLib::File::position()
```

!!! note "戻り値"
	uint32_t



### size()



```c
uint32_t BridgeLib::File::size()
```

!!! note "戻り値"
	uint32_t



### close()



```c
void BridgeLib::File::close()
```



### operator bool()



```c
BridgeLib::File::operator bool()
```



### name()



```c
const char * BridgeLib::File::name()
```

!!! note "戻り値"
	constchar *



### isDirectory()



```c
boolean BridgeLib::File::isDirectory()
```

!!! note "戻り値"
	boolean



### openNextFile()



```c
File BridgeLib::File::openNextFile(uint8_t mode=FILE_READ)
```

!!! summary "引数"
	- uint8_t `mode` 

!!! note "戻り値"
	File



### rewindDirectory()



```c
void BridgeLib::File::rewindDirectory(void)
```



