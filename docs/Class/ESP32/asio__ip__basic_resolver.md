# asio::ip::basic_resolver

Provides endpoint resolution functionality. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1basic__resolver.html)

## メンバー













###  service

```c
ASIO_STRING_VIEW_PARAM ASIO_STRING_VIEW_PARAM asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::service
```


###  resolve_flags

```c
ASIO_STRING_VIEW_PARAM resolver_base::flags asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve_flags
```


###  host

```c
ASIO_STRING_VIEW_PARAM asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::host
```


###  service

```c
ASIO_STRING_VIEW_PARAM ASIO_STRING_VIEW_PARAM asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::service
```


###  resolve_flags

```c
ASIO_STRING_VIEW_PARAM ASIO_STRING_VIEW_PARAM resolver_base::flags asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve_flags
```


### basic_resolver()
Constructor.

This constructor creates a .
```c
asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::basic_resolver(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### ~basic_resolver()
Destroys the resolver.

This function destroys the resolver, cancelling any outstanding asynchronous wait operations associated with the resolver as if by calling . 
```c
asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::~basic_resolver()
```



### get_io_context()




```c
asio::io_context& asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::get_io_context()
```

!!! note "戻り値"
	asio::io_context&



### get_io_service()




```c
asio::io_context& asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::get_io_service()
```

!!! note "戻り値"
	asio::io_context&



### get_executor()
Get the executor associated with the object.


```c
executor_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::get_executor() ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



### cancel()
Cancel any asynchronous operations that are waiting on the resolver.

This function forces the completion of any pending asynchronous operations on the host resolver. The handler for each cancelled operation will be invoked with the  error code. 
```c
void asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::cancel()
```



### resolve()
(Deprecated.) Perform forward resolution of a query to a list of entries.

This function is used to resolve a query into a list of endpoint entries.
```c
results_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve(const query &q)
```

!!! summary "引数"
	- const& `q` A query object that determines what endpoints will be returned.

!!! note "戻り値"
	results_type



### resolve()
(Deprecated.) Perform forward resolution of a query to a list of entries.

This function is used to resolve a query into a list of endpoint entries.
```c
results_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve(const query &q, asio::error_code &ec)
```

!!! summary "引数"
	- const& `q` A query object that determines what endpoints will be returned.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	results_type



### resolve()
Perform forward resolution of a query to a list of entries.

This function is used to resolve host and service names into a list of endpoint entries.
```c
results_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve(ASIO_STRING_VIEW_PARAM host, ASIO_STRING_VIEW_PARAM service)
```

!!! summary "引数"
	- ASIO_STRING_VIEW_PARAM `host` A string identifying a location. May be a descriptive name or a numeric address string. If an empty string and the passive flag has been specified, the resolved endpoints are suitable for local service binding. If an empty string and passive is not specified, the resolved endpoints will use the loopback address.
	- ASIO_STRING_VIEW_PARAM `service` A string identifying the requested service. This may be a descriptive name or a numeric string corresponding to a port number. May be an empty string, in which case all resolved endpoints will have a port number of 0.

!!! note "戻り値"
	results_type



### resolve()
Perform forward resolution of a query to a list of entries.

This function is used to resolve host and service names into a list of endpoint entries.
```c
results_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve(ASIO_STRING_VIEW_PARAM host, ASIO_STRING_VIEW_PARAM service, asio::error_code &ec)
```

!!! summary "引数"
	- ASIO_STRING_VIEW_PARAM `host` A string identifying a location. May be a descriptive name or a numeric address string. If an empty string and the passive flag has been specified, the resolved endpoints are suitable for local service binding. If an empty string and passive is not specified, the resolved endpoints will use the loopback address.
	- ASIO_STRING_VIEW_PARAM `service` A string identifying the requested service. This may be a descriptive name or a numeric string corresponding to a port number. May be an empty string, in which case all resolved endpoints will have a port number of 0.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	results_type



### resolve()
Perform forward resolution of a query to a list of entries.

This function is used to resolve host and service names into a list of endpoint entries.
```c
results_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve(ASIO_STRING_VIEW_PARAM host, ASIO_STRING_VIEW_PARAM service, resolver_base::flags resolve_flags)
```

!!! summary "引数"
	- ASIO_STRING_VIEW_PARAM `host` A string identifying a location. May be a descriptive name or a numeric address string. If an empty string and the passive flag has been specified, the resolved endpoints are suitable for local service binding. If an empty string and passive is not specified, the resolved endpoints will use the loopback address.
	- ASIO_STRING_VIEW_PARAM `service` A string identifying the requested service. This may be a descriptive name or a numeric string corresponding to a port number. May be an empty string, in which case all resolved endpoints will have a port number of 0.
	- resolver_base::flags `resolve_flags` A set of flags that determine how name resolution should be performed. The default flags are suitable for communication with remote hosts.

!!! note "戻り値"
	results_type



