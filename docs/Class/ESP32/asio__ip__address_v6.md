# asio::ip::address_v6

Implements IP version 6 style addresses. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1address__v6.html)

## メンバー















### address_v6()
Default constructor.


```c
ASIO_DECL asio::ip::address_v6::address_v6()
```

!!! note "戻り値"
	ASIO_DECL



### address_v6()
Construct an address from raw bytes and scope ID.


```c
ASIO_DECL asio::ip::address_v6::address_v6(const bytes_type &bytes, unsigned long scope_id=0)
```

!!! summary "引数"
	- const& `bytes` 
	- unsigned long `scope_id` 

!!! note "戻り値"
	ASIO_DECL



### address_v6()
Copy constructor.


```c
ASIO_DECL asio::ip::address_v6::address_v6(const address_v6 &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	ASIO_DECL



### operator=()
Assign from another address.


```c
ASIO_DECL address_v6& asio::ip::address_v6::operator=(const address_v6 &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	ASIO_DECL&



### scope_id()
The scope ID of the address.

Returns the scope ID associated with the IPv6 address. 
```c
unsigned long asio::ip::address_v6::scope_id() const
```

!!! note "戻り値"
	unsigned long



### scope_id()
The scope ID of the address.

Modifies the scope ID associated with the IPv6 address. 
```c
void asio::ip::address_v6::scope_id(unsigned long id)
```

!!! summary "引数"
	- unsigned long `id` 



### to_bytes()
Get the address in bytes, in network byte order.


```c
ASIO_DECL bytes_type asio::ip::address_v6::to_bytes() const
```

!!! note "戻り値"
	ASIO_DECL



### to_string()
Get the address as a string.


```c
ASIO_DECL std::string asio::ip::address_v6::to_string() const
```

!!! note "戻り値"
	ASIO_DECL



### to_string()
(Deprecated: Use other overload.) Get the address as a string.


```c
ASIO_DECL std::string asio::ip::address_v6::to_string(asio::error_code &ec) const
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### to_v4()


(Deprecated: Use .) Converts an IPv4-mapped or IPv4-compatible address to an IPv4 address. 
```c
ASIO_DECL address_v4 asio::ip::address_v6::to_v4() const
```

!!! note "戻り値"
	ASIO_DECL



### is_loopback()
Determine whether the address is a loopback address.


```c
ASIO_DECL bool asio::ip::address_v6::is_loopback() const
```

!!! note "戻り値"
	ASIO_DECL



### is_unspecified()
Determine whether the address is unspecified.


```c
ASIO_DECL bool asio::ip::address_v6::is_unspecified() const
```

!!! note "戻り値"
	ASIO_DECL



### is_link_local()
Determine whether the address is link local.


```c
ASIO_DECL bool asio::ip::address_v6::is_link_local() const
```

!!! note "戻り値"
	ASIO_DECL



### is_site_local()
Determine whether the address is site local.


```c
ASIO_DECL bool asio::ip::address_v6::is_site_local() const
```

!!! note "戻り値"
	ASIO_DECL



### is_v4_mapped()
Determine whether the address is a mapped IPv4 address.


```c
ASIO_DECL bool asio::ip::address_v6::is_v4_mapped() const
```

!!! note "戻り値"
	ASIO_DECL



### is_v4_compatible()


(Deprecated: No replacement.) Determine whether the address is an IPv4-compatible address. 
```c
ASIO_DECL bool asio::ip::address_v6::is_v4_compatible() const
```

!!! note "戻り値"
	ASIO_DECL



### is_multicast()
Determine whether the address is a multicast address.


```c
ASIO_DECL bool asio::ip::address_v6::is_multicast() const
```

!!! note "戻り値"
	ASIO_DECL



### is_multicast_global()
Determine whether the address is a global multicast address.


```c
ASIO_DECL bool asio::ip::address_v6::is_multicast_global() const
```

!!! note "戻り値"
	ASIO_DECL



### is_multicast_link_local()
Determine whether the address is a link-local multicast address.


```c
ASIO_DECL bool asio::ip::address_v6::is_multicast_link_local() const
```

!!! note "戻り値"
	ASIO_DECL



### is_multicast_node_local()
Determine whether the address is a node-local multicast address.


```c
ASIO_DECL bool asio::ip::address_v6::is_multicast_node_local() const
```

!!! note "戻り値"
	ASIO_DECL



### is_multicast_org_local()
Determine whether the address is a org-local multicast address.


```c
ASIO_DECL bool asio::ip::address_v6::is_multicast_org_local() const
```

!!! note "戻り値"
	ASIO_DECL



### is_multicast_site_local()
Determine whether the address is a site-local multicast address.


```c
ASIO_DECL bool asio::ip::address_v6::is_multicast_site_local() const
```

!!! note "戻り値"
	ASIO_DECL



### from_string()


(Deprecated: Use .) Create an IPv6 address from an IP address string. 
```c
address_v6 asio::ip::address_v6::from_string(const char *str)
```

!!! summary "引数"
	- constchar * `str` 

!!! note "戻り値"
	address_v6



### from_string()


(Deprecated: Use .) Create an IPv6 address from an IP address string. 
```c
address_v6 asio::ip::address_v6::from_string(const char *str, asio::error_code &ec)
```

!!! summary "引数"
	- constchar * `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	address_v6



### from_string()


(Deprecated: Use .) Create an IPv6 address from an IP address string. 
```c
address_v6 asio::ip::address_v6::from_string(const std::string &str)
```

!!! summary "引数"
	- const& `str` 

!!! note "戻り値"
	address_v6



### from_string()


(Deprecated: Use .) Create an IPv6 address from an IP address string. 
```c
address_v6 asio::ip::address_v6::from_string(const std::string &str, asio::error_code &ec)
```

!!! summary "引数"
	- const& `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	address_v6



### any()
Obtain an address object that represents any address.


```c
static address_v6 asio::ip::address_v6::any()
```

!!! note "戻り値"
	address_v6



### loopback()
Obtain an address object that represents the loopback address.


```c
static ASIO_DECL address_v6 asio::ip::address_v6::loopback()
```

!!! note "戻り値"
	ASIO_DECL



### v4_mapped()
(Deprecated: Use .) Create an IPv4-mapped IPv6 address.


```c
static ASIO_DECL address_v6 asio::ip::address_v6::v4_mapped(const address_v4 &addr)
```

!!! summary "引数"
	- const& `addr` 

!!! note "戻り値"
	ASIO_DECL



### v4_compatible()
(Deprecated: No replacement.) Create an IPv4-compatible IPv6 address.


```c
static ASIO_DECL address_v6 asio::ip::address_v6::v4_compatible(const address_v4 &addr)
```

!!! summary "引数"
	- const& `addr` 

!!! note "戻り値"
	ASIO_DECL



### make_address_v6()
Create an IPv6 address from raw bytes and scope ID.


```c
address_v6 make_address_v6(const address_v6::bytes_type &bytes, unsigned long scope_id=0)
```

!!! summary "引数"
	- const& `bytes` 
	- unsigned long `scope_id` 

!!! note "戻り値"
	address_v6



### make_address_v6()
Create an IPv6 address from an IP address string.


```c
ASIO_DECL address_v6 make_address_v6(const char *str)
```

!!! summary "引数"
	- constchar * `str` 

!!! note "戻り値"
	ASIO_DECL



### make_address_v6()
Create an IPv6 address from an IP address string.


```c
ASIO_DECL address_v6 make_address_v6(const char *str, asio::error_code &ec)
```

!!! summary "引数"
	- constchar * `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### make_address_v6()
Createan IPv6 address from an IP address string.


```c
ASIO_DECL address_v6 make_address_v6(const std::string &str)
```

!!! summary "引数"
	- const& `str` 

!!! note "戻り値"
	ASIO_DECL



### make_address_v6()
Create an IPv6 address from an IP address string.


```c
ASIO_DECL address_v6 make_address_v6(const std::string &str, asio::error_code &ec)
```

!!! summary "引数"
	- const& `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### make_address_v6()
Create an IPv4-mapped IPv6 address from an IPv4 address.


```c
ASIO_DECL address_v6 make_address_v6(v4_mapped_t, const address_v4 &v4_addr)
```

!!! summary "引数"
	- v4_mapped_t `` 
	- const& `v4_addr` 

!!! note "戻り値"
	ASIO_DECL



### operator<<()
Output an address as a string.

Used to output a human-readable string for a specified address.
```c
std::basic_ostream< Elem, Traits > & operator<<(std::basic_ostream< Elem, Traits > &os, const address_v6 &addr)
```

!!! summary "引数"
	- std::basic_ostream< Elem, Traits > & `os` The output stream to which the string will be written.
	- const& `addr` The address to be written.

!!! note "戻り値"
	std::basic_ostream< Elem, Traits > &



### make_network_v6()
Create an IPv6 network from an address and prefix length.


```c
network_v6 make_network_v6(const address_v6 &addr, unsigned short prefix_len)
```

!!! summary "引数"
	- const& `addr` 
	- unsigned short `prefix_len` 

!!! note "戻り値"
	network_v6



### operator<<()
Output a network as a string.

Used to output a human-readable string for a specified network.
```c
std::basic_ostream< Elem, Traits > & operator<<(std::basic_ostream< Elem, Traits > &os, const network_v6 &net)
```

!!! summary "引数"
	- std::basic_ostream< Elem, Traits > & `os` The output stream to which the string will be written.
	- const& `net` The network to be written.

!!! note "戻り値"
	std::basic_ostream< Elem, Traits > &



