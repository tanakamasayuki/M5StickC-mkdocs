# asio::detail::reactive_null_buffers_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__null__buffers__op.html)

## メンバー

### ASIO_DEFINE_HANDLER_PTR()



```c
asio::detail::reactive_null_buffers_op< Handler >::ASIO_DEFINE_HANDLER_PTR(reactive_null_buffers_op)
```

!!! summary "引数"
	- reactive_null_buffers_op `` 



### reactive_null_buffers_op()



```c
asio::detail::reactive_null_buffers_op< Handler >::reactive_null_buffers_op(Handler &handler)
```

!!! summary "引数"
	- Handler & `handler` 



### do_perform()



```c
static status asio::detail::reactive_null_buffers_op< Handler >::do_perform(reactor_op *)
```

!!! summary "引数"
	- reactor_op* `` 

!!! note "戻り値"
	status



### do_complete()



```c
static void asio::detail::reactive_null_buffers_op< Handler >::do_complete(void *owner, operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- operation* `base` 
	- std::size_t `` 



