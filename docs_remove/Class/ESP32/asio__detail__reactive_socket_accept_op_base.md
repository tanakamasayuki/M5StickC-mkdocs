# asio::detail::reactive_socket_accept_op_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__socket__accept__op__base.html)

## メンバー

### reactive_socket_accept_op_base()



```c
asio::detail::reactive_socket_accept_op_base< Socket, Protocol >::reactive_socket_accept_op_base(socket_type socket, socket_ops::state_type state, Socket &peer, const Protocol &protocol, typename Protocol::endpoint *peer_endpoint, func_type complete_func)
```

!!! summary "引数"
	- socket_type `socket` 
	- socket_ops::state_type `state` 
	- Socket & `peer` 
	- constProtocol & `protocol` 
	- typename Protocol::endpoint * `peer_endpoint` 
	- func_type `complete_func` 



### do_assign()



```c
void asio::detail::reactive_socket_accept_op_base< Socket, Protocol >::do_assign()
```



### do_perform()



```c
static status asio::detail::reactive_socket_accept_op_base< Socket, Protocol >::do_perform(reactor_op *base)
```

!!! summary "引数"
	- reactor_op* `base` 

!!! note "戻り値"
	status



