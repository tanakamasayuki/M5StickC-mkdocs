# asio::detail::completion_handler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1completion__handler.html)

## メンバー

### ASIO_DEFINE_HANDLER_PTR()



```c
asio::detail::completion_handler< Handler >::ASIO_DEFINE_HANDLER_PTR(completion_handler)
```

!!! summary "引数"
	- completion_handler `` 



### completion_handler()



```c
asio::detail::completion_handler< Handler >::completion_handler(Handler &h)
```

!!! summary "引数"
	- Handler & `h` 



### do_complete()



```c
static void asio::detail::completion_handler< Handler >::do_complete(void *owner, operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- operation* `base` 
	- std::size_t `` 



