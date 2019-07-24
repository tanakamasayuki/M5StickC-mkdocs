# VFSImpl



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_v_f_s_impl.html)

## メンバー

### open()



```c
FileImplPtr VFSImpl::open(const char *path, const char *mode) override
```

!!! summary "引数"
	- constchar * `path` 
	- constchar * `mode` 

!!! note "戻り値"
	FileImplPtr



### exists()



```c
bool VFSImpl::exists(const char *path) override
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



### rename()



```c
bool VFSImpl::rename(const char *pathFrom, const char *pathTo) override
```

!!! summary "引数"
	- constchar * `pathFrom` 
	- constchar * `pathTo` 

!!! note "戻り値"
	bool



### remove()



```c
bool VFSImpl::remove(const char *path) override
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



### mkdir()



```c
bool VFSImpl::mkdir(const char *path) override
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



### rmdir()



```c
bool VFSImpl::rmdir(const char *path) override
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



