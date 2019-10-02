# asio::detail::reactive_socket_connect_op_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__socket__connect__op__base.html)

## メンバー

### reactive_socket_connect_op_base()



```c
asio::detail::reactive_socket_connect_op_base::reactive_socket_connect_op_base(socket_type socket, func_type complete_func)
```

!!! summary "引数"
	- socket_type `socket` 
	- func_type `complete_func` 



### do_perform()



```c
static status asio::detail::reactive_socket_connect_op_base::do_perform(reactor_op *base)
```

!!! summary "引数"
	- reactor_op* `base` 

!!! note "戻り値"
	status



