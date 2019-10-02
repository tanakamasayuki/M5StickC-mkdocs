# asio::detail::buffered_fill_handler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1buffered__fill__handler.html)

## メンバー

###  storage_

```c
detail::buffered_stream_storage& asio::detail::buffered_fill_handler< ReadHandler >::storage_
```


###  previous_size_

```c
std::size_t asio::detail::buffered_fill_handler< ReadHandler >::previous_size_
```


###  handler_

```c
ReadHandler asio::detail::buffered_fill_handler< ReadHandler >::handler_
```


### buffered_fill_handler()



```c
asio::detail::buffered_fill_handler< ReadHandler >::buffered_fill_handler(detail::buffered_stream_storage &storage, std::size_t previous_size, ReadHandler &handler)
```

!!! summary "引数"
	- detail::buffered_stream_storage& `storage` 
	- std::size_t `previous_size` 
	- ReadHandler & `handler` 



### operator()()



```c
void asio::detail::buffered_fill_handler< ReadHandler >::operator()(const asio::error_code &ec, const std::size_t bytes_transferred)
```

!!! summary "引数"
	- const& `ec` 
	- conststd::size_t `bytes_transferred` 



