# asio::detail::service_registry



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1service__registry.html)

## メンバー

### service_registry()



```c
ASIO_DECL asio::detail::service_registry::service_registry(execution_context &owner)
```

!!! summary "引数"
	- execution_context& `owner` 

!!! note "戻り値"
	ASIO_DECL



### ~service_registry()



```c
ASIO_DECL asio::detail::service_registry::~service_registry()
```

!!! note "戻り値"
	ASIO_DECL



### shutdown_services()



```c
ASIO_DECL void asio::detail::service_registry::shutdown_services()
```

!!! note "戻り値"
	ASIO_DECLvoid



### destroy_services()



```c
ASIO_DECL void asio::detail::service_registry::destroy_services()
```

!!! note "戻り値"
	ASIO_DECLvoid



### notify_fork()



```c
ASIO_DECL void asio::detail::service_registry::notify_fork(execution_context::fork_event fork_ev)
```

!!! summary "引数"
	- execution_context::fork_event `fork_ev` 

!!! note "戻り値"
	ASIO_DECLvoid



### use_service()



```c
Service & asio::detail::service_registry::use_service()
```

!!! note "戻り値"
	Service &



### use_service()



```c
Service & asio::detail::service_registry::use_service(io_context &owner)
```

!!! summary "引数"
	- io_context& `owner` 

!!! note "戻り値"
	Service &



### add_service()



```c
void asio::detail::service_registry::add_service(Service *new_service)
```

!!! summary "引数"
	- Service * `new_service` 



### has_service()



```c
bool asio::detail::service_registry::has_service() const
```

!!! note "戻り値"
	bool



