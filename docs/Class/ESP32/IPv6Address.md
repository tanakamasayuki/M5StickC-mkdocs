# IPv6Address



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_i_pv6_address.html)

## メンバー

###  bytes

```c
uint8_t IPv6Address::bytes[16]
```


###  dword

```c
uint32_t IPv6Address::dword[4]
```








### IPv6Address()



```c
IPv6Address::IPv6Address()
```



### IPv6Address()



```c
IPv6Address::IPv6Address(const uint8_t *address)
```

!!! summary "引数"
	- const* `address` 



### IPv6Address()



```c
IPv6Address::IPv6Address(const uint32_t *address)
```

!!! summary "引数"
	- const* `address` 



### ~IPv6Address()



```c
virtual IPv6Address::~IPv6Address()
```



### fromString()



```c
bool IPv6Address::fromString(const char *address)
```

!!! summary "引数"
	- constchar * `address` 

!!! note "戻り値"
	bool



### fromString()



```c
bool IPv6Address::fromString(const String &address)
```

!!! summary "引数"
	- constString & `address` 

!!! note "戻り値"
	bool



### operator const uint8_t *()



```c
IPv6Address::operator const uint8_t *() const
```



### operator const uint32_t *()



```c
IPv6Address::operator const uint32_t *() const
```



### operator==()



```c
bool IPv6Address::operator==(const IPv6Address &addr) const
```

!!! summary "引数"
	- const& `addr` 

!!! note "戻り値"
	bool



### operator==()



```c
bool IPv6Address::operator==(const uint8_t *addr) const
```

!!! summary "引数"
	- const* `addr` 

!!! note "戻り値"
	bool



### operator[]()



```c
uint8_t IPv6Address::operator[](int index) const
```

!!! summary "引数"
	- int `index` 

!!! note "戻り値"
	uint8_t



### operator[]()



```c
uint8_t& IPv6Address::operator[](int index)
```

!!! summary "引数"
	- int `index` 

!!! note "戻り値"
	uint8_t&



### operator=()



```c
IPv6Address & IPv6Address::operator=(const uint8_t *address)
```

!!! summary "引数"
	- const* `address` 

!!! note "戻り値"
	IPv6Address&



### printTo()



```c
size_t IPv6Address::printTo(Print &p) const
```

!!! summary "引数"
	- Print& `p` 

!!! note "戻り値"
	size_t



### toString()



```c
String IPv6Address::toString() const
```

!!! note "戻り値"
	String