### resolve()
Perform forward resolution of a query to a list of entries.

This function is used to resolve host and service names into a list of endpoint entries.
```c
results_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve(ASIO_STRING_VIEW_PARAM host, ASIO_STRING_VIEW_PARAM service, resolver_base::flags resolve_flags, asio::error_code &ec)
```

!!! summary "引数"
	- ASIO_STRING_VIEW_PARAM `host` A string identifying a location. May be a descriptive name or a numeric address string. If an empty string and the passive flag has been specified, the resolved endpoints are suitable for local service binding. If an empty string and passive is not specified, the resolved endpoints will use the loopback address.
	- ASIO_STRING_VIEW_PARAM `service` A string identifying the requested service. This may be a descriptive name or a numeric string corresponding to a port number. May be an empty string, in which case all resolved endpoints will have a port number of 0.
	- resolver_base::flags `resolve_flags` A set of flags that determine how name resolution should be performed. The default flags are suitable for communication with remote hosts.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	results_type



### resolve()
Perform forward resolution of a query to a list of entries.

This function is used to resolve host and service names into a list of endpoint entries.
```c
results_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve(const protocol_type &protocol, ASIO_STRING_VIEW_PARAM host, ASIO_STRING_VIEW_PARAM service)
```

!!! summary "引数"
	- const& `protocol` A protocol object, normally representing either the IPv4 or IPv6 version of an internet protocol.
	- ASIO_STRING_VIEW_PARAM `host` A string identifying a location. May be a descriptive name or a numeric address string. If an empty string and the passive flag has been specified, the resolved endpoints are suitable for local service binding. If an empty string and passive is not specified, the resolved endpoints will use the loopback address.
	- ASIO_STRING_VIEW_PARAM `service` A string identifying the requested service. This may be a descriptive name or a numeric string corresponding to a port number. May be an empty string, in which case all resolved endpoints will have a port number of 0.

!!! note "戻り値"
	results_type



### resolve()
Perform forward resolution of a query to a list of entries.

This function is used to resolve host and service names into a list of endpoint entries.
```c
results_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve(const protocol_type &protocol, ASIO_STRING_VIEW_PARAM host, ASIO_STRING_VIEW_PARAM service, asio::error_code &ec)
```

!!! summary "引数"
	- const& `protocol` A protocol object, normally representing either the IPv4 or IPv6 version of an internet protocol.
	- ASIO_STRING_VIEW_PARAM `host` A string identifying a location. May be a descriptive name or a numeric address string. If an empty string and the passive flag has been specified, the resolved endpoints are suitable for local service binding. If an empty string and passive is not specified, the resolved endpoints will use the loopback address.
	- ASIO_STRING_VIEW_PARAM `service` A string identifying the requested service. This may be a descriptive name or a numeric string corresponding to a port number. May be an empty string, in which case all resolved endpoints will have a port number of 0.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	results_type



### resolve()
Perform forward resolution of a query to a list of entries.

This function is used to resolve host and service names into a list of endpoint entries.
```c
results_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve(const protocol_type &protocol, ASIO_STRING_VIEW_PARAM host, ASIO_STRING_VIEW_PARAM service, resolver_base::flags resolve_flags)
```

!!! summary "引数"
	- const& `protocol` A protocol object, normally representing either the IPv4 or IPv6 version of an internet protocol.
	- ASIO_STRING_VIEW_PARAM `host` A string identifying a location. May be a descriptive name or a numeric address string. If an empty string and the passive flag has been specified, the resolved endpoints are suitable for local service binding. If an empty string and passive is not specified, the resolved endpoints will use the loopback address.
	- ASIO_STRING_VIEW_PARAM `service` A string identifying the requested service. This may be a descriptive name or a numeric string corresponding to a port number. May be an empty string, in which case all resolved endpoints will have a port number of 0.
	- resolver_base::flags `resolve_flags` A set of flags that determine how name resolution should be performed. The default flags are suitable for communication with remote hosts.

!!! note "戻り値"
	results_type



### resolve()
Perform forward resolution of a query to a list of entries.

This function is used to resolve host and service names into a list of endpoint entries.
```c
results_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve(const protocol_type &protocol, ASIO_STRING_VIEW_PARAM host, ASIO_STRING_VIEW_PARAM service, resolver_base::flags resolve_flags, asio::error_code &ec)
```

!!! summary "引数"
	- const& `protocol` A protocol object, normally representing either the IPv4 or IPv6 version of an internet protocol.
	- ASIO_STRING_VIEW_PARAM `host` A string identifying a location. May be a descriptive name or a numeric address string. If an empty string and the passive flag has been specified, the resolved endpoints are suitable for local service binding. If an empty string and passive is not specified, the resolved endpoints will use the loopback address.
	- ASIO_STRING_VIEW_PARAM `service` A string identifying the requested service. This may be a descriptive name or a numeric string corresponding to a port number. May be an empty string, in which case all resolved endpoints will have a port number of 0.
	- resolver_base::flags `resolve_flags` A set of flags that determine how name resolution should be performed. The default flags are suitable for communication with remote hosts.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	results_type



