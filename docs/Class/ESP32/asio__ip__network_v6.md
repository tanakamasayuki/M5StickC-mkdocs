# asio::ip::network_v6

Represents an IPv6 network. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1network__v6.html)

## メンバー

### network_v6()
Default constructor.


```c
asio::ip::network_v6::network_v6() ASIO_NOEXCEPT
```



### network_v6()
Construct a network based on the specified address and prefix length.


```c
ASIO_DECL asio::ip::network_v6::network_v6(const address_v6 &addr, unsigned short prefix_len)
```

!!! summary "引数"
	- const& `addr` 
	- unsigned short `prefix_len` 

!!! note "戻り値"
	ASIO_DECL



### network_v6()
Copy constructor.


```c
asio::ip::network_v6::network_v6(const network_v6 &other) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `other` 



### operator=()
Assign from another network.


```c
network_v6& asio::ip::network_v6::operator=(const network_v6 &other) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	network_v6&



### address()
Obtain the address object specified when the network object was created.


```c
address_v6 asio::ip::network_v6::address() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	address_v6



### prefix_length()


Obtain the prefix length that was specified when the network object was created. 
```c
unsigned short asio::ip::network_v6::prefix_length() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	unsigned short



### network()
Obtain an address object that represents the network address.


```c
ASIO_DECL address_v6 asio::ip::network_v6::network() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	ASIO_DECL



### hosts()
Obtain an address range corresponding to the hosts in the network.


```c
ASIO_DECL address_v6_range asio::ip::network_v6::hosts() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	ASIO_DECL



### canonical()
Obtain the true network address, omitting any host bits.


```c
network_v6 asio::ip::network_v6::canonical() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	network_v6



### is_host()
Test if network is a valid host address.


```c
bool asio::ip::network_v6::is_host() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	bool



### is_subnet_of()
Test if a network is a real subnet of another network.


```c
ASIO_DECL bool asio::ip::network_v6::is_subnet_of(const network_v6 &other) const
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	ASIO_DECL



### to_string()
Get the network as an address in dotted decimal format.


```c
ASIO_DECL std::string asio::ip::network_v6::to_string() const
```

!!! note "戻り値"
	ASIO_DECL



### to_string()
Get the network as an address in dotted decimal format.


```c
ASIO_DECL std::string asio::ip::network_v6::to_string(asio::error_code &ec) const
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL







### make_network_v6()


Create an IPv6 network from a string containing IP address and prefix length. 
```c
ASIO_DECL network_v6 make_network_v6(const char *str)
```

!!! summary "引数"
	- constchar * `str` 

!!! note "戻り値"
	ASIO_DECL



### make_network_v6()


Create an IPv6 network from a string containing IP address and prefix length. 
```c
ASIO_DECL network_v6 make_network_v6(const char *str, asio::error_code &ec)
```

!!! summary "引数"
	- constchar * `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### make_network_v6()


Create an IPv6 network from a string containing IP address and prefix length. 
```c
ASIO_DECL network_v6 make_network_v6(const std::string &str)
```

!!! summary "引数"
	- const& `str` 

!!! note "戻り値"
	ASIO_DECL



### make_network_v6()


Create an IPv6 network from a string containing IP address and prefix length. 
```c
ASIO_DECL network_v6 make_network_v6(const std::string &str, asio::error_code &ec)
```

!!! summary "引数"
	- const& `str` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



