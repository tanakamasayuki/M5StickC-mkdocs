# MD5Builder



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_m_d5_builder.html)

## メンバー

### begin()



```c
void MD5Builder::begin(void)
```



### add()



```c
void MD5Builder::add(uint8_t *data, uint16_t len)
```

!!! summary "引数"
	- uint8_t* `data` 
	- uint16_t `len` 



### add()



```c
void MD5Builder::add(const char *data)
```

!!! summary "引数"
	- constchar * `data` 



### add()



```c
void MD5Builder::add(char *data)
```

!!! summary "引数"
	- char * `data` 



### add()



```c
void MD5Builder::add(String data)
```

!!! summary "引数"
	- String `data` 



### addHexString()



```c
void MD5Builder::addHexString(const char *data)
```

!!! summary "引数"
	- constchar * `data` 



### addHexString()



```c
void MD5Builder::addHexString(char *data)
```

!!! summary "引数"
	- char * `data` 



### addHexString()



```c
void MD5Builder::addHexString(String data)
```

!!! summary "引数"
	- String `data` 



### addStream()



```c
bool MD5Builder::addStream(Stream &stream, const size_t maxLen)
```

!!! summary "引数"
	- Stream& `stream` 
	- constsize_t `maxLen` 

!!! note "戻り値"
	bool



### calculate()



```c
void MD5Builder::calculate(void)
```



### getBytes()



```c
void MD5Builder::getBytes(uint8_t *output)
```

!!! summary "引数"
	- uint8_t* `output` 



### getChars()



```c
void MD5Builder::getChars(char *output)
```

!!! summary "引数"
	- char * `output` 



### toString()



```c
String MD5Builder::toString(void)
```

!!! note "戻り値"
	String



