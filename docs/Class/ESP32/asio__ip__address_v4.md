# asio::ip::address_v4

Implements IP version 4 style addresses. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1address__v4.html)

## メンバー





### address_v4()
Default constructor.


```c
asio::ip::address_v4::address_v4()
```



### address_v4()
Construct an address from raw bytes.


```c
ASIO_DECL asio::ip::address_v4::address_v4(const bytes_type &bytes)
```

!!! summary "引数"
	- const& `bytes` 

!!! note "戻り値"
	ASIO_DECL



### address_v4()
Construct an address from an unsigned integer in host byte order.


```c
ASIO_DECL asio::ip::address_v4::address_v4(uint_type addr)
```

!!! summary "引数"
	- uint_type `addr` 

!!! note "戻り値"
	ASIO_DECL



### address_v4()
Copy constructor.


```c
asio::ip::address_v4::address_v4(const address_v4 &other)
```

!!! summary "引数"
	- const& `other` 



### operator=()
Assign from another address.


```c
address_v4& asio::ip::address_v4::operator=(const address_v4 &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	address_v4&



### to_bytes()
Get the address in bytes, in network byte order.


```c
ASIO_DECL bytes_type asio::ip::address_v4::to_bytes() const
```

!!! note "戻り値"
	ASIO_DECL



### to_uint()
Get the address as an unsigned integer in host byte order


```c
ASIO_DECL uint_type asio::ip::address_v4::to_uint() const
```

!!! note "戻り値"
	ASIO_DECL



### to_ulong()
Get the address as an unsigned long in host byte order


```c
ASIO_DECL unsigned long asio::ip::address_v4::to_ulong() const
```

!!! note "戻り値"
	ASIO_DECLunsigned long



### to_string()
Get the address as a string in dotted decimal format.


```c
ASIO_DECL std::string asio::ip::address_v4::to_string() const
```

!!! note "戻り値"
	ASIO_DECL



### to_string()


(Deprecated: Use other overload.) Get the address as a string in dotted decimal format. 
```c
ASIO_DECL std::string asio::ip::address_v4::to_string(asio::error_code &ec) const
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### is_loopback()
Determine whether the address is a loopback address.


```c
ASIO_DECL bool asio::ip::address_v4::is_loopback() const
```

!!! note "戻り値"
	ASIO_DECL



### is_unspecified()
Determine whether the address is unspecified.


```c
ASIO_DECL bool asio::ip::address_v4::is_unspecified() const
```

!!! note "戻り値"
	ASIO_DECL



### is_class_a()


(Deprecated: Use  class.) Determine whether the address is a class A address. 
```c
ASIO_DECL bool asio::ip::address_v4::is_class_a() const
```

!!! note "戻り値"
	ASIO_DECL



### is_class_b()


(Deprecated: Use  class.) Determine whether the address is a class B address. 
```c
ASIO_DECL bool asio::ip::address_v4::is_class_b() const
```

!!! note "戻り値"
	ASIO_DECL



### is_class_c()


(Deprecated: Use  class.) Determine whether the address is a class C address. 
```c
ASIO_DECL bool asio::ip::address_v4::is_class_c() const
```

!!! note "戻り値"
	ASIO_DECL



### is_multicast()
Determine whether the address is a multicast address.


```c
ASIO_DECL bool asio::ip::address_v4::is_multicast() const
```

!!! note "戻り値"
	ASIO_DECL



### from_string()


(Deprecated: Use .) Create an address from an IP address string in dotted decimal form. 
```c
address_v4 asio::ip::address_v4::from_string(const char *str)
```

!!! summary "引数"
	- constchar * `str` 

!!! note "戻り値"
	address_v4



### from_string()


(Deprecated: Use .) Create an address from an IP address string in dotted decimal form. 
```c
address_v4 asio::ip::address_v4::from_string(const char *str, asio::error_code &ec)
```

!!! summary "引数"
	- constchar * `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	address_v4



### from_string()


(Deprecated: Use .) Create an address from an IP address string in dotted decimal form. 
```c
address_v4 asio::ip::address_v4::from_string(const std::string &str)
```

!!! summary "引数"
	- const& `str` 

!!! note "戻り値"
	address_v4



### from_string()


(Deprecated: Use .) Create an address from an IP address string in dotted decimal form. 
```c
address_v4 asio::ip::address_v4::from_string(const std::string &str, asio::error_code &ec)
```

!!! summary "引数"
	- const& `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	address_v4



