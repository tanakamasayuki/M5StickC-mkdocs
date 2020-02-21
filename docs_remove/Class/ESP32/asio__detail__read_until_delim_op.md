# asio::detail::read_until_delim_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1read__until__delim__op.html)

## メンバー

###  stream_

```c
AsyncReadStream& asio::detail::read_until_delim_op< AsyncReadStream, DynamicBuffer, ReadHandler >::stream_
```


###  buffers_

```c
DynamicBuffer asio::detail::read_until_delim_op< AsyncReadStream, DynamicBuffer, ReadHandler >::buffers_
```


###  delim_

```c
char asio::detail::read_until_delim_op< AsyncReadStream, DynamicBuffer, ReadHandler >::delim_
```


###  start_

```c
int asio::detail::read_until_delim_op< AsyncReadStream, DynamicBuffer, ReadHandler >::start_
```


###  search_position_

```c
std::size_t asio::detail::read_until_delim_op< AsyncReadStream, DynamicBuffer, ReadHandler >::search_position_
```


###  handler_

```c
ReadHandler asio::detail::read_until_delim_op< AsyncReadStream, DynamicBuffer, ReadHandler >::handler_
```


### read_until_delim_op()



```c
asio::detail::read_until_delim_op< AsyncReadStream, DynamicBuffer, ReadHandler >::read_until_delim_op(AsyncReadStream &stream, ASIO_MOVE_ARG(BufferSequence) buffers, char delim, ReadHandler &handler)
```

!!! summary "引数"
	- AsyncReadStream & `stream` 
	- ASIO_MOVE_ARG(BufferSequence) `buffers` 
	- char `delim` 
	- ReadHandler & `handler` 



### operator()()



```c
void asio::detail::read_until_delim_op< AsyncReadStream, DynamicBuffer, ReadHandler >::operator()(const asio::error_code &ec, std::size_t bytes_transferred, int start=0)
```

!!! summary "引数"
	- const& `ec` 
	- std::size_t `bytes_transferred` 
	- int `start` 



