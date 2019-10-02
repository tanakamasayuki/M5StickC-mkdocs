# asio::detail::descriptor_write_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1descriptor__write__op.html)

## メンバー

### ASIO_DEFINE_HANDLER_PTR()



```c
asio::detail::descriptor_write_op< ConstBufferSequence, Handler >::ASIO_DEFINE_HANDLER_PTR(descriptor_write_op)
```

!!! summary "引数"
	- descriptor_write_op `` 



### descriptor_write_op()



```c
asio::detail::descriptor_write_op< ConstBufferSequence, Handler >::descriptor_write_op(int descriptor, const ConstBufferSequence &buffers, Handler &handler)
```

!!! summary "引数"
	- int `descriptor` 
	- constConstBufferSequence & `buffers` 
	- Handler & `handler` 



### do_complete()



```c
static void asio::detail::descriptor_write_op< ConstBufferSequence, Handler >::do_complete(void *owner, operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- operation* `base` 
	- std::size_t `` 



