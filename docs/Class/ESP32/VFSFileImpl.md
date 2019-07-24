# VFSFileImpl



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_v_f_s_file_impl.html)

## メンバー

### VFSFileImpl()



```c
VFSFileImpl::VFSFileImpl(VFSImpl *fs, const char *path, const char *mode)
```

!!! summary "引数"
	- VFSImpl* `fs` 
	- constchar * `path` 
	- constchar * `mode` 



### ~VFSFileImpl()



```c
VFSFileImpl::~VFSFileImpl() override
```



### write()



```c
size_t VFSFileImpl::write(const uint8_t *buf, size_t size) override
```

!!! summary "引数"
	- const* `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### read()



```c
size_t VFSFileImpl::read(uint8_t *buf, size_t size) override
```

!!! summary "引数"
	- uint8_t* `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### flush()



```c
void VFSFileImpl::flush() override
```



### seek()



```c
bool VFSFileImpl::seek(uint32_t pos, SeekMode mode) override
```

!!! summary "引数"
	- uint32_t `pos` 
	- SeekMode `mode` 

!!! note "戻り値"
	bool



### position()



```c
size_t VFSFileImpl::position() const override
```

!!! note "戻り値"
	size_t



### size()



```c
size_t VFSFileImpl::size() const override
```

!!! note "戻り値"
	size_t



### close()



```c
void VFSFileImpl::close() override
```



### name()



```c
const char * VFSFileImpl::name() const override
```

!!! note "戻り値"
	constchar *



### getLastWrite()



```c
time_t VFSFileImpl::getLastWrite() override
```

!!! note "戻り値"
	time_t



### isDirectory()



```c
boolean VFSFileImpl::isDirectory(void) override
```

!!! note "戻り値"
	boolean



### openNextFile()



```c
FileImplPtr VFSFileImpl::openNextFile(const char *mode) override
```

!!! summary "引数"
	- constchar * `mode` 

!!! note "戻り値"
	FileImplPtr



### rewindDirectory()



```c
void VFSFileImpl::rewindDirectory(void) override
```



### operator bool()



```c
VFSFileImpl::operator bool()
```



