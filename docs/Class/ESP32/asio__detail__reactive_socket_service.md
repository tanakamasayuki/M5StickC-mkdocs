# asio::detail::reactive_socket_service



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__socket__service.html)

## メンバー







### reactive_socket_service()



```c
asio::detail::reactive_socket_service< Protocol >::reactive_socket_service(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### shutdown()
Destroy all user-defined handler objects owned by the service.


```c
void asio::detail::reactive_socket_service< Protocol >::shutdown()
```



### move_construct()



```c
void asio::detail::reactive_socket_service< Protocol >::move_construct(implementation_type &impl, implementation_type &other_impl)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- implementation_type& `other_impl` 



### move_assign()



```c
void asio::detail::reactive_socket_service< Protocol >::move_assign(implementation_type &impl, reactive_socket_service_base &other_service, implementation_type &other_impl)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- reactive_socket_service_base& `other_service` 
	- implementation_type& `other_impl` 



### converting_move_construct()



```c
void asio::detail::reactive_socket_service< Protocol >::converting_move_construct(implementation_type &impl, reactive_socket_service< Protocol1 > &, typename reactive_socket_service< Protocol1 >::implementation_type &other_impl)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- reactive_socket_service< Protocol1 > & `` 
	- reactive_socket_servicetypename < Protocol1 >:: & `other_impl` 



### open()



```c
asio::error_code asio::detail::reactive_socket_service< Protocol >::open(implementation_type &impl, const protocol_type &protocol, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `protocol` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### assign()



```c
asio::error_code asio::detail::reactive_socket_service< Protocol >::assign(implementation_type &impl, const protocol_type &protocol, const native_handle_type &native_socket, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `protocol` 
	- const& `native_socket` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### native_handle()



```c
native_handle_type asio::detail::reactive_socket_service< Protocol >::native_handle(implementation_type &impl)
```

!!! summary "引数"
	- implementation_type& `impl` 

!!! note "戻り値"
	native_handle_type



### bind()



```c
asio::error_code asio::detail::reactive_socket_service< Protocol >::bind(implementation_type &impl, const endpoint_type &endpoint, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `endpoint` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### set_option()



```c
asio::error_code asio::detail::reactive_socket_service< Protocol >::set_option(implementation_type &impl, const Option &option, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- constOption & `option` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### get_option()



```c
asio::error_code asio::detail::reactive_socket_service< Protocol >::get_option(const implementation_type &impl, Option &option, asio::error_code &ec) const
```

!!! summary "引数"
	- const& `impl` 
	- Option & `option` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### local_endpoint()



```c
endpoint_type asio::detail::reactive_socket_service< Protocol >::local_endpoint(const implementation_type &impl, asio::error_code &ec) const
```

!!! summary "引数"
	- const& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	endpoint_type



### remote_endpoint()



```c
endpoint_type asio::detail::reactive_socket_service< Protocol >::remote_endpoint(const implementation_type &impl, asio::error_code &ec) const
```

!!! summary "引数"
	- const& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	endpoint_type



### shutdown()



```c
asio::error_code asio::detail::reactive_socket_service< Protocol >::shutdown(base_implementation_type &impl, socket_base::shutdown_type what, asio::error_code &ec)
```

!!! summary "引数"
	- base_implementation_type& `impl` 
	- socket_base::shutdown_type `what` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### send_to()



```c
size_t asio::detail::reactive_socket_service< Protocol >::send_to(implementation_type &impl, const ConstBufferSequence &buffers, const endpoint_type &destination, socket_base::message_flags flags, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- constConstBufferSequence & `buffers` 
	- const& `destination` 
	- socket_base::message_flags `flags` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### send_to()



```c
size_t asio::detail::reactive_socket_service< Protocol >::send_to(implementation_type &impl, const null_buffers &, const endpoint_type &, socket_base::message_flags, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- socket_base::message_flags `` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### async_send_to()



```c
void asio::detail::reactive_socket_service< Protocol >::async_send_to(implementation_type &impl, const ConstBufferSequence &buffers, const endpoint_type &destination, socket_base::message_flags flags, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- constConstBufferSequence & `buffers` 
	- const& `destination` 
	- socket_base::message_flags `flags` 
	- Handler & `handler` 



### async_send_to()



```c
void asio::detail::reactive_socket_service< Protocol >::async_send_to(implementation_type &impl, const null_buffers &, const endpoint_type &, socket_base::message_flags, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- socket_base::message_flags `` 
	- Handler & `handler` 



### receive_from()



```c
size_t asio::detail::reactive_socket_service< Protocol >::receive_from(implementation_type &impl, const MutableBufferSequence &buffers, endpoint_type &sender_endpoint, socket_base::message_flags flags, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- constMutableBufferSequence & `buffers` 
	- endpoint_type& `sender_endpoint` 
	- socket_base::message_flags `flags` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### receive_from()



```c
size_t asio::detail::reactive_socket_service< Protocol >::receive_from(implementation_type &impl, const null_buffers &, endpoint_type &sender_endpoint, socket_base::message_flags, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- socket_base::message_flags `` 
	- endpoint_type& `sender_endpoint` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	size_t



### async_receive_from()



```c
void asio::detail::reactive_socket_service< Protocol >::async_receive_from(implementation_type &impl, const MutableBufferSequence &buffers, endpoint_type &sender_endpoint, socket_base::message_flags flags, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- constMutableBufferSequence & `buffers` 
	- endpoint_type& `sender_endpoint` 
	- socket_base::message_flags `flags` 
	- Handler & `handler` 



### async_receive_from()



```c
void asio::detail::reactive_socket_service< Protocol >::async_receive_from(implementation_type &impl, const null_buffers &, endpoint_type &sender_endpoint, socket_base::message_flags flags, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `` 
	- endpoint_type& `sender_endpoint` 
	- socket_base::message_flags `flags` 
	- Handler & `handler` 



### accept()



```c
asio::error_code asio::detail::reactive_socket_service< Protocol >::accept(implementation_type &impl, Socket &peer, endpoint_type *peer_endpoint, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- Socket & `peer` 
	- endpoint_type* `peer_endpoint` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### async_accept()



```c
void asio::detail::reactive_socket_service< Protocol >::async_accept(implementation_type &impl, Socket &peer, endpoint_type *peer_endpoint, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- Socket & `peer` 
	- endpoint_type* `peer_endpoint` 
	- Handler & `handler` 



### connect()



```c
asio::error_code asio::detail::reactive_socket_service< Protocol >::connect(implementation_type &impl, const endpoint_type &peer_endpoint, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `peer_endpoint` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	asio::error_code



### async_connect()



```c
void asio::detail::reactive_socket_service< Protocol >::async_connect(implementation_type &impl, const endpoint_type &peer_endpoint, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `peer_endpoint` 
	- Handler & `handler` 



