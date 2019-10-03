# UpdateClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_update_class.html)

## メンバー



### UpdateClass()



```c
UpdateClass::UpdateClass()
```



### onProgress()



```c
UpdateClass & UpdateClass::onProgress(THandlerFunction_Progress fn)
```

!!! summary "引数"
	- THandlerFunction_Progress `fn` 

!!! note "戻り値"
	UpdateClass&



### begin()



```c
bool UpdateClass::begin(size_t size=UPDATE_SIZE_UNKNOWN, int command=U_FLASH, int ledPin=-1, uint8_t ledOn=LOW)
```

!!! summary "引数"
	- size_t `size` 
	- int `command` 
	- int `ledPin` 
	- uint8_t `ledOn` 

!!! note "戻り値"
	bool



### write()



```c
size_t UpdateClass::write(uint8_t *data, size_t len)
```

!!! summary "引数"
	- uint8_t* `data` 
	- size_t `len` 

!!! note "戻り値"
	size_t



### writeStream()



```c
size_t UpdateClass::writeStream(Stream &data)
```

!!! summary "引数"
	- Stream& `data` 

!!! note "戻り値"
	size_t



### end()



```c
bool UpdateClass::end(bool evenIfRemaining=false)
```

!!! summary "引数"
	- bool `evenIfRemaining` 

!!! note "戻り値"
	bool



### abort()



```c
void UpdateClass::abort()
```



### printError()



```c
void UpdateClass::printError(Stream &out)
```

!!! summary "引数"
	- Stream& `out` 



### errorString()



```c
const char * UpdateClass::errorString()
```

!!! note "戻り値"
	constchar *



### setMD5()



```c
bool UpdateClass::setMD5(const char *expected_md5)
```

!!! summary "引数"
	- constchar * `expected_md5` 

!!! note "戻り値"
	bool



### md5String()



```c
String UpdateClass::md5String(void)
```

!!! note "戻り値"
	String



### md5()



```c
void UpdateClass::md5(uint8_t *result)
```

!!! summary "引数"
	- uint8_t* `result` 



### getError()



```c
uint8_t UpdateClass::getError()
```

!!! note "戻り値"
	uint8_t



### clearError()



```c
void UpdateClass::clearError()
```



### hasError()



```c
bool UpdateClass::hasError()
```

!!! note "戻り値"
	bool



### isRunning()



```c
bool UpdateClass::isRunning()
```

!!! note "戻り値"
	bool



### isFinished()



```c
bool UpdateClass::isFinished()
```

!!! note "戻り値"
	bool



### size()



```c
size_t UpdateClass::size()
```

!!! note "戻り値"
	size_t



### progress()



```c
size_t UpdateClass::progress()
```

!!! note "戻り値"
	size_t



### remaining()



```c
size_t UpdateClass::remaining()
```

!!! note "戻り値"
	size_t



### write()



```c
size_t UpdateClass::write(T &data)
```

!!! summary "引数"
	- T& `data` 

!!! note "戻り値"
	size_t



### canRollBack()



```c
bool UpdateClass::canRollBack()
```

!!! note "戻り値"
	bool



### rollBack()



```c
bool UpdateClass::rollBack()
```

!!! note "戻り値"
	bool



