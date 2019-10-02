# asio::detail::resolver_service



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1resolver__service.html)

## メンバー









### resolver_service()



```c
asio::detail::resolver_service< Protocol >::resolver_service(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### shutdown()
Destroy all user-defined handler objects owned by the service.


```c
void asio::detail::resolver_service< Protocol >::shutdown()
```



### notify_fork()


Handle notification of a fork-related event to perform any necessary housekeeping. This function is not a pure virtual so that services only have to implement it if necessary. The default implementation does nothing. 
```c
void asio::detail::resolver_service< Protocol >::notify_fork(asio::io_context::fork_event fork_ev)
```

!!! summary "引数"
	- asio::io_context::fork_event `event` 



### resolve()



```c
results_type asio::detail::resolver_service< Protocol >::resolve(implementation_type &, const query_type &query, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `` 
	- const& `query` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	results_type



### async_resolve()



```c
void asio::detail::resolver_service< Protocol >::async_resolve(implementation_type &impl, const query_type &query, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `query` 
	- Handler & `handler` 



### resolve()



```c
results_type asio::detail::resolver_service< Protocol >::resolve(implementation_type &, const endpoint_type &endpoint, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `` 
	- const& `endpoint` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	results_type



### async_resolve()



```c
void asio::detail::resolver_service< Protocol >::async_resolve(implementation_type &impl, const endpoint_type &endpoint, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `endpoint` 
	- Handler & `handler` 



