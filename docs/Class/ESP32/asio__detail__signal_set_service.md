# asio::detail::signal_set_service



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1signal__set__service.html)

## メンバー

### signal_set_service()



```c
ASIO_DECL asio::detail::signal_set_service::signal_set_service(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 

!!! note "戻り値"
	ASIO_DECL



### ~signal_set_service()



```c
ASIO_DECL asio::detail::signal_set_service::~signal_set_service()
```

!!! note "戻り値"
	ASIO_DECL



### shutdown()
Destroy all user-defined handler objects owned by the service.


```c
ASIO_DECL void asio::detail::signal_set_service::shutdown()
```

!!! note "戻り値"
	ASIO_DECLvoid



### notify_fork()


Handle notification of a fork-related event to perform any necessary housekeeping. This function is not a pure virtual so that services only have to implement it if necessary. The default implementation does nothing. 
```c
ASIO_DECL void asio::detail::signal_set_service::notify_fork(asio::io_context::fork_event fork_ev)
```

!!! summary "引数"
	- asio::io_context::fork_event `event` 

!!! note "戻り値"
	ASIO_DECLvoid



### construct()



```c
ASIO_DECL void asio::detail::signal_set_service::construct(implementation_type &impl)
```

!!! summary "引数"
	- implementation_type& `impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### destroy()



```c
ASIO_DECL void asio::detail::signal_set_service::destroy(implementation_type &impl)
```

!!! summary "引数"
	- implementation_type& `impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### add()



```c
ASIO_DECL asio::error_code asio::detail::signal_set_service::add(implementation_type &impl, int signal_number, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- int `signal_number` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### remove()



```c
ASIO_DECL asio::error_code asio::detail::signal_set_service::remove(implementation_type &impl, int signal_number, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- int `signal_number` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### clear()



```c
ASIO_DECL asio::error_code asio::detail::signal_set_service::clear(implementation_type &impl, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### cancel()



```c
ASIO_DECL asio::error_code asio::detail::signal_set_service::cancel(implementation_type &impl, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### async_wait()



```c
void asio::detail::signal_set_service::async_wait(implementation_type &impl, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- Handler & `handler` 



### deliver_signal()



```c
static ASIO_DECL void asio::detail::signal_set_service::deliver_signal(int signal_number)
```

!!! summary "引数"
	- int `signal_number` 

!!! note "戻り値"
	ASIO_DECLvoid



