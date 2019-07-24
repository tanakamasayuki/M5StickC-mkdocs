# Preferences



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_preferences.html)

## メンバー

### Preferences()



```c
Preferences::Preferences()
```



### ~Preferences()



```c
Preferences::~Preferences()
```



### begin()



```c
bool Preferences::begin(const char *name, bool readOnly=false)
```

!!! summary "引数"
	- constchar * `name` 
	- bool `readOnly` 

!!! note "戻り値"
	bool



### end()



```c
void Preferences::end()
```



### clear()



```c
bool Preferences::clear()
```

!!! note "戻り値"
	bool



### remove()



```c
bool Preferences::remove(const char *key)
```

!!! summary "引数"
	- constchar * `key` 

!!! note "戻り値"
	bool



### putChar()



```c
size_t Preferences::putChar(const char *key, int8_t value)
```

!!! summary "引数"
	- constchar * `key` 
	- int8_t `value` 

!!! note "戻り値"
	size_t



### putUChar()



```c
size_t Preferences::putUChar(const char *key, uint8_t value)
```

!!! summary "引数"
	- constchar * `key` 
	- uint8_t `value` 

!!! note "戻り値"
	size_t



### putShort()



```c
size_t Preferences::putShort(const char *key, int16_t value)
```

!!! summary "引数"
	- constchar * `key` 
	- int16_t `value` 

!!! note "戻り値"
	size_t



### putUShort()



```c
size_t Preferences::putUShort(const char *key, uint16_t value)
```

!!! summary "引数"
	- constchar * `key` 
	- uint16_t `value` 

!!! note "戻り値"
	size_t



### putInt()



```c
size_t Preferences::putInt(const char *key, int32_t value)
```

!!! summary "引数"
	- constchar * `key` 
	- int32_t `value` 

!!! note "戻り値"
	size_t



### putUInt()



```c
size_t Preferences::putUInt(const char *key, uint32_t value)
```

!!! summary "引数"
	- constchar * `key` 
	- uint32_t `value` 

!!! note "戻り値"
	size_t



### putLong()



```c
size_t Preferences::putLong(const char *key, int32_t value)
```

!!! summary "引数"
	- constchar * `key` 
	- int32_t `value` 

!!! note "戻り値"
	size_t



### putULong()



```c
size_t Preferences::putULong(const char *key, uint32_t value)
```

!!! summary "引数"
	- constchar * `key` 
	- uint32_t `value` 

!!! note "戻り値"
	size_t



### putLong64()



```c
size_t Preferences::putLong64(const char *key, int64_t value)
```

!!! summary "引数"
	- constchar * `key` 
	- int64_t `value` 

!!! note "戻り値"
	size_t



### putULong64()



```c
size_t Preferences::putULong64(const char *key, uint64_t value)
```

!!! summary "引数"
	- constchar * `key` 
	- uint64_t `value` 

!!! note "戻り値"
	size_t



### putFloat()



```c
size_t Preferences::putFloat(const char *key, float_t value)
```

!!! summary "引数"
	- constchar * `key` 
	- float_t `value` 

!!! note "戻り値"
	size_t



### putDouble()



```c
size_t Preferences::putDouble(const char *key, double_t value)
```

!!! summary "引数"
	- constchar * `key` 
	- double_t `value` 

!!! note "戻り値"
	size_t



### putBool()



```c
size_t Preferences::putBool(const char *key, bool value)
```

!!! summary "引数"
	- constchar * `key` 
	- bool `value` 

!!! note "戻り値"
	size_t



### putString()



```c
size_t Preferences::putString(const char *key, const char *value)
```

!!! summary "引数"
	- constchar * `key` 
	- constchar * `value` 

!!! note "戻り値"
	size_t



### putString()



```c
size_t Preferences::putString(const char *key, String value)
```

!!! summary "引数"
	- constchar * `key` 
	- String `value` 

!!! note "戻り値"
	size_t



### putBytes()



```c
size_t Preferences::putBytes(const char *key, const void *value, size_t len)
```

!!! summary "引数"
	- constchar * `key` 
	- constvoid * `value` 
	- size_t `len` 

!!! note "戻り値"
	size_t



