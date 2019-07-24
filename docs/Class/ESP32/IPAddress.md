# IPAddress



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_i_p_address.html)

## メンバー

###  bytes

```c
uint8_t IPAddress::bytes[4]
```


###  dword

```c
uint32_t IPAddress::dword
```














### IPAddress()



```c
IPAddress::IPAddress()
```



### IPAddress()



```c
IPAddress::IPAddress(uint8_t first_octet, uint8_t second_octet, uint8_t third_octet, uint8_t fourth_octet)
```

!!! summary "引数"
	- uint8_t `first_octet` 
	- uint8_t `second_octet` 
	- uint8_t `third_octet` 
	- uint8_t `fourth_octet` 



### IPAddress()



```c
IPAddress::IPAddress(uint32_t address)
```

!!! summary "引数"
	- uint32_t `address` 



### IPAddress()



```c
IPAddress::IPAddress(const uint8_t *address)
```

!!! summary "引数"
	- const* `address` 



### ~IPAddress()



```c
virtual IPAddress::~IPAddress()
```



### fromString()



```c
bool IPAddress::fromString(const char *address)
```

!!! summary "引数"
	- constchar * `address` 

!!! note "戻り値"
	bool



### fromString()



```c
bool IPAddress::fromString(const String &address)
```

!!! summary "引数"
	- constString & `address` 

!!! note "戻り値"
	bool



### operator uint32_t()



```c
IPAddress::operator uint32_t() const
```



### operator==()



```c
bool IPAddress::operator==(const IPAddress &addr) const
```

!!! summary "引数"
	- const& `addr` 

!!! note "戻り値"
	bool



### operator==()



```c
bool IPAddress::operator==(const uint8_t *addr) const
```

!!! summary "引数"
	- const* `addr` 

!!! note "戻り値"
	bool



### operator[]()



```c
uint8_t IPAddress::operator[](int index) const
```

!!! summary "引数"
	- int `index` 

!!! note "戻り値"
	uint8_t



### operator[]()



```c
uint8_t& IPAddress::operator[](int index)
```

!!! summary "引数"
	- int `index` 

!!! note "戻り値"
	uint8_t&



### operator=()



```c
IPAddress & IPAddress::operator=(const uint8_t *address)
```

!!! summary "引数"
	- const* `address` 

!!! note "戻り値"
	IPAddress&



### operator=()



```c
IPAddress & IPAddress::operator=(uint32_t address)
```

!!! summary "引数"
	- uint32_t `address` 

!!! note "戻り値"
	IPAddress&



### printTo()



```c
size_t IPAddress::printTo(Print &p) const
```

!!! summary "引数"
	- Print& `p` 

!!! note "戻り値"
	size_t



### toString()



```c
String IPAddress::toString() const
```

!!! note "戻り値"
	String



