# asio::detail::buffered_read_some_handler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1buffered__read__some__handler.html)

## メンバー

###  storage_

```c
detail::buffered_stream_storage& asio::detail::buffered_read_some_handler< MutableBufferSequence, ReadHandler >::storage_
```


###  buffers_

```c
MutableBufferSequence asio::detail::buffered_read_some_handler< MutableBufferSequence, ReadHandler >::buffers_
```


###  handler_

```c
ReadHandler asio::detail::buffered_read_some_handler< MutableBufferSequence, ReadHandler >::handler_
```


### buffered_read_some_handler()



```c
asio::detail::buffered_read_some_handler< MutableBufferSequence, ReadHandler >::buffered_read_some_handler(detail::buffered_stream_storage &storage, const MutableBufferSequence &buffers, ReadHandler &handler)
```

!!! summary "引数"
	- detail::buffered_stream_storage& `storage` 
	- constMutableBufferSequence & `buffers` 
	- ReadHandler & `handler` 



### operator()()



```c
void asio::detail::buffered_read_some_handler< MutableBufferSequence, ReadHandler >::operator()(const asio::error_code &ec, std::size_t)
```

!!! summary "引数"
	- const& `ec` 
	- std::size_t `` 