### any()
Obtain an address object that represents any address.


```c
static address_v4 asio::ip::address_v4::any()
```

!!! note "戻り値"
	address_v4



### loopback()
Obtain an address object that represents the loopback address.


```c
static address_v4 asio::ip::address_v4::loopback()
```

!!! note "戻り値"
	address_v4



### broadcast()
Obtain an address object that represents the broadcast address.


```c
static address_v4 asio::ip::address_v4::broadcast()
```

!!! note "戻り値"
	address_v4



### broadcast()


(Deprecated: Use  class.) Obtain an address object that represents the broadcast address that corresponds to the specified address and netmask. 
```c
static ASIO_DECL address_v4 asio::ip::address_v4::broadcast(const address_v4 &addr, const address_v4 &mask)
```

!!! summary "引数"
	- const& `addr` 
	- const& `mask` 

!!! note "戻り値"
	ASIO_DECL



### netmask()


(Deprecated: Use  class.) Obtain the netmask that corresponds to the address, based on its address class. 
```c
static ASIO_DECL address_v4 asio::ip::address_v4::netmask(const address_v4 &addr)
```

!!! summary "引数"
	- const& `addr` 

!!! note "戻り値"
	ASIO_DECL















### make_address_v4()
Create an IPv4 address from raw bytes in network order.


```c
address_v4 make_address_v4(const address_v4::bytes_type &bytes)
```

!!! summary "引数"
	- const& `bytes` 

!!! note "戻り値"
	address_v4



### make_address_v4()
Create an IPv4 address from an unsigned integer in host byte order.


```c
address_v4 make_address_v4(address_v4::uint_type addr)
```

!!! summary "引数"
	- address_v4::uint_type `addr` 

!!! note "戻り値"
	address_v4



### make_address_v4()
Create an IPv4 address from an IP address string in dotted decimal form.


```c
ASIO_DECL address_v4 make_address_v4(const char *str)
```

!!! summary "引数"
	- constchar * `str` 

!!! note "戻り値"
	ASIO_DECL



### make_address_v4()
Create an IPv4 address from an IP address string in dotted decimal form.


```c
ASIO_DECL address_v4 make_address_v4(const char *str, asio::error_code &ec)
```

!!! summary "引数"
	- constchar * `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### make_address_v4()
Create an IPv4 address from an IP address string in dotted decimal form.


```c
ASIO_DECL address_v4 make_address_v4(const std::string &str)
```

!!! summary "引数"
	- const& `str` 

!!! note "戻り値"
	ASIO_DECL



### make_address_v4()
Create an IPv4 address from an IP address string in dotted decimal form.


```c
ASIO_DECL address_v4 make_address_v4(const std::string &str, asio::error_code &ec)
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
std::basic_ostream< Elem, Traits > & operator<<(std::basic_ostream< Elem, Traits > &os, const address_v4 &addr)
```

!!! summary "引数"
	- std::basic_ostream< Elem, Traits > & `os` The output stream to which the string will be written.
	- const& `addr` The address to be written.

!!! note "戻り値"
	std::basic_ostream< Elem, Traits > &



### make_address_v4()
Create an IPv4 address from a IPv4-mapped IPv6 address.


```c
ASIO_DECL address_v4 make_address_v4(v4_mapped_t, const address_v6 &v6_addr)
```

!!! summary "引数"
	- v4_mapped_t `` 
	- const& `v6_addr` 

!!! note "戻り値"
	ASIO_DECL



### make_network_v4()
Create an IPv4 network from an address and prefix length.


```c
network_v4 make_network_v4(const address_v4 &addr, unsigned short prefix_len)
```

!!! summary "引数"
	- const& `addr` 
	- unsigned short `prefix_len` 

!!! note "戻り値"
	network_v4



### make_network_v4()
Create an IPv4 network from an address and netmask.


```c
network_v4 make_network_v4(const address_v4 &addr, const address_v4 &mask)
```

!!! summary "引数"
	- const& `addr` 
	- const& `mask` 

!!! note "戻り値"
	network_v4



### operator<<()
Output a network as a string.

Used to output a human-readable string for a specified network.
```c
std::basic_ostream< Elem, Traits > & operator<<(std::basic_ostream< Elem, Traits > &os, const network_v4 &net)
```

!!! summary "引数"
	- std::basic_ostream< Elem, Traits > & `os` The output stream to which the string will be written.
	- const& `net` The network to be written.

!!! note "戻り値"
	std::basic_ostream< Elem, Traits > &



