# asio::detail::reactive_descriptor_service



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__descriptor__service.html)

## メンバー



### reactive_descriptor_service()



```c
ASIO_DECL asio::detail::reactive_descriptor_service::reactive_descriptor_service(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 

!!! note "戻り値"
	ASIO_DECL



### shutdown()
Destroy all user-defined handler objects owned by the service.


```c
ASIO_DECL void asio::detail::reactive_descriptor_service::shutdown()
```

!!! note "戻り値"
	ASIO_DECLvoid



### construct()



```c
ASIO_DECL void asio::detail::reactive_descriptor_service::construct(implementation_type &impl)
```

!!! summary "引数"
	- implementation_type& `impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### move_construct()



```c
ASIO_DECL void asio::detail::reactive_descriptor_service::move_construct(implementation_type &impl, implementation_type &other_impl)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- implementation_type& `other_impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### move_assign()



```c
ASIO_DECL void asio::detail::reactive_descriptor_service::move_assign(implementation_type &impl, reactive_descriptor_service &other_service, implementation_type &other_impl)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- reactive_descriptor_service& `other_service` 
	- implementation_type& `other_impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### destroy()



```c
ASIO_DECL void asio::detail::reactive_descriptor_service::destroy(implementation_type &impl)
```

!!! summary "引数"
	- implementation_type& `impl` 

!!! note "戻り値"
	ASIO_DECLvoid



### assign()



```c
ASIO_DECL asio::error_code asio::detail::reactive_descriptor_service::assign(implementation_type &impl, const native_handle_type &native_descriptor, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `native_descriptor` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### is_open()



```c
bool asio::detail::reactive_descriptor_service::is_open(const implementation_type &impl) const
```

!!! summary "引数"
	- const& `impl` 

!!! note "戻り値"
	bool



### close()



```c
ASIO_DECL asio::error_code asio::detail::reactive_descriptor_service::close(implementation_type &impl, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### native_handle()



```c
native_handle_type asio::detail::reactive_descriptor_service::native_handle(const implementation_type &impl) const
```

!!! summary "引数"
	- const& `impl` 

!!! note "戻り値"
	native_handle_type



### release()



```c
ASIO_DECL native_handle_type asio::detail::reactive_descriptor_service::release(implementation_type &impl)
```

!!! summary "引数"
	- implementation_type& `impl` 

!!! note "戻り値"
	ASIO_DECL



### cancel()



```c
ASIO_DECL asio::error_code asio::detail::reactive_descriptor_service::cancel(implementation_type &impl, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### io_control()



```c
asio::error_code asio::detail::reactive_descriptor_service::io_control(implementation_type &impl, IO_Control_Command &command, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- IO_Control_Command & `command` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### non_blocking()



```c
bool asio::detail::reactive_descriptor_service::non_blocking(const implementation_type &impl) const
```

!!! summary "引数"
	- const& `impl` 

!!! note "戻り値"
	bool



### non_blocking()



```c
asio::error_code asio::detail::reactive_descriptor_service::non_blocking(implementation_type &impl, bool mode, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- bool `mode` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### native_non_blocking()



```c
bool asio::detail::reactive_descriptor_service::native_non_blocking(const implementation_type &impl) const
```

!!! summary "引数"
	- const& `impl` 

!!! note "戻り値"
	bool



### native_non_blocking()



```c
asio::error_code asio::detail::reactive_descriptor_service::native_non_blocking(implementation_type &impl, bool mode, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- bool `mode` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### wait()



```c
asio::error_code asio::detail::reactive_descriptor_service::wait(implementation_type &impl, posix::descriptor_base::wait_type w, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- posix::descriptor_base::wait_type `w` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### async_wait()



```c
void asio::detail::reactive_descriptor_service::async_wait(implementation_type &impl, posix::descriptor_base::wait_type w, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- posix::descriptor_base::wait_type `w` 
	- Handler & `handler` 



### write_some()



```c
size_t asio::detail::reactive_descriptor_service::write_some(implementation_type &impl, const ConstBufferSequence &buffers, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- constConstBufferSequence & `buffers` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### write_some()



```c
size_t asio::detail::reactive_descriptor_service::write_some(implementation_type &impl, const null_buffers &, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### async_write_some()



```c
void asio::detail::reactive_descriptor_service::async_write_some(implementation_type &impl, const ConstBufferSequence &buffers, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- constConstBufferSequence & `buffers` 
	- Handler & `handler` 



### async_write_some()



```c
void asio::detail::reactive_descriptor_service::async_write_some(implementation_type &impl, const null_buffers &, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `` 
	- Handler & `handler` 



### read_some()



```c
size_t asio::detail::reactive_descriptor_service::read_some(implementation_type &impl, const MutableBufferSequence &buffers, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- constMutableBufferSequence & `buffers` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### read_some()



```c
size_t asio::detail::reactive_descriptor_service::read_some(implementation_type &impl, const null_buffers &, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### async_read_some()



```c
void asio::detail::reactive_descriptor_service::async_read_some(implementation_type &impl, const MutableBufferSequence &buffers, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- constMutableBufferSequence & `buffers` 
	- Handler & `handler` 



### async_read_some()



```c
void asio::detail::reactive_descriptor_service::async_read_some(implementation_type &impl, const null_buffers &, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `` 
	- Handler & `handler` 



