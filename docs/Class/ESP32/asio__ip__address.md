# asio::ip::address

Implements version-independent IP addresses. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1address.html)

## メンバー

### address()
Default constructor.


```c
ASIO_DECL asio::ip::address::address()
```

!!! note "戻り値"
	ASIO_DECL



### address()
Construct an address from an IPv4 address.


```c
ASIO_DECL asio::ip::address::address(const asio::ip::address_v4 &ipv4_address)
```

!!! summary "引数"
	- const& `ipv4_address` 

!!! note "戻り値"
	ASIO_DECL



### address()
Construct an address from an IPv6 address.


```c
ASIO_DECL asio::ip::address::address(const asio::ip::address_v6 &ipv6_address)
```

!!! summary "引数"
	- const& `ipv6_address` 

!!! note "戻り値"
	ASIO_DECL



### address()
Copy constructor.


```c
ASIO_DECL asio::ip::address::address(const address &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	ASIO_DECL



### operator=()
Assign from another address.


```c
ASIO_DECL address& asio::ip::address::operator=(const address &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	ASIO_DECL&



### operator=()
Assign from an IPv4 address.


```c
ASIO_DECL address& asio::ip::address::operator=(const asio::ip::address_v4 &ipv4_address)
```

!!! summary "引数"
	- const& `ipv4_address` 

!!! note "戻り値"
	ASIO_DECL&



### operator=()
Assign from an IPv6 address.


```c
ASIO_DECL address& asio::ip::address::operator=(const asio::ip::address_v6 &ipv6_address)
```

!!! summary "引数"
	- const& `ipv6_address` 

!!! note "戻り値"
	ASIO_DECL&



### is_v4()
Get whether the address is an IP version 4 address.


```c
bool asio::ip::address::is_v4() const
```

!!! note "戻り値"
	bool



### is_v6()
Get whether the address is an IP version 6 address.


```c
bool asio::ip::address::is_v6() const
```

!!! note "戻り値"
	bool



### to_v4()
Get the address as an IP version 4 address.


```c
ASIO_DECL asio::ip::address_v4 asio::ip::address::to_v4() const
```

!!! note "戻り値"
	ASIO_DECL



### to_v6()
Get the address as an IP version 6 address.


```c
ASIO_DECL asio::ip::address_v6 asio::ip::address::to_v6() const
```

!!! note "戻り値"
	ASIO_DECL



### to_string()
Get the address as a string.


```c
ASIO_DECL std::string asio::ip::address::to_string() const
```

!!! note "戻り値"
	ASIO_DECL



### to_string()
(Deprecated: Use other overload.) Get the address as a string.


```c
ASIO_DECL std::string asio::ip::address::to_string(asio::error_code &ec) const
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### is_loopback()
Determine whether the address is a loopback address.


```c
ASIO_DECL bool asio::ip::address::is_loopback() const
```

!!! note "戻り値"
	ASIO_DECL



### is_unspecified()
Determine whether the address is unspecified.


```c
ASIO_DECL bool asio::ip::address::is_unspecified() const
```

!!! note "戻り値"
	ASIO_DECL



### is_multicast()
Determine whether the address is a multicast address.


```c
ASIO_DECL bool asio::ip::address::is_multicast() const
```

!!! note "戻り値"
	ASIO_DECL



### from_string()


(Deprecated: Use .) Create an address from an IPv4 address string in dotted decimal form, or from an IPv6 address in hexadecimal notation. 
```c
address asio::ip::address::from_string(const char *str)
```

!!! summary "引数"
	- constchar * `str` 

!!! note "戻り値"
	address



### from_string()


(Deprecated: Use .) Create an address from an IPv4 address string in dotted decimal form, or from an IPv6 address in hexadecimal notation. 
```c
address asio::ip::address::from_string(const char *str, asio::error_code &ec)
```

!!! summary "引数"
	- constchar * `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	address



### from_string()


(Deprecated: Use .) Create an address from an IPv4 address string in dotted decimal form, or from an IPv6 address in hexadecimal notation. 
```c
address asio::ip::address::from_string(const std::string &str)
```

!!! summary "引数"
	- const& `str` 

!!! note "戻り値"
	address



### from_string()


(Deprecated: Use .) Create an address from an IPv4 address string in dotted decimal form, or from an IPv6 address in hexadecimal notation. 
```c
address asio::ip::address::from_string(const std::string &str, asio::error_code &ec)
```

!!! summary "引数"
	- const& `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	address















### make_address()


Create an address from an IPv4 address string in dotted decimal form, or from an IPv6 address in hexadecimal notation. 
```c
ASIO_DECL address make_address(const char *str)
```

!!! summary "引数"
	- constchar * `str` 

!!! note "戻り値"
	ASIO_DECL



### make_address()


Create an address from an IPv4 address string in dotted decimal form, or from an IPv6 address in hexadecimal notation. 
```c
ASIO_DECL address make_address(const char *str, asio::error_code &ec)
```

!!! summary "引数"
	- constchar * `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### make_address()


Create an address from an IPv4 address string in dotted decimal form, or from an IPv6 address in hexadecimal notation. 
```c
ASIO_DECL address make_address(const std::string &str)
```

!!! summary "引数"
	- const& `str` 

!!! note "戻り値"
	ASIO_DECL



### make_address()


Create an address from an IPv4 address string in dotted decimal form, or from an IPv6 address in hexadecimal notation. 
```c
ASIO_DECL address make_address(const std::string &str, asio::error_code &ec)
```

!!! summary "引数"
	- const& `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### operator<<()
Output an address as a string.

Used to output a human-readable string for a specified address.
```c
std::basic_ostream< Elem, Traits > & operator<<(std::basic_ostream< Elem, Traits > &os, const address &addr)
```

!!! summary "引数"
	- std::basic_ostream< Elem, Traits > & `os` The output stream to which the string will be written.
	- const& `addr` The address to be written.

!!! note "戻り値"
	std::basic_ostream< Elem, Traits > &



