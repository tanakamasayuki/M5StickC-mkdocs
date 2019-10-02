# fs::FSImpl



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classfs_1_1_f_s_impl.html)

## メンバー

### FSImpl()



```c
fs::FSImpl::FSImpl()
```



### ~FSImpl()



```c
virtual fs::FSImpl::~FSImpl()
```



### open()



```c
virtual FileImplPtr fs::FSImpl::open(const char *path, const char *mode)=0
```

!!! summary "引数"
	- constchar * `path` 
	- constchar * `mode` 

!!! note "戻り値"
	FileImplPtr



### exists()



```c
virtual bool fs::FSImpl::exists(const char *path)=0
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



### rename()



```c
virtual bool fs::FSImpl::rename(const char *pathFrom, const char *pathTo)=0
```

!!! summary "引数"
	- constchar * `pathFrom` 
	- constchar * `pathTo` 

!!! note "戻り値"
	bool



### remove()



```c
virtual bool fs::FSImpl::remove(const char *path)=0
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



### mkdir()



```c
virtual bool fs::FSImpl::mkdir(const char *path)=0
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



### rmdir()



```c
virtual bool fs::FSImpl::rmdir(const char *path)=0
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



### mountpoint()



```c
void FSImpl::mountpoint(const char *)
```

!!! summary "引数"
	- constchar * `` 



### mountpoint()



```c
const char * FSImpl::mountpoint()
```

!!! note "戻り値"
	constchar *



