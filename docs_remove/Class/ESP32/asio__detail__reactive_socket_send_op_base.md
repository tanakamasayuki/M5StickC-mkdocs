# asio::detail::reactive_socket_send_op_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__socket__send__op__base.html)

## メンバー

### reactive_socket_send_op_base()



```c
asio::detail::reactive_socket_send_op_base< ConstBufferSequence >::reactive_socket_send_op_base(socket_type socket, socket_ops::state_type state, const ConstBufferSequence &buffers, socket_base::message_flags flags, func_type complete_func)
```

!!! summary "引数"
	- socket_type `socket` 
	- socket_ops::state_type `state` 
	- constConstBufferSequence & `buffers` 
	- socket_base::message_flags `flags` 
	- func_type `complete_func` 



### do_perform()



```c
static status asio::detail::reactive_socket_send_op_base< ConstBufferSequence >::do_perform(reactor_op *base)
```

!!! summary "引数"
	- reactor_op* `base` 

!!! note "戻り値"
	status