### getChar()



```c
int8_t Preferences::getChar(const char *key, int8_t defaultValue=0)
```

!!! summary "引数"
	- constchar * `key` 
	- int8_t `defaultValue` 

!!! note "戻り値"
	int8_t



### getUChar()



```c
uint8_t Preferences::getUChar(const char *key, uint8_t defaultValue=0)
```

!!! summary "引数"
	- constchar * `key` 
	- uint8_t `defaultValue` 

!!! note "戻り値"
	uint8_t



### getShort()



```c
int16_t Preferences::getShort(const char *key, int16_t defaultValue=0)
```

!!! summary "引数"
	- constchar * `key` 
	- int16_t `defaultValue` 

!!! note "戻り値"
	int16_t



### getUShort()



```c
uint16_t Preferences::getUShort(const char *key, uint16_t defaultValue=0)
```

!!! summary "引数"
	- constchar * `key` 
	- uint16_t `defaultValue` 

!!! note "戻り値"
	uint16_t



### getInt()



```c
int32_t Preferences::getInt(const char *key, int32_t defaultValue=0)
```

!!! summary "引数"
	- constchar * `key` 
	- int32_t `defaultValue` 

!!! note "戻り値"
	int32_t



### getUInt()



```c
uint32_t Preferences::getUInt(const char *key, uint32_t defaultValue=0)
```

!!! summary "引数"
	- constchar * `key` 
	- uint32_t `defaultValue` 

!!! note "戻り値"
	uint32_t



### getLong()



```c
int32_t Preferences::getLong(const char *key, int32_t defaultValue=0)
```

!!! summary "引数"
	- constchar * `key` 
	- int32_t `defaultValue` 

!!! note "戻り値"
	int32_t



### getULong()



```c
uint32_t Preferences::getULong(const char *key, uint32_t defaultValue=0)
```

!!! summary "引数"
	- constchar * `key` 
	- uint32_t `defaultValue` 

!!! note "戻り値"
	uint32_t



### getLong64()



```c
int64_t Preferences::getLong64(const char *key, int64_t defaultValue=0)
```

!!! summary "引数"
	- constchar * `key` 
	- int64_t `defaultValue` 

!!! note "戻り値"
	int64_t



### getULong64()



```c
uint64_t Preferences::getULong64(const char *key, uint64_t defaultValue=0)
```

!!! summary "引数"
	- constchar * `key` 
	- uint64_t `defaultValue` 

!!! note "戻り値"
	uint64_t



### getFloat()



```c
float_t Preferences::getFloat(const char *key, float_t defaultValue=NAN)
```

!!! summary "引数"
	- constchar * `key` 
	- float_t `defaultValue` 

!!! note "戻り値"
	float_t



### getDouble()



```c
double_t Preferences::getDouble(const char *key, double_t defaultValue=NAN)
```

!!! summary "引数"
	- constchar * `key` 
	- double_t `defaultValue` 

!!! note "戻り値"
	double_t



### getBool()



```c
bool Preferences::getBool(const char *key, bool defaultValue=false)
```

!!! summary "引数"
	- constchar * `key` 
	- bool `defaultValue` 

!!! note "戻り値"
	bool



### getString()



```c
size_t Preferences::getString(const char *key, char *value, size_t maxLen)
```

!!! summary "引数"
	- constchar * `key` 
	- char * `value` 
	- size_t `maxLen` 

!!! note "戻り値"
	size_t



### getString()



```c
String Preferences::getString(const char *key, String defaultValue=String())
```

!!! summary "引数"
	- constchar * `key` 
	- String `defaultValue` 

!!! note "戻り値"
	String



### getBytesLength()



```c
size_t Preferences::getBytesLength(const char *key)
```

!!! summary "引数"
	- constchar * `key` 

!!! note "戻り値"
	size_t



### getBytes()



```c
size_t Preferences::getBytes(const char *key, void *buf, size_t maxLen)
```

!!! summary "引数"
	- constchar * `key` 
	- void * `buf` 
	- size_t `maxLen` 

!!! note "戻り値"
	size_t



### freeEntries()



```c
size_t Preferences::freeEntries()
```

!!! note "戻り値"
	size_t



