# asio::detail::descriptor_read_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1descriptor__read__op.html)

## メンバー

### ASIO_DEFINE_HANDLER_PTR()



```c
asio::detail::descriptor_read_op< MutableBufferSequence, Handler >::ASIO_DEFINE_HANDLER_PTR(descriptor_read_op)
```

!!! summary "引数"
	- descriptor_read_op `` 



### descriptor_read_op()



```c
asio::detail::descriptor_read_op< MutableBufferSequence, Handler >::descriptor_read_op(int descriptor, const MutableBufferSequence &buffers, Handler &handler)
```

!!! summary "引数"
	- int `descriptor` 
	- constMutableBufferSequence & `buffers` 
	- Handler & `handler` 



### do_complete()



```c
static void asio::detail::descriptor_read_op< MutableBufferSequence, Handler >::do_complete(void *owner, operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- operation* `base` 
	- std::size_t `` 



