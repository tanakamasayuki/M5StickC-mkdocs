# asio::detail::reactive_socket_recvmsg_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__socket__recvmsg__op.html)

## メンバー

### ASIO_DEFINE_HANDLER_PTR()



```c
asio::detail::reactive_socket_recvmsg_op< MutableBufferSequence, Handler >::ASIO_DEFINE_HANDLER_PTR(reactive_socket_recvmsg_op)
```

!!! summary "引数"
	- reactive_socket_recvmsg_op `` 



### reactive_socket_recvmsg_op()



```c
asio::detail::reactive_socket_recvmsg_op< MutableBufferSequence, Handler >::reactive_socket_recvmsg_op(socket_type socket, const MutableBufferSequence &buffers, socket_base::message_flags in_flags, socket_base::message_flags &out_flags, Handler &handler)
```

!!! summary "引数"
	- socket_type `socket` 
	- constMutableBufferSequence & `buffers` 
	- socket_base::message_flags `in_flags` 
	- socket_base::message_flags& `out_flags` 
	- Handler & `handler` 



### do_complete()



```c
static void asio::detail::reactive_socket_recvmsg_op< MutableBufferSequence, Handler >::do_complete(void *owner, operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- operation* `base` 
	- std::size_t `` 



