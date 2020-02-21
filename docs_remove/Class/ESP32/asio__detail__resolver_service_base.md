# asio::detail::resolver_service_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1resolver__service__base.html)

## メンバー



### resolver_service_base()



```c
ASIO_DECL asio::detail::resolver_service_base::resolver_service_base(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 

!!! note "戻り値"
	ASIO_DECL



### ~resolver_service_base()



```c
ASIO_DECL asio::detail::resolver_service_base::~resolver_service_base()
```

!!! note "戻り値"
	ASIO_DECL



### base_shutdown()



```c
ASIO_DECL void asio::detail::resolver_service_base::base_shutdown()
```

!!! note "戻り値"
	ASIO_DECLvoid



### base_notify_fork()



```c
ASIO_DECL void asio::detail::resolver_service_base::base_notify_fork(asio::io_context::fork_event fork_ev)
```

!!! summary "引数"
	- asio::io_context::fork_event `fork_ev` 

!!! note "戻り値"
	ASIO_DECLvoid



### construct()



```c
ASIO_DECL void asio::detail::resolver_service_base::construct(implementation_type &impl)
```

!!! summary "引数"
	- implementation_type& `impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### destroy()



```c
ASIO_DECL void asio::detail::resolver_service_base::destroy(implementation_type &)
```

!!! summary "引数"
	- implementation_type& `` 

!!! note "戻り値"
	ASIO_DECLvoid



### move_construct()



```c
ASIO_DECL void asio::detail::resolver_service_base::move_construct(implementation_type &impl, implementation_type &other_impl)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- implementation_type& `other_impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### move_assign()



```c
ASIO_DECL void asio::detail::resolver_service_base::move_assign(implementation_type &impl, resolver_service_base &other_service, implementation_type &other_impl)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- resolver_service_base& `other_service` 
	- implementation_type& `other_impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### cancel()



```c
ASIO_DECL void asio::detail::resolver_service_base::cancel(implementation_type &impl)
```

!!! summary "引数"
	- implementation_type& `impl` 

!!! note "戻り値"
	ASIO_DECLvoid



