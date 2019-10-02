# asio::detail::reactive_socket_recvfrom_op_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__socket__recvfrom__op__base.html)

## メンバー

### reactive_socket_recvfrom_op_base()



```c
asio::detail::reactive_socket_recvfrom_op_base< MutableBufferSequence, Endpoint >::reactive_socket_recvfrom_op_base(socket_type socket, int protocol_type, const MutableBufferSequence &buffers, Endpoint &endpoint, socket_base::message_flags flags, func_type complete_func)
```

!!! summary "引数"
	- socket_type `socket` 
	- int `protocol_type` 
	- constMutableBufferSequence & `buffers` 
	- Endpoint & `endpoint` 
	- socket_base::message_flags `flags` 
	- func_type `complete_func` 



### do_perform()



```c
static status asio::detail::reactive_socket_recvfrom_op_base< MutableBufferSequence, Endpoint >::do_perform(reactor_op *base)
```

!!! summary "引数"
	- reactor_op* `base` 

!!! note "戻り値"
	status



