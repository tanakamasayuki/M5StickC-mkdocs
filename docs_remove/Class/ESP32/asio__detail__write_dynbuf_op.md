# asio::detail::write_dynbuf_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1write__dynbuf__op.html)

## メンバー

###  stream_

```c
AsyncWriteStream& asio::detail::write_dynbuf_op< AsyncWriteStream, DynamicBuffer, CompletionCondition, WriteHandler >::stream_
```


###  buffers_

```c
DynamicBuffer asio::detail::write_dynbuf_op< AsyncWriteStream, DynamicBuffer, CompletionCondition, WriteHandler >::buffers_
```


###  completion_condition_

```c
CompletionCondition asio::detail::write_dynbuf_op< AsyncWriteStream, DynamicBuffer, CompletionCondition, WriteHandler >::completion_condition_
```


###  handler_

```c
WriteHandler asio::detail::write_dynbuf_op< AsyncWriteStream, DynamicBuffer, CompletionCondition, WriteHandler >::handler_
```


### write_dynbuf_op()



```c
asio::detail::write_dynbuf_op< AsyncWriteStream, DynamicBuffer, CompletionCondition, WriteHandler >::write_dynbuf_op(AsyncWriteStream &stream, ASIO_MOVE_ARG(BufferSequence) buffers, CompletionCondition completion_condition, WriteHandler &handler)
```

!!! summary "引数"
	- AsyncWriteStream & `stream` 
	- ASIO_MOVE_ARG(BufferSequence) `buffers` 
	- CompletionCondition `completion_condition` 
	- WriteHandler & `handler` 



### operator()()



```c
void asio::detail::write_dynbuf_op< AsyncWriteStream, DynamicBuffer, CompletionCondition, WriteHandler >::operator()(const asio::error_code &ec, std::size_t bytes_transferred, int start=0)
```

!!! summary "引数"
	- const& `ec` 
	- std::size_t `bytes_transferred` 
	- int `start` 



