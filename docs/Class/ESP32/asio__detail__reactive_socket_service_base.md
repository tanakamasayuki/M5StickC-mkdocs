# asio::detail::reactive_socket_service_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__socket__service__base.html)

## メンバー



### reactive_socket_service_base()



```c
ASIO_DECL asio::detail::reactive_socket_service_base::reactive_socket_service_base(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 

!!! note "戻り値"
	ASIO_DECL



### base_shutdown()



```c
ASIO_DECL void asio::detail::reactive_socket_service_base::base_shutdown()
```

!!! note "戻り値"
	ASIO_DECLvoid



### construct()



```c
ASIO_DECL void asio::detail::reactive_socket_service_base::construct(base_implementation_type &impl)
```

!!! summary "引数"
	- base_implementation_type& `impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### base_move_construct()



```c
ASIO_DECL void asio::detail::reactive_socket_service_base::base_move_construct(base_implementation_type &impl, base_implementation_type &other_impl)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- base_implementation_type& `other_impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### base_move_assign()



```c
ASIO_DECL void asio::detail::reactive_socket_service_base::base_move_assign(base_implementation_type &impl, reactive_socket_service_base &other_service, base_implementation_type &other_impl)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- reactive_socket_service_base& `other_service` 
	- base_implementation_type& `other_impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### destroy()



```c
ASIO_DECL void asio::detail::reactive_socket_service_base::destroy(base_implementation_type &impl)
```

