# fs::File



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classfs_1_1_file.html)

## メンバー

### File()



```c
fs::File::File(FileImplPtr p=FileImplPtr())
```

!!! summary "引数"
	- FileImplPtr `p` 



### write()



```c
size_t File::write(uint8_t) override
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t File::write(const uint8_t *buf, size_t size) override
```

!!! summary "引数"
	- const* `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### available()



```c
int File::available() override
```

!!! note "戻り値"
	int



### read()



```c
int File::read() override
```

!!! note "戻り値"
	int



### peek()



```c
int File::peek() override
```

!!! note "戻り値"
	int



### flush()



```c
void File::flush() override
```



### read()



```c
size_t File::read(uint8_t *buf, size_t size)
```

!!! summary "引数"
	- uint8_t* `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### readBytes()



```c
size_t fs::File::readBytes(char *buffer, size_t length)
```

!!! summary "引数"
	- char * `buffer` 
	- size_t `length` 

!!! note "戻り値"
	size_t



### seek()



```c
bool File::seek(uint32_t pos, SeekMode mode)
```

!!! summary "引数"
	- uint32_t `pos` 
	- SeekMode `mode` 

!!! note "戻り値"
	bool



### seek()



```c
bool fs::File::seek(uint32_t pos)
```

!!! summary "引数"
	- uint32_t `pos` 

!!! note "戻り値"
	bool



### position()



```c
size_t File::position() const
```

!!! note "戻り値"
	size_t



### size()



```c
size_t File::size() const
```

!!! note "戻り値"
	size_t



### close()



```c
void File::close()
```



### operator bool()



```c
File::operator bool() const
```



### getLastWrite()



```c
time_t File::getLastWrite()
```

!!! note "戻り値"
	time_t



### name()



```c
const char * File::name() const
```

!!! note "戻り値"
	constchar *



### isDirectory()



```c
boolean File::isDirectory(void)
```

!!! note "戻り値"
	boolean



### openNextFile()



```c
File File::openNextFile(const char *mode=FILE_READ)
```

!!! summary "引数"
	- constchar * `mode` 

!!! note "戻り値"
	File



### rewindDirectory()



```c
void File::rewindDirectory(void)
```



