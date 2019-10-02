# fs::F_Fat



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classfs_1_1_f___fat.html)

## メンバー

### F_Fat()



```c
F_Fat::F_Fat(FSImplPtr impl)
```

!!! summary "引数"
	- FSImplPtr `impl` 



### begin()



```c
bool F_Fat::begin(bool formatOnFail=false, const char *basePath="/ffat", uint8_t maxOpenFiles=10, const char *partitionLabel=(char *) FFAT_PARTITION_LABEL)
```

!!! summary "引数"
	- bool `formatOnFail` 
	- constchar * `basePath` 
	- uint8_t `maxOpenFiles` 
	- constchar * `partitionLabel` 

!!! note "戻り値"
	bool



### format()



```c
bool F_Fat::format(bool full_wipe=FFAT_WIPE_QUICK, char *partitionLabel=(char *) FFAT_PARTITION_LABEL)
```

!!! summary "引数"
	- bool `full_wipe` 
	- char * `partitionLabel` 

!!! note "戻り値"
	bool



### totalBytes()



```c
size_t F_Fat::totalBytes()
```

!!! note "戻り値"
	size_t



### freeBytes()



```c
size_t F_Fat::freeBytes()
```

!!! note "戻り値"
	size_t



### end()



```c
void F_Fat::end()
```



### exists()



```c
bool F_Fat::exists(const char *path)
```

!!! summary "引数"
	- constchar * `path` 

!!! note "戻り値"
	bool



### exists()



```c
bool F_Fat::exists(const String &path)
```

!!! summary "引数"
	- constString & `path` 

!!! note "戻り値"
	bool



