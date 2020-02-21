# BridgeLib::FileSystemClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_bridge_lib_1_1_file_system_class.html)

## メンバー

### FileSystemClass()



```c
BridgeLib::FileSystemClass::FileSystemClass()
```



### FileSystemClass()



```c
BridgeLib::FileSystemClass::FileSystemClass(BridgeClass &_b)
```

!!! summary "引数"
	- BridgeClass& `_b` 



### begin()



```c
boolean BridgeLib::FileSystemClass::begin()
```

!!! note "戻り値"
	boolean



### open()



```c
File BridgeLib::FileSystemClass::open(const char *filename, uint8_t mode=FILE_READ)
```

!!! summary "引数"
	- constchar * `filename` 
	- uint8_t `mode` 

!!! note "戻り値"
	File



### exists()



```c
boolean BridgeLib::FileSystemClass::exists(const char *filepath)
```

!!! summary "引数"
	- constchar * `filepath` 

!!! note "戻り値"
	boolean



### mkdir()



```c
boolean BridgeLib::FileSystemClass::mkdir(const char *filepath)
```

!!! summary "引数"
	- constchar * `filepath` 

!!! note "戻り値"
	boolean



### remove()



```c
boolean BridgeLib::FileSystemClass::remove(const char *filepath)
```

!!! summary "引数"
	- constchar * `filepath` 

!!! note "戻り値"
	boolean



### rmdir()



```c
boolean BridgeLib::FileSystemClass::rmdir(const char *filepath)
```

!!! summary "引数"
	- constchar * `filepath` 

!!! note "戻り値"
	boolean



