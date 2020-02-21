# asio::detail::reactive_wait_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactive__wait__op.html)

## メンバー

### ASIO_DEFINE_HANDLER_PTR()



```c
asio::detail::reactive_wait_op< Handler >::ASIO_DEFINE_HANDLER_PTR(reactive_wait_op)
```

!!! summary "引数"
	- reactive_wait_op `` 



### reactive_wait_op()



```c
asio::detail::reactive_wait_op< Handler >::reactive_wait_op(Handler &handler)
```

!!! summary "引数"
	- Handler & `handler` 



### do_perform()



```c
static status asio::detail::reactive_wait_op< Handler >::do_perform(reactor_op *)
```

!!! summary "引数"
	- reactor_op* `` 

!!! note "戻り値"
	status



### do_complete()



```c
static void asio::detail::reactive_wait_op< Handler >::do_complete(void *owner, operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- operation* `base` 
	- std::size_t `` 



