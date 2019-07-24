# EEPROMClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_e_e_p_r_o_m_class.html)

## メンバー

### EEPROMClass()



```c
EEPROMClass::EEPROMClass(uint32_t sector)
```

!!! summary "引数"
	- uint32_t `sector` 



### EEPROMClass()



```c
EEPROMClass::EEPROMClass(const char *name, uint32_t user_defined_size)
```

!!! summary "引数"
	- constchar * `name` 
	- uint32_t `user_defined_size` 



### EEPROMClass()



```c
EEPROMClass::EEPROMClass(void)
```



### ~EEPROMClass()



```c
EEPROMClass::~EEPROMClass(void)
```



### begin()



```c
bool EEPROMClass::begin(size_t size)
```

!!! summary "引数"
	- size_t `size` 

!!! note "戻り値"
	bool



### read()



```c
uint8_t EEPROMClass::read(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	uint8_t



### write()



```c
void EEPROMClass::write(int address, uint8_t val)
```

!!! summary "引数"
	- int `address` 
	- uint8_t `val` 



### length()



```c
uint16_t EEPROMClass::length()
```

!!! note "戻り値"
	uint16_t



### commit()



```c
bool EEPROMClass::commit()
```

!!! note "戻り値"
	bool



### end()



```c
void EEPROMClass::end()
```



### getDataPtr()



```c
uint8_t * EEPROMClass::getDataPtr()
```

!!! note "戻り値"
	uint8_t*



### get()



```c
T& EEPROMClass::get(int address, T &t)
```

!!! summary "引数"
	- int `address` 
	- T& `t` 

!!! note "戻り値"
	T&



### put()



```c
const T& EEPROMClass::put(int address, const T &t)
```

!!! summary "引数"
	- int `address` 
	- const& `t` 

!!! note "戻り値"
	const&



### readByte()



```c
uint8_t EEPROMClass::readByte(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	uint8_t



### readChar()



```c
int8_t EEPROMClass::readChar(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	int8_t



### readUChar()



```c
uint8_t EEPROMClass::readUChar(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	uint8_t



### readShort()



```c
int16_t EEPROMClass::readShort(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	int16_t



### readUShort()



```c
uint16_t EEPROMClass::readUShort(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	uint16_t



### readInt()



```c
int32_t EEPROMClass::readInt(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	int32_t



### readUInt()



```c
uint32_t EEPROMClass::readUInt(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	uint32_t



### readLong()



```c
int32_t EEPROMClass::readLong(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	int32_t



### readULong()



```c
uint32_t EEPROMClass::readULong(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	uint32_t



### readLong64()



```c
int64_t EEPROMClass::readLong64(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	int64_t



### readULong64()



```c
uint64_t EEPROMClass::readULong64(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	uint64_t



### readFloat()



```c
float_t EEPROMClass::readFloat(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	float_t



### readDouble()



```c
double_t EEPROMClass::readDouble(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	double_t



### readBool()



```c
bool EEPROMClass::readBool(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	bool



### readString()



```c
size_t EEPROMClass::readString(int address, char *value, size_t maxLen)
```

!!! summary "引数"
	- int `address` 
	- char * `value` 
	- size_t `maxLen` 

!!! note "戻り値"
	size_t



### readString()



```c
String EEPROMClass::readString(int address)
```

!!! summary "引数"
	- int `address` 

!!! note "戻り値"
	String



### readBytes()



```c
size_t EEPROMClass::readBytes(int address, void *value, size_t maxLen)
```

!!! summary "引数"
	- int `address` 
	- void * `value` 
	- size_t `maxLen` 

!!! note "戻り値"
	size_t



### readAll()



```c
T EEPROMClass::readAll(int address, T &)
```

!!! summary "引数"
	- int `address` 
	- T& `` 

!!! note "戻り値"
	T



### writeByte()



```c
size_t EEPROMClass::writeByte(int address, uint8_t value)
```

!!! summary "引数"
	- int `address` 
	- uint8_t `value` 

!!! note "戻り値"
	size_t



### writeChar()



```c
size_t EEPROMClass::writeChar(int address, int8_t value)
```

!!! summary "引数"
	- int `address` 
	- int8_t `value` 

!!! note "戻り値"
	size_t



### writeUChar()



```c
size_t EEPROMClass::writeUChar(int address, uint8_t value)
```

!!! summary "引数"
	- int `address` 
	- uint8_t `value` 

!!! note "戻り値"
	size_t



### writeShort()



```c
size_t EEPROMClass::writeShort(int address, int16_t value)
```

!!! summary "引数"
	- int `address` 
	- int16_t `value` 

!!! note "戻り値"
	size_t



### writeUShort()



```c
size_t EEPROMClass::writeUShort(int address, uint16_t value)
```

!!! summary "引数"
	- int `address` 
	- uint16_t `value` 

!!! note "戻り値"
	size_t



### writeInt()



```c
size_t EEPROMClass::writeInt(int address, int32_t value)
```

!!! summary "引数"
	- int `address` 
	- int32_t `value` 

!!! note "戻り値"
	size_t



### writeUInt()



```c
size_t EEPROMClass::writeUInt(int address, uint32_t value)
```

!!! summary "引数"
	- int `address` 
	- uint32_t `value` 

!!! note "戻り値"
	size_t



### writeLong()



```c
size_t EEPROMClass::writeLong(int address, int32_t value)
```

!!! summary "引数"
	- int `address` 
	- int32_t `value` 

!!! note "戻り値"
	size_t



### writeULong()



```c
size_t EEPROMClass::writeULong(int address, uint32_t value)
```

!!! summary "引数"
	- int `address` 
	- uint32_t `value` 

!!! note "戻り値"
	size_t



### writeLong64()



```c
size_t EEPROMClass::writeLong64(int address, int64_t value)
```

!!! summary "引数"
	- int `address` 
	- int64_t `value` 

!!! note "戻り値"
	size_t



### writeULong64()



```c
size_t EEPROMClass::writeULong64(int address, uint64_t value)
```

!!! summary "引数"
	- int `address` 
	- uint64_t `value` 

!!! note "戻り値"
	size_t



### writeFloat()



```c
size_t EEPROMClass::writeFloat(int address, float_t value)
```

!!! summary "引数"
	- int `address` 
	- float_t `value` 

!!! note "戻り値"
	size_t



### writeDouble()



```c
size_t EEPROMClass::writeDouble(int address, double_t value)
```

!!! summary "引数"
	- int `address` 
	- double_t `value` 

!!! note "戻り値"
	size_t



### writeBool()



```c
size_t EEPROMClass::writeBool(int address, bool value)
```

!!! summary "引数"
	- int `address` 
	- bool `value` 

!!! note "戻り値"
	size_t



### writeString()



```c
size_t EEPROMClass::writeString(int address, const char *value)
```

!!! summary "引数"
	- int `address` 
	- constchar * `value` 

!!! note "戻り値"
	size_t



### writeString()



```c
size_t EEPROMClass::writeString(int address, String value)
```

!!! summary "引数"
	- int `address` 
	- String `value` 

!!! note "戻り値"
	size_t



### writeBytes()



```c
size_t EEPROMClass::writeBytes(int address, const void *value, size_t len)
```

!!! summary "引数"
	- int `address` 
	- constvoid * `value` 
	- size_t `len` 

!!! note "戻り値"
	size_t



### writeAll()



```c
T EEPROMClass::writeAll(int address, const T &)
```

!!! summary "引数"
	- int `address` 
	- const& `` 

!!! note "戻り値"
	T



