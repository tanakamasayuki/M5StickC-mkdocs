# fs::FileImpl



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classfs_1_1_file_impl.html)

## メンバー

### ~FileImpl()



```c
virtual fs::FileImpl::~FileImpl()
```



### write()



```c
virtual size_t fs::FileImpl::write(const uint8_t *buf, size_t size)=0
```

!!! summary "引数"
	- const* `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### read()



```c
virtual size_t fs::FileImpl::read(uint8_t *buf, size_t size)=0
```

!!! summary "引数"
	- uint8_t* `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### flush()



```c
virtual void fs::FileImpl::flush()=0
```



### seek()



```c
virtual bool fs::FileImpl::seek(uint32_t pos, SeekMode mode)=0
```

!!! summary "引数"
	- uint32_t `pos` 
	- SeekMode `mode` 

!!! note "戻り値"
	bool



### position()



```c
virtual size_t fs::FileImpl::position() const =0
```

!!! note "戻り値"
	size_t



### size()



```c
virtual size_t fs::FileImpl::size() const =0
```

!!! note "戻り値"
	size_t



### close()



```c
virtual void fs::FileImpl::close()=0
```



### getLastWrite()



```c
virtual time_t fs::FileImpl::getLastWrite()=0
```

!!! note "戻り値"
	time_t



### name()



```c
virtual const char* fs::FileImpl::name() const =0
```

!!! note "戻り値"
	constchar *



### isDirectory()



```c
virtual boolean fs::FileImpl::isDirectory(void)=0
```

!!! note "戻り値"
	boolean



### openNextFile()



```c
virtual FileImplPtr fs::FileImpl::openNextFile(const char *mode)=0
```

!!! summary "引数"
	- constchar * `mode` 

!!! note "戻り値"
	FileImplPtr



### rewindDirectory()



```c
virtual void fs::FileImpl::rewindDirectory(void)=0
```



### operator bool()



```c
virtual fs::FileImpl::operator bool()=0
```



