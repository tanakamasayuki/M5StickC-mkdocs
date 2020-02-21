# asio::detail::buffered_flush_handler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1buffered__flush__handler.html)

## メンバー

###  storage_

```c
detail::buffered_stream_storage& asio::detail::buffered_flush_handler< WriteHandler >::storage_
```


###  handler_

```c
WriteHandler asio::detail::buffered_flush_handler< WriteHandler >::handler_
```


### buffered_flush_handler()



```c
asio::detail::buffered_flush_handler< WriteHandler >::buffered_flush_handler(detail::buffered_stream_storage &storage, WriteHandler &handler)
```

!!! summary "引数"
	- detail::buffered_stream_storage& `storage` 
	- WriteHandler & `handler` 



### operator()()



```c
void asio::detail::buffered_flush_handler< WriteHandler >::operator()(const asio::error_code &ec, const std::size_t bytes_written)
```

!!! summary "引数"
	- const& `ec` 
	- conststd::size_t `bytes_written` 



