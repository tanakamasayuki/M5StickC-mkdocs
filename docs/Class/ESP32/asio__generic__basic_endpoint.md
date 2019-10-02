# asio::generic::basic_endpoint

Describes an endpoint for any socket type. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1generic_1_1basic__endpoint.html)

## メンバー





### basic_endpoint()
Default constructor.


```c
asio::generic::basic_endpoint< Protocol >::basic_endpoint()
```



### basic_endpoint()
Construct an endpoint from the specified socket address.


```c
asio::generic::basic_endpoint< Protocol >::basic_endpoint(const void *socket_address, std::size_t socket_address_size, int socket_protocol=0)
```

!!! summary "引数"
	- constvoid * `socket_address` 
	- std::size_t `socket_address_size` 
	- int `socket_protocol` 



### basic_endpoint()
Construct an endpoint from the specific endpoint type.


```c
asio::generic::basic_endpoint< Protocol >::basic_endpoint(const Endpoint &endpoint)
```

!!! summary "引数"
	- constEndpoint & `endpoint` 



### basic_endpoint()
Copy constructor.


```c
asio::generic::basic_endpoint< Protocol >::basic_endpoint(const basic_endpoint &other)
```

!!! summary "引数"
	- const& `other` 



### operator=()
Assign from another endpoint.


```c
basic_endpoint& asio::generic::basic_endpoint< Protocol >::operator=(const basic_endpoint &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	basic_endpoint&



### protocol()
The protocol associated with the endpoint.


```c
protocol_type asio::generic::basic_endpoint< Protocol >::protocol() const
```

!!! note "戻り値"
	protocol_type



### data()
Get the underlying endpoint in the native type.


```c
data_type* asio::generic::basic_endpoint< Protocol >::data()
```

!!! note "戻り値"
	data_type*



### data()
Get the underlying endpoint in the native type.


```c
const data_type* asio::generic::basic_endpoint< Protocol >::data() const
```

!!! note "戻り値"
	const*



### size()
Get the underlying size of the endpoint in the native type.


```c
std::size_t asio::generic::basic_endpoint< Protocol >::size() const
```

!!! note "戻り値"
	std::size_t



### resize()
Set the underlying size of the endpoint in the native type.


```c
void asio::generic::basic_endpoint< Protocol >::resize(std::size_t new_size)
```

!!! summary "引数"
	- std::size_t `new_size` 



### capacity()
Get the capacity of the endpoint in the native type.


```c
std::size_t asio::generic::basic_endpoint< Protocol >::capacity() const
```

!!! note "戻り値"
	std::size_t















