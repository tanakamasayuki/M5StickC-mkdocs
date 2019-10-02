# SDLib::SDClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_s_d_lib_1_1_s_d_class.html)

## メンバー

### begin()



```c
boolean SDLib::SDClass::begin(uint8_t csPin=SD_CHIP_SELECT_PIN)
```

!!! summary "引数"
	- uint8_t `csPin` 

!!! note "戻り値"
	boolean



### begin()



```c
boolean SDLib::SDClass::begin(uint32_t clock, uint8_t csPin)
```

!!! summary "引数"
	- uint32_t `clock` 
	- uint8_t `csPin` 

!!! note "戻り値"
	boolean



### end()



```c
void SDLib::SDClass::end()
```



### open()



```c
File SDLib::SDClass::open(const char *filename, uint8_t mode=FILE_READ)
```

!!! summary "引数"
	- constchar * `filename` 
	- uint8_t `mode` 

!!! note "戻り値"
	File



### open()



```c
File SDLib::SDClass::open(const String &filename, uint8_t mode=FILE_READ)
```

!!! summary "引数"
	- constString & `filename` 
	- uint8_t `mode` 

!!! note "戻り値"
	File



### exists()



```c
boolean SDLib::SDClass::exists(const char *filepath)
```

!!! summary "引数"
	- constchar * `filepath` 

!!! note "戻り値"
	boolean



### exists()



```c
boolean SDLib::SDClass::exists(const String &filepath)
```

!!! summary "引数"
	- constString & `filepath` 

!!! note "戻り値"
	boolean



### mkdir()



```c
boolean SDLib::SDClass::mkdir(const char *filepath)
```

!!! summary "引数"
	- constchar * `filepath` 

!!! note "戻り値"
	boolean



### mkdir()



```c
boolean SDLib::SDClass::mkdir(const String &filepath)
```

!!! summary "引数"
	- constString & `filepath` 

!!! note "戻り値"
	boolean



### remove()



```c
boolean SDLib::SDClass::remove(const char *filepath)
```

!!! summary "引数"
	- constchar * `filepath` 

!!! note "戻り値"
	boolean



### remove()



```c
boolean SDLib::SDClass::remove(const String &filepath)
```

!!! summary "引数"
	- constString & `filepath` 

!!! note "戻り値"
	boolean



### rmdir()



```c
boolean SDLib::SDClass::rmdir(const char *filepath)
```

!!! summary "引数"
	- constchar * `filepath` 

!!! note "戻り値"
	boolean



### rmdir()



```c
boolean SDLib::SDClass::rmdir(const String &filepath)
```

!!! summary "引数"
	- constString & `filepath` 

!!! note "戻り値"
	boolean