!!! summary "引数"
	- base_implementation_type& `impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### is_open()



```c
bool asio::detail::reactive_socket_service_base::is_open(const base_implementation_type &impl) const
```

!!! summary "引数"
	- const& `impl` 

!!! note "戻り値"
	bool



### close()



```c
ASIO_DECL asio::error_code asio::detail::reactive_socket_service_base::close(base_implementation_type &impl, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### release()



```c
ASIO_DECL socket_type asio::detail::reactive_socket_service_base::release(base_implementation_type &impl, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### native_handle()



```c
native_handle_type asio::detail::reactive_socket_service_base::native_handle(base_implementation_type &impl)
```

!!! summary "引数"
	- base_implementation_type& `impl` 

!!! note "戻り値"
	native_handle_type



### cancel()



```c
ASIO_DECL asio::error_code asio::detail::reactive_socket_service_base::cancel(base_implementation_type &impl, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### at_mark()



```c
bool asio::detail::reactive_socket_service_base::at_mark(const base_implementation_type &impl, asio::error_code &ec) const
```

!!! summary "引数"
	- const& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	bool



### available()



```c
std::size_t asio::detail::reactive_socket_service_base::available(const base_implementation_type &impl, asio::error_code &ec) const
```

!!! summary "引数"
	- const& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	std::size_t



### listen()



```c
asio::error_code asio::detail::reactive_socket_service_base::listen(base_implementation_type &impl, int backlog, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- int `backlog` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### io_control()



```c
asio::error_code asio::detail::reactive_socket_service_base::io_control(base_implementation_type &impl, IO_Control_Command &command, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- IO_Control_Command & `command` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### non_blocking()



```c
bool asio::detail::reactive_socket_service_base::non_blocking(const base_implementation_type &impl) const
```

!!! summary "引数"
	- const& `impl` 

!!! note "戻り値"
	bool



### non_blocking()



```c
asio::error_code asio::detail::reactive_socket_service_base::non_blocking(base_implementation_type &impl, bool mode, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- bool `mode` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### native_non_blocking()



```c
bool asio::detail::reactive_socket_service_base::native_non_blocking(const base_implementation_type &impl) const
```

!!! summary "引数"
	- const& `impl` 

!!! note "戻り値"
	bool



### native_non_blocking()



```c
asio::error_code asio::detail::reactive_socket_service_base::native_non_blocking(base_implementation_type &impl, bool mode, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- bool `mode` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### wait()



```c
asio::error_code asio::detail::reactive_socket_service_base::wait(base_implementation_type &impl, socket_base::wait_type w, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- socket_base::wait_type `w` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### async_wait()



```c
void asio::detail::reactive_socket_service_base::async_wait(base_implementation_type &impl, socket_base::wait_type w, Handler &handler)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- socket_base::wait_type `w` 
	- Handler & `handler` 



### send()



```c
size_t asio::detail::reactive_socket_service_base::send(base_implementation_type &impl, const ConstBufferSequence &buffers, socket_base::message_flags flags, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- constConstBufferSequence & `buffers` 
	- socket_base::message_flags `flags` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### send()



```c
size_t asio::detail::reactive_socket_service_base::send(base_implementation_type &impl, const null_buffers &, socket_base::message_flags, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- socket_base::message_flags `` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### async_send()



```c
void asio::detail::reactive_socket_service_base::async_send(base_implementation_type &impl, const ConstBufferSequence &buffers, socket_base::message_flags flags, Handler &handler)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- constConstBufferSequence & `buffers` 
	- socket_base::message_flags `flags` 
	- Handler & `handler` 



### async_send()



```c
void asio::detail::reactive_socket_service_base::async_send(base_implementation_type &impl, const null_buffers &, socket_base::message_flags, Handler &handler)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- socket_base::message_flags `` 
	- Handler & `handler` 



### receive()



```c
size_t asio::detail::reactive_socket_service_base::receive(base_implementation_type &impl, const MutableBufferSequence &buffers, socket_base::message_flags flags, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- constMutableBufferSequence & `buffers` 
	- socket_base::message_flags `flags` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### receive()



```c
size_t asio::detail::reactive_socket_service_base::receive(base_implementation_type &impl, const null_buffers &, socket_base::message_flags, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- socket_base::message_flags `` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### async_receive()



```c
void asio::detail::reactive_socket_service_base::async_receive(base_implementation_type &impl, const MutableBufferSequence &buffers, socket_base::message_flags flags, Handler &handler)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- constMutableBufferSequence & `buffers` 
	- socket_base::message_flags `flags` 
	- Handler & `handler` 



### async_receive()



```c
void asio::detail::reactive_socket_service_base::async_receive(base_implementation_type &impl, const null_buffers &, socket_base::message_flags flags, Handler &handler)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- const& `` 
	- socket_base::message_flags `flags` 
	- Handler & `handler` 



### receive_with_flags()



```c
size_t asio::detail::reactive_socket_service_base::receive_with_flags(base_implementation_type &impl, const MutableBufferSequence &buffers, socket_base::message_flags in_flags, socket_base::message_flags &out_flags, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- constMutableBufferSequence & `buffers` 
	- socket_base::message_flags `in_flags` 
	- socket_base::message_flags& `out_flags` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### receive_with_flags()



```c
size_t asio::detail::reactive_socket_service_base::receive_with_flags(base_implementation_type &impl, const null_buffers &, socket_base::message_flags, socket_base::message_flags &out_flags, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- socket_base::message_flags `` 
	- socket_base::message_flags& `out_flags` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### async_receive_with_flags()



```c
void asio::detail::reactive_socket_service_base::async_receive_with_flags(base_implementation_type &impl, const MutableBufferSequence &buffers, socket_base::message_flags in_flags, socket_base::message_flags &out_flags, Handler &handler)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- constMutableBufferSequence & `buffers` 
	- socket_base::message_flags `in_flags` 
	- socket_base::message_flags& `out_flags` 
	- Handler & `handler` 



### async_receive_with_flags()



```c
void asio::detail::reactive_socket_service_base::async_receive_with_flags(base_implementation_type &impl, const null_buffers &, socket_base::message_flags in_flags, socket_base::message_flags &out_flags, Handler &handler)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- const& `` 
	- socket_base::message_flags `in_flags` 
	- socket_base::message_flags& `out_flags` 
	- Handler & `handler` 



