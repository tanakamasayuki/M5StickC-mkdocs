# asio::detail::reactive_socket_connect_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__socket__connect__op.html)

## メンバー

### ASIO_DEFINE_HANDLER_PTR()



```c
asio::detail::reactive_socket_connect_op< Handler >::ASIO_DEFINE_HANDLER_PTR(reactive_socket_connect_op)
```

!!! summary "引数"
	- reactive_socket_connect_op `` 



### reactive_socket_connect_op()



```c
asio::detail::reactive_socket_connect_op< Handler >::reactive_socket_connect_op(socket_type socket, Handler &handler)
```

!!! summary "引数"
	- socket_type `socket` 
	- Handler & `handler` 



### do_complete()



```c
static void asio::detail::reactive_socket_connect_op< Handler >::do_complete(void *owner, operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- operation* `base` 
	- std::size_t `` 



