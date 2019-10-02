# asio::generic::detail::endpoint



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1generic_1_1detail_1_1endpoint.html)

## メンバー

### endpoint()



```c
ASIO_DECL asio::generic::detail::endpoint::endpoint()
```

!!! note "戻り値"
	ASIO_DECL



### endpoint()



```c
ASIO_DECL asio::generic::detail::endpoint::endpoint(const void *sock_addr, std::size_t sock_addr_size, int sock_protocol)
```

!!! summary "引数"
	- constvoid * `sock_addr` 
	- std::size_t `sock_addr_size` 
	- int `sock_protocol` 

!!! note "戻り値"
	ASIO_DECL



### endpoint()



```c
asio::generic::detail::endpoint::endpoint(const endpoint &other)
```

!!! summary "引数"
	- const& `other` 



### operator=()



```c
endpoint& asio::generic::detail::endpoint::operator=(const endpoint &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	endpoint&



### family()



```c
int asio::generic::detail::endpoint::family() const
```

!!! note "戻り値"
	int



### protocol()



```c
int asio::generic::detail::endpoint::protocol() const
```

!!! note "戻り値"
	int



### data()



```c
asio::detail::socket_addr_type* asio::generic::detail::endpoint::data()
```

!!! note "戻り値"
	asio::detail::socket_addr_type*



### data()



```c
const asio::detail::socket_addr_type* asio::generic::detail::endpoint::data() const
```

!!! note "戻り値"
	const*



### size()



```c
std::size_t asio::generic::detail::endpoint::size() const
```

!!! note "戻り値"
	std::size_t



### resize()



```c
ASIO_DECL void asio::generic::detail::endpoint::resize(std::size_t size)
```

!!! summary "引数"
	- std::size_t `size` 

!!! note "戻り値"
	ASIO_DECLvoid



### capacity()



```c
std::size_t asio::generic::detail::endpoint::capacity() const
```

!!! note "戻り値"
	std::size_t







