# asio::ip::detail::endpoint



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1detail_1_1endpoint.html)

## メンバー

### endpoint()



```c
ASIO_DECL asio::ip::detail::endpoint::endpoint()
```

!!! note "戻り値"
	ASIO_DECL



### endpoint()



```c
ASIO_DECL asio::ip::detail::endpoint::endpoint(int family, unsigned short port_num)
```

!!! summary "引数"
	- int `family` 
	- unsigned short `port_num` 

!!! note "戻り値"
	ASIO_DECL



### endpoint()



```c
ASIO_DECL asio::ip::detail::endpoint::endpoint(const asio::ip::address &addr, unsigned short port_num)
```

!!! summary "引数"
	- const& `addr` 
	- unsigned short `port_num` 

!!! note "戻り値"
	ASIO_DECL



### endpoint()



```c
asio::ip::detail::endpoint::endpoint(const endpoint &other)
```

!!! summary "引数"
	- const& `other` 



### operator=()



```c
endpoint& asio::ip::detail::endpoint::operator=(const endpoint &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	endpoint&



### data()



```c
asio::detail::socket_addr_type* asio::ip::detail::endpoint::data()
```

!!! note "戻り値"
	asio::detail::socket_addr_type*



### data()



```c
const asio::detail::socket_addr_type* asio::ip::detail::endpoint::data() const
```

!!! note "戻り値"
	const*



### size()



```c
std::size_t asio::ip::detail::endpoint::size() const
```

!!! note "戻り値"
	std::size_t



### resize()



```c
ASIO_DECL void asio::ip::detail::endpoint::resize(std::size_t new_size)
```

!!! summary "引数"
	- std::size_t `new_size` 

!!! note "戻り値"
	ASIO_DECLvoid



### capacity()



```c
std::size_t asio::ip::detail::endpoint::capacity() const
```

!!! note "戻り値"
	std::size_t



### port()



```c
ASIO_DECL unsigned short asio::ip::detail::endpoint::port() const
```

!!! note "戻り値"
	ASIO_DECLunsigned short



### port()



```c
ASIO_DECL void asio::ip::detail::endpoint::port(unsigned short port_num)
```

!!! summary "引数"
	- unsigned short `port_num` 

!!! note "戻り値"
	ASIO_DECLvoid



### address()



```c
ASIO_DECL asio::ip::address asio::ip::detail::endpoint::address() const
```

!!! note "戻り値"
	ASIO_DECL



### address()



```c
ASIO_DECL void asio::ip::detail::endpoint::address(const asio::ip::address &addr)
```

!!! summary "引数"
	- const& `addr` 

!!! note "戻り値"
	ASIO_DECLvoid



### is_v4()



```c
bool asio::ip::detail::endpoint::is_v4() const
```

!!! note "戻り値"
	bool



### to_string()



```c
ASIO_DECL std::string asio::ip::detail::endpoint::to_string() const
```

!!! note "戻り値"
	ASIO_DECL







