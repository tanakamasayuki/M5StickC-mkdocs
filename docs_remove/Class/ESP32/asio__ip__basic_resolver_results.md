# asio::ip::basic_resolver_results

A range of entries produced by a resolver. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1basic__resolver__results.html)

## メンバー



















### basic_resolver_results()
Default constructor creates an empty range.


```c
asio::ip::basic_resolver_results< InternetProtocol >::basic_resolver_results()
```



### basic_resolver_results()
Copy constructor.


```c
asio::ip::basic_resolver_results< InternetProtocol >::basic_resolver_results(const basic_resolver_results &other)
```

!!! summary "引数"
	- const& `other` 



### operator=()
Assignment operator.


```c
basic_resolver_results& asio::ip::basic_resolver_results< InternetProtocol >::operator=(const basic_resolver_results &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	basic_resolver_results&



### size()
Get the number of entries in the results range.


```c
size_type asio::ip::basic_resolver_results< InternetProtocol >::size() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	size_type



### max_size()
Get the maximum number of entries permitted in a results range.


```c
size_type asio::ip::basic_resolver_results< InternetProtocol >::max_size() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	size_type



### empty()
Determine whether the results range is empty.


```c
bool asio::ip::basic_resolver_results< InternetProtocol >::empty() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	bool



### begin()
Obtain a begin iterator for the results range.


```c
const_iterator asio::ip::basic_resolver_results< InternetProtocol >::begin() const
```

!!! note "戻り値"
	const_iterator



### end()
Obtain an end iterator for the results range.


```c
const_iterator asio::ip::basic_resolver_results< InternetProtocol >::end() const
```

!!! note "戻り値"
	const_iterator



### cbegin()
Obtain a begin iterator for the results range.


```c
const_iterator asio::ip::basic_resolver_results< InternetProtocol >::cbegin() const
```

!!! note "戻り値"
	const_iterator



### cend()
Obtain an end iterator for the results range.


```c
const_iterator asio::ip::basic_resolver_results< InternetProtocol >::cend() const
```

!!! note "戻り値"
	const_iterator



### swap()
Swap the results range with another.


```c
void asio::ip::basic_resolver_results< InternetProtocol >::swap(basic_resolver_results &that) ASIO_NOEXCEPT
```

!!! summary "引数"
	- basic_resolver_results& `that` 



### create()



```c
static basic_resolver_results asio::ip::basic_resolver_results< InternetProtocol >::create(asio::detail::addrinfo_type *address_info, const std::string &host_name, const std::string &service_name)
```

!!! summary "引数"
	- asio::detail::addrinfo_type* `address_info` 
	- const& `host_name` 
	- const& `service_name` 

!!! note "戻り値"
	basic_resolver_results



### create()



```c
static basic_resolver_results asio::ip::basic_resolver_results< InternetProtocol >::create(const endpoint_type &endpoint, const std::string &host_name, const std::string &service_name)
```

!!! summary "引数"
	- const& `endpoint` 
	- const& `host_name` 
	- const& `service_name` 

!!! note "戻り値"
	basic_resolver_results



### create()



```c
static basic_resolver_results asio::ip::basic_resolver_results< InternetProtocol >::create(EndpointIterator begin, EndpointIterator end, const std::string &host_name, const std::string &service_name)
```

!!! summary "引数"
	- EndpointIterator `begin` 
	- EndpointIterator `end` 
	- const& `host_name` 
	- const& `service_name` 

!!! note "戻り値"
	basic_resolver_results