### ASIO_INITFN_RESULT_TYPE()


(Deprecated.) Asynchronously perform forward resolution of a query to a list of entries. This function is used to asynchronously resolve a query into a list of endpoint entries.
```c
asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ResolveHandler, void(asio::error_code, results_type)) async_resolve(const query &q
```

!!! summary "引数"
	- asio::error_codevoid(, ) `` 



### ASIO_MOVE_ARG()



```c
asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ResolveHandler) handler)
```

!!! summary "引数"
	- ResolveHandler `` 



### ASIO_INITFN_RESULT_TYPE()
Asynchronously perform forward resolution of a query to a list of entries.


On POSIX systems, service names are typically defined in the file . On Windows, service names may be found in the file . Operating systems may use additional locations when resolving service names. 
```c
asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ResolveHandler, void(asio::error_code, results_type)) async_resolve(ASIO_STRING_VIEW_PARAM host
```

!!! summary "引数"
	- asio::error_codevoid(, ) `` 



### ASIO_MOVE_ARG()



```c
ASIO_STRING_VIEW_PARAM asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ResolveHandler) handler)
```

!!! summary "引数"
	- ResolveHandler `` 

!!! note "戻り値"
	ASIO_STRING_VIEW_PARAM



### ASIO_INITFN_RESULT_TYPE()
Asynchronously perform forward resolution of a query to a list of entries.


On POSIX systems, service names are typically defined in the file . On Windows, service names may be found in the file . Operating systems may use additional locations when resolving service names. 
```c
asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ResolveHandler, void(asio::error_code, results_type)) async_resolve(ASIO_STRING_VIEW_PARAM host
```

!!! summary "引数"
	- asio::error_codevoid(, ) `` 



### ASIO_MOVE_ARG()



```c
ASIO_STRING_VIEW_PARAM resolver_base::flags asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ResolveHandler) handler)
```

!!! summary "引数"
	- ResolveHandler `` 

!!! note "戻り値"
	ASIO_STRING_VIEW_PARAM



### ASIO_INITFN_RESULT_TYPE()
Asynchronously perform forward resolution of a query to a list of entries.


On POSIX systems, service names are typically defined in the file . On Windows, service names may be found in the file . Operating systems may use additional locations when resolving service names. 
```c
asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ResolveHandler, void(asio::error_code, results_type)) async_resolve(const protocol_type &protocol
```

!!! summary "引数"
	- asio::error_codevoid(, ) `` 



### ASIO_MOVE_ARG()



```c
ASIO_STRING_VIEW_PARAM ASIO_STRING_VIEW_PARAM asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ResolveHandler) handler)
```

!!! summary "引数"
	- ResolveHandler `` 

!!! note "戻り値"
	ASIO_STRING_VIEW_PARAM



### ASIO_INITFN_RESULT_TYPE()
Asynchronously perform forward resolution of a query to a list of entries.


On POSIX systems, service names are typically defined in the file . On Windows, service names may be found in the file . Operating systems may use additional locations when resolving service names. 
```c
asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ResolveHandler, void(asio::error_code, results_type)) async_resolve(const protocol_type &protocol
```

!!! summary "引数"
	- asio::error_codevoid(, ) `` 



### ASIO_MOVE_ARG()



```c
ASIO_STRING_VIEW_PARAM ASIO_STRING_VIEW_PARAM resolver_base::flags asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ResolveHandler) handler)
```

!!! summary "引数"
	- ResolveHandler `` 

!!! note "戻り値"
	ASIO_STRING_VIEW_PARAM



### resolve()
Perform reverse resolution of an endpoint to a list of entries.

This function is used to resolve an endpoint into a list of endpoint entries.
```c
results_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve(const endpoint_type &e)
```

!!! summary "引数"
	- const& `e` An endpoint object that determines what endpoints will be returned.

!!! note "戻り値"
	results_type



### resolve()
Perform reverse resolution of an endpoint to a list of entries.

This function is used to resolve an endpoint into a list of endpoint entries.
```c
results_type asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::resolve(const endpoint_type &e, asio::error_code &ec)
```

!!! summary "引数"
	- const& `e` An endpoint object that determines what endpoints will be returned.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	results_type



### ASIO_INITFN_RESULT_TYPE()


Asynchronously perform reverse resolution of an endpoint to a list of entries. This function is used to asynchronously resolve an endpoint into a list of endpoint entries.
```c
asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ResolveHandler, void(asio::error_code, results_type)) async_resolve(const endpoint_type &e
```

!!! summary "引数"
	- asio::error_codevoid(, ) `` 



### ASIO_MOVE_ARG()



```c
asio::ip::basic_resolver< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ResolveHandler) handler)
```

!!! summary "引数"
	- ResolveHandler `` 



