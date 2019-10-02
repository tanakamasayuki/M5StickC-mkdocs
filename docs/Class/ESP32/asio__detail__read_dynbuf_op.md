# asio::detail::read_dynbuf_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1read__dynbuf__op.html)

## メンバー

###  stream_

```c
AsyncReadStream& asio::detail::read_dynbuf_op< AsyncReadStream, DynamicBuffer, CompletionCondition, ReadHandler >::stream_
```


###  buffers_

```c
DynamicBuffer asio::detail::read_dynbuf_op< AsyncReadStream, DynamicBuffer, CompletionCondition, ReadHandler >::buffers_
```


###  start_

```c
int asio::detail::read_dynbuf_op< AsyncReadStream, DynamicBuffer, CompletionCondition, ReadHandler >::start_
```


###  total_transferred_

```c
std::size_t asio::detail::read_dynbuf_op< AsyncReadStream, DynamicBuffer, CompletionCondition, ReadHandler >::total_transferred_
```


###  handler_

```c
ReadHandler asio::detail::read_dynbuf_op< AsyncReadStream, DynamicBuffer, CompletionCondition, ReadHandler >::handler_
```


### read_dynbuf_op()



```c
asio::detail::read_dynbuf_op< AsyncReadStream, DynamicBuffer, CompletionCondition, ReadHandler >::read_dynbuf_op(AsyncReadStream &stream, ASIO_MOVE_ARG(BufferSequence) buffers, CompletionCondition completion_condition, ReadHandler &handler)
```

!!! summary "引数"
	- AsyncReadStream & `stream` 
	- ASIO_MOVE_ARG(BufferSequence) `buffers` 
	- CompletionCondition `completion_condition` 
	- ReadHandler & `handler` 



### operator()()



```c
void asio::detail::read_dynbuf_op< AsyncReadStream, DynamicBuffer, CompletionCondition, ReadHandler >::operator()(const asio::error_code &ec, std::size_t bytes_transferred, int start=0)
```

!!! summary "引数"
	- const& `ec` 
	- std::size_t `bytes_transferred` 
	- int `start` 



