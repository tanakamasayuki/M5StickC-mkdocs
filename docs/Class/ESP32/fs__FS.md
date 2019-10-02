# fs::FS



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classfs_1_1_f_s.html)

## メンバー

### FS()



```c
fs::FS::FS(FSImplPtr impl)
```

!!! summary "引数"
	- FSImplPtr `impl` 



### open()



```c
File FS::open(const char *path, const char *mode=FILE_READ)
```

!!! summary "引数"
	- constchar * `path` 
	- constchar * `mode` 

!!! note "戻り値"
	File



### open()



```c
File FS::open(const String &path, const char *mode=FILE_READ)
```

!!! summary "引数"
	- constString & `path` 
	- constchar * `mode` 

!!! note "戻り値"
	File



### exists()



```c
bool FS::exists(const char *path)
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



### exists()



```c
bool FS::exists(const String &path)
```

!!! summary "引数"
	- constString & `path` 

!!! note "戻り値"
	bool



### remove()



```c
bool FS::remove(const char *path)
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



### remove()



```c
bool FS::remove(const String &path)
```

!!! summary "引数"
	- constString & `path` 

!!! note "戻り値"
	bool



### rename()



```c
bool FS::rename(const char *pathFrom, const char *pathTo)
```

!!! summary "引数"
	- constchar * `pathFrom` 
	- constchar * `pathTo` 

!!! note "戻り値"
	bool



### rename()



```c
bool FS::rename(const String &pathFrom, const String &pathTo)
```

!!! summary "引数"
	- constString & `pathFrom` 
	- constString & `pathTo` 

!!! note "戻り値"
	bool



### mkdir()



```c
bool FS::mkdir(const char *path)
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



### mkdir()



```c
bool FS::mkdir(const String &path)
```

!!! summary "引数"
	- constString & `path` 

!!! note "戻り値"
	bool



### rmdir()



```c
bool FS::rmdir(const char *path)
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



### rmdir()



```c
bool FS::rmdir(const String &path)
```

!!! summary "引数"
	- constString & `path` 

!!! note "戻り値"
	bool



