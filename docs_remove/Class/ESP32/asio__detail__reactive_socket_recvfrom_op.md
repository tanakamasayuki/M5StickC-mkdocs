# asio::detail::reactive_socket_recvfrom_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__socket__recvfrom__op.html)

## メンバー

### ASIO_DEFINE_HANDLER_PTR()



```c
asio::detail::reactive_socket_recvfrom_op< MutableBufferSequence, Endpoint, Handler >::ASIO_DEFINE_HANDLER_PTR(reactive_socket_recvfrom_op)
```

!!! summary "引数"
	- reactive_socket_recvfrom_op `` 



### reactive_socket_recvfrom_op()



```c
asio::detail::reactive_socket_recvfrom_op< MutableBufferSequence, Endpoint, Handler >::reactive_socket_recvfrom_op(socket_type socket, int protocol_type, const MutableBufferSequence &buffers, Endpoint &endpoint, socket_base::message_flags flags, Handler &handler)
```

!!! summary "引数"
	- socket_type `socket` 
	- int `protocol_type` 
	- constMutableBufferSequence & `buffers` 
	- Endpoint & `endpoint` 
	- socket_base::message_flags `flags` 
	- Handler & `handler` 



### do_complete()



```c
static void asio::detail::reactive_socket_recvfrom_op< MutableBufferSequence, Endpoint, Handler >::do_complete(void *owner, operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- operation* `base` 
	- std::size_t `` 



