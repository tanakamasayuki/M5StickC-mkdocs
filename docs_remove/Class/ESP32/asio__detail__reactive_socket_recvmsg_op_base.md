# asio::detail::reactive_socket_recvmsg_op_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__socket__recvmsg__op__base.html)

## メンバー

### reactive_socket_recvmsg_op_base()



```c
asio::detail::reactive_socket_recvmsg_op_base< MutableBufferSequence >::reactive_socket_recvmsg_op_base(socket_type socket, const MutableBufferSequence &buffers, socket_base::message_flags in_flags, socket_base::message_flags &out_flags, func_type complete_func)
```

!!! summary "引数"
	- socket_type `socket` 
	- constMutableBufferSequence & `buffers` 
	- socket_base::message_flags `in_flags` 
	- socket_base::message_flags& `out_flags` 
	- func_type `complete_func` 



### do_perform()



```c
static status asio::detail::reactive_socket_recvmsg_op_base< MutableBufferSequence >::do_perform(reactor_op *base)
```

!!! summary "引数"
	- reactor_op* `base` 

!!! note "戻り値"
	status



