# asio::ip::basic_resolver_query

An query to be passed to a resolver. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1basic__resolver__query.html)

## メンバー



### basic_resolver_query()
Construct with specified service name for any protocol.

This constructor is typically used to perform name resolution for local service binding.
```c
asio::ip::basic_resolver_query< InternetProtocol >::basic_resolver_query(const std::string &service, resolver_query_base::flags resolve_flags=passive|address_configured)
```

!!! summary "引数"
	- const& `service` A string identifying the requested service. This may be a descriptive name or a numeric string corresponding to a port number.
	- resolver_query_base::flags `resolve_flags` A set of flags that determine how name resolution should be performed. The default flags are suitable for local service binding.



### basic_resolver_query()
Construct with specified service name for a given protocol.

This constructor is typically used to perform name resolution for local service binding with a specific protocol version.
```c
asio::ip::basic_resolver_query< InternetProtocol >::basic_resolver_query(const protocol_type &protocol, const std::string &service, resolver_query_base::flags resolve_flags=passive|address_configured)
```

!!! summary "引数"
	- const& `protocol` A protocol object, normally representing either the IPv4 or IPv6 version of an internet protocol.
	- const& `service` A string identifying the requested service. This may be a descriptive name or a numeric string corresponding to a port number.
	- resolver_query_base::flags `resolve_flags` A set of flags that determine how name resolution should be performed. The default flags are suitable for local service binding.



### basic_resolver_query()
Construct with specified host name and service name for any protocol.

This constructor is typically used to perform name resolution for communication with remote hosts.
```c
asio::ip::basic_resolver_query< InternetProtocol >::basic_resolver_query(const std::string &host, const std::string &service, resolver_query_base::flags resolve_flags=address_configured)
```

!!! summary "引数"
	- const& `host` A string identifying a location. May be a descriptive name or a numeric address string. If an empty string and the passive flag has been specified, the resolved endpoints are suitable for local service binding. If an empty string and passive is not specified, the resolved endpoints will use the loopback address.
	- const& `service` A string identifying the requested service. This may be a descriptive name or a numeric string corresponding to a port number. May be an empty string, in which case all resolved endpoints will have a port number of 0.
	- resolver_query_base::flags `resolve_flags` A set of flags that determine how name resolution should be performed. The default flags are suitable for communication with remote hosts.



### basic_resolver_query()
Construct with specified host name and service name for a given protocol.

This constructor is typically used to perform name resolution for communication with remote hosts.
```c
asio::ip::basic_resolver_query< InternetProtocol >::basic_resolver_query(const protocol_type &protocol, const std::string &host, const std::string &service, resolver_query_base::flags resolve_flags=address_configured)
```

!!! summary "引数"
	- const& `protocol` A protocol object, normally representing either the IPv4 or IPv6 version of an internet protocol.
	- const& `host` A string identifying a location. May be a descriptive name or a numeric address string. If an empty string and the passive flag has been specified, the resolved endpoints are suitable for local service binding. If an empty string and passive is not specified, the resolved endpoints will use the loopback address.
	- const& `service` A string identifying the requested service. This may be a descriptive name or a numeric string corresponding to a port number. May be an empty string, in which case all resolved endpoints will have a port number of 0.
	- resolver_query_base::flags `resolve_flags` A set of flags that determine how name resolution should be performed. The default flags are suitable for communication with remote hosts.



### hints()
Get the hints associated with the query.


```c
const asio::detail::addrinfo_type& asio::ip::basic_resolver_query< InternetProtocol >::hints() const
```

!!! note "戻り値"
	const&



### host_name()
Get the host name associated with the query.


```c
std::string asio::ip::basic_resolver_query< InternetProtocol >::host_name() const
```

!!! note "戻り値"
	std::string



### service_name()
Get the service name associated with the query.


```c
std::string asio::ip::basic_resolver_query< InternetProtocol >::service_name() const
```

!!! note "戻り値"
	std::string



