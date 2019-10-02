# asio::ip::basic_resolver_entry

An entry produced by a resolver. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1basic__resolver__entry.html)

## メンバー





### basic_resolver_entry()
Default constructor.


```c
asio::ip::basic_resolver_entry< InternetProtocol >::basic_resolver_entry()
```



### basic_resolver_entry()
Construct with specified endpoint, host name and service name.


```c
asio::ip::basic_resolver_entry< InternetProtocol >::basic_resolver_entry(const endpoint_type &ep, ASIO_STRING_VIEW_PARAM host, ASIO_STRING_VIEW_PARAM service)
```

!!! summary "引数"
	- const& `ep` 
	- ASIO_STRING_VIEW_PARAM `host` 
	- ASIO_STRING_VIEW_PARAM `service` 



### endpoint()
Get the endpoint associated with the entry.


```c
endpoint_type asio::ip::basic_resolver_entry< InternetProtocol >::endpoint() const
```

!!! note "戻り値"
	endpoint_type



### operator endpoint_type()
Convert to the endpoint associated with the entry.


```c
asio::ip::basic_resolver_entry< InternetProtocol >::operator endpoint_type() const
```



### host_name()
Get the host name associated with the entry.


```c
std::string asio::ip::basic_resolver_entry< InternetProtocol >::host_name() const
```

!!! note "戻り値"
	std::string



### host_name()
Get the host name associated with the entry.


```c
std::basic_string<char, std::char_traits<char>, Allocator> asio::ip::basic_resolver_entry< InternetProtocol >::host_name(const Allocator &alloc=Allocator()) const
```

!!! summary "引数"
	- constAllocator & `alloc` 

!!! note "戻り値"
	std::basic_string< char, std::char_traits< char >, Allocator >



### service_name()
Get the service name associated with the entry.


```c
std::string asio::ip::basic_resolver_entry< InternetProtocol >::service_name() const
```

!!! note "戻り値"
	std::string



### service_name()
Get the service name associated with the entry.


```c
std::basic_string<char, std::char_traits<char>, Allocator> asio::ip::basic_resolver_entry< InternetProtocol >::service_name(const Allocator &alloc=Allocator()) const
```

!!! summary "引数"
	- constAllocator & `alloc` 

!!! note "戻り値"
	std::basic_string< char, std::char_traits< char >, Allocator >



