# asio::detail::signal_handler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1signal__handler.html)

## メンバー

### ASIO_DEFINE_HANDLER_PTR()



```c
asio::detail::signal_handler< Handler >::ASIO_DEFINE_HANDLER_PTR(signal_handler)
```

!!! summary "引数"
	- signal_handler `` 



### signal_handler()



```c
asio::detail::signal_handler< Handler >::signal_handler(Handler &h)
```

!!! summary "引数"
	- Handler & `h` 



### do_complete()



```c
static void asio::detail::signal_handler< Handler >::do_complete(void *owner, operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- operation* `base` 
	- std::size_t `` 



