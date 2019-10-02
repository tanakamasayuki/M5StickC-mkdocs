# asio::detail::buffered_write_some_handler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1buffered__write__some__handler.html)

## メンバー

###  storage_

```c
detail::buffered_stream_storage& asio::detail::buffered_write_some_handler< ConstBufferSequence, WriteHandler >::storage_
```


###  buffers_

```c
ConstBufferSequence asio::detail::buffered_write_some_handler< ConstBufferSequence, WriteHandler >::buffers_
```


###  handler_

```c
WriteHandler asio::detail::buffered_write_some_handler< ConstBufferSequence, WriteHandler >::handler_
```


### buffered_write_some_handler()



```c
asio::detail::buffered_write_some_handler< ConstBufferSequence, WriteHandler >::buffered_write_some_handler(detail::buffered_stream_storage &storage, const ConstBufferSequence &buffers, WriteHandler &handler)
```

!!! summary "引数"
	- detail::buffered_stream_storage& `storage` 
	- constConstBufferSequence & `buffers` 
	- WriteHandler & `handler` 



### operator()()



```c
void asio::detail::buffered_write_some_handler< ConstBufferSequence, WriteHandler >::operator()(const asio::error_code &ec, std::size_t)
```

!!! summary "引数"
	- const& `ec` 
	- std::size_t `` 



