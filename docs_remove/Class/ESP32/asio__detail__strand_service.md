# asio::detail::strand_service



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1strand__service.html)

## メンバー



### strand_service()



```c
ASIO_DECL asio::detail::strand_service::strand_service(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 

!!! note "戻り値"
	ASIO_DECL



### shutdown()
Destroy all user-defined handler objects owned by the service.


```c
ASIO_DECL void asio::detail::strand_service::shutdown()
```

!!! note "戻り値"
	ASIO_DECLvoid



### construct()



```c
ASIO_DECL void asio::detail::strand_service::construct(implementation_type &impl)
```

!!! summary "引数"
	- implementation_type& `impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### dispatch()



```c
void asio::detail::strand_service::dispatch(implementation_type &impl, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- Handler & `handler` 



### post()



```c
void asio::detail::strand_service::post(implementation_type &impl, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- Handler & `handler` 



### running_in_this_thread()



```c
ASIO_DECL bool asio::detail::strand_service::running_in_this_thread(const implementation_type &impl) const
```

!!! summary "引数"
	- const& `impl` 

!!! note "戻り値"
	ASIO_DECL



