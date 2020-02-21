# asio::detail::wait_handler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1wait__handler.html)

## メンバー

### ASIO_DEFINE_HANDLER_PTR()



```c
asio::detail::wait_handler< Handler >::ASIO_DEFINE_HANDLER_PTR(wait_handler)
```

!!! summary "引数"
	- wait_handler `` 



### wait_handler()



```c
asio::detail::wait_handler< Handler >::wait_handler(Handler &h)
```

!!! summary "引数"
	- Handler & `h` 



### do_complete()



```c
static void asio::detail::wait_handler< Handler >::do_complete(void *owner, operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- operation* `base` 
	- std::size_t `` 



