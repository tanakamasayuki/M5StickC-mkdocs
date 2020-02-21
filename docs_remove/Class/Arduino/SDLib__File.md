# SDLib::File



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_s_d_lib_1_1_file.html)

## メンバー

### File()



```c
File::File(SdFile f, const char *name)
```

!!! summary "引数"
	- SdFile `f` 
	- constchar * `name` 



### File()



```c
File::File(void)
```



### write()



```c
size_t File::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t File::write(const uint8_t *buf, size_t size)
```

!!! summary "引数"
	- constuint8_t * `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### read()



```c
int File::read()
```

!!! note "戻り値"
	int



### peek()



```c
int File::peek()
```

!!! note "戻り値"
	int



### available()



```c
int File::available()
```

!!! note "戻り値"
	int



### flush()



```c
void File::flush()
```



### read()



```c
int File::read(void *buf, uint16_t nbyte)
```

!!! summary "引数"
	- void * `buf` 
	- uint16_t `nbyte` 

!!! note "戻り値"
	int



### seek()



```c
boolean File::seek(uint32_t pos)
```

!!! summary "引数"
	- uint32_t `pos` 

!!! note "戻り値"
	boolean



### position()



```c
uint32_t File::position()
```

!!! note "戻り値"
	uint32_t



### size()



```c
uint32_t File::size()
```

!!! note "戻り値"
	uint32_t



### close()



```c
void File::close()
```



### operator bool()



```c
File::operator bool()
```



### name()



```c
char * File::name()
```

!!! note "戻り値"
	char *



### isDirectory()



```c
boolean File::isDirectory(void)
```

!!! note "戻り値"
	boolean



### openNextFile()



```c
File SDLib::File::openNextFile(uint8_t mode=O_RDONLY)
```

!!! summary "引数"
	- uint8_t `mode` 

!!! note "戻り値"
	File



### rewindDirectory()



```c
void SDLib::File::rewindDirectory(void)
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



