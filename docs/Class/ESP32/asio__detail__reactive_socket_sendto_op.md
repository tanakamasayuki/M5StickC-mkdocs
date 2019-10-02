# asio::detail::reactive_socket_sendto_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__socket__sendto__op.html)

## メンバー

### ASIO_DEFINE_HANDLER_PTR()



```c
asio::detail::reactive_socket_sendto_op< ConstBufferSequence, Endpoint, Handler >::ASIO_DEFINE_HANDLER_PTR(reactive_socket_sendto_op)
```

!!! summary "引数"
	- reactive_socket_sendto_op `` 



### reactive_socket_sendto_op()



```c
asio::detail::reactive_socket_sendto_op< ConstBufferSequence, Endpoint, Handler >::reactive_socket_sendto_op(socket_type socket, const ConstBufferSequence &buffers, const Endpoint &endpoint, socket_base::message_flags flags, Handler &handler)
```

!!! summary "引数"
	- socket_type `socket` 
	- constConstBufferSequence & `buffers` 
	- constEndpoint & `endpoint` 
	- socket_base::message_flags `flags` 
	- Handler & `handler` 



### do_complete()



```c
static void asio::detail::reactive_socket_sendto_op< ConstBufferSequence, Endpoint, Handler >::do_complete(void *owner, operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- operation* `base` 
	- std::size_t `` 



