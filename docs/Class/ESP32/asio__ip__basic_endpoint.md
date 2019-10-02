# asio::ip::basic_endpoint

Describes an endpoint for a version-independent IP socket. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1basic__endpoint.html)

## メンバー





### basic_endpoint()
Default constructor.


```c
asio::ip::basic_endpoint< InternetProtocol >::basic_endpoint()
```



### basic_endpoint()


Construct an endpoint using a port number, specified in the host's byte order. The IP address will be the any address (i.e. INADDR_ANY or in6addr_any). This constructor would typically be used for accepting new connections. 
To specify an IPv6  endpoint for port 9876, use:  
```c
asio::ip::basic_endpoint< InternetProtocol >::basic_endpoint(const InternetProtocol &internet_protocol, unsigned short port_num)
```

!!! summary "引数"
	- constInternetProtocol & `internet_protocol` 
	- unsigned short `port_num` 



### basic_endpoint()


Construct an endpoint using a port number and an IP address. This constructor may be used for accepting connections on a specific interface or for making a connection to a remote endpoint. 
```c
asio::ip::basic_endpoint< InternetProtocol >::basic_endpoint(const asio::ip::address &addr, unsigned short port_num)
```

!!! summary "引数"
	- const& `addr` 
	- unsigned short `port_num` 



### basic_endpoint()
Copy constructor.


```c
asio::ip::basic_endpoint< InternetProtocol >::basic_endpoint(const basic_endpoint &other)
```

!!! summary "引数"
	- const& `other` 



### operator=()
Assign from another endpoint.


```c
basic_endpoint& asio::ip::basic_endpoint< InternetProtocol >::operator=(const basic_endpoint &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	basic_endpoint&



### protocol()
The protocol associated with the endpoint.


```c
protocol_type asio::ip::basic_endpoint< InternetProtocol >::protocol() const
```

!!! note "戻り値"
	protocol_type



### data()
Get the underlying endpoint in the native type.


```c
data_type* asio::ip::basic_endpoint< InternetProtocol >::data()
```

!!! note "戻り値"
	data_type*



### data()
Get the underlying endpoint in the native type.


```c
const data_type* asio::ip::basic_endpoint< InternetProtocol >::data() const
```

!!! note "戻り値"
	const*



### size()
Get the underlying size of the endpoint in the native type.


```c
std::size_t asio::ip::basic_endpoint< InternetProtocol >::size() const
```

!!! note "戻り値"
	std::size_t



### resize()
Set the underlying size of the endpoint in the native type.


```c
void asio::ip::basic_endpoint< InternetProtocol >::resize(std::size_t new_size)
```

!!! summary "引数"
	- std::size_t `new_size` 



### capacity()
Get the capacity of the endpoint in the native type.


```c
std::size_t asio::ip::basic_endpoint< InternetProtocol >::capacity() const
```

!!! note "戻り値"
	std::size_t



### port()


Get the port associated with the endpoint. The port number is always in the host's byte order. 
```c
unsigned short asio::ip::basic_endpoint< InternetProtocol >::port() const
```

!!! note "戻り値"
	unsigned short



### port()


Set the port associated with the endpoint. The port number is always in the host's byte order. 
```c
void asio::ip::basic_endpoint< InternetProtocol >::port(unsigned short port_num)
```

!!! summary "引数"
	- unsigned short `port_num` 



### address()
Get the IP address associated with the endpoint.


```c
asio::ip::address asio::ip::basic_endpoint< InternetProtocol >::address() const
```

!!! note "戻り値"
	asio::ip::address



### address()
Set the IP address associated with the endpoint.


```c
void asio::ip::basic_endpoint< InternetProtocol >::address(const asio::ip::address &addr)
```

!!! summary "引数"
	- const& `addr` 















### operator<<()
Output an endpoint as a string.

Used to output a human-readable string for a specified endpoint.
```c
std::basic_ostream< Elem, Traits > & operator<<(std::basic_ostream< Elem, Traits > &os, const basic_endpoint< InternetProtocol > &endpoint)
```

!!! summary "引数"
	- std::basic_ostream< Elem, Traits > & `os` The output stream to which the string will be written.
	- const< InternetProtocol > & `endpoint` The endpoint to be written.

!!! note "戻り値"
	std::basic_ostream< Elem, Traits > &



