# asio::detail::read_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1read__op.html)

## メンバー

###  stream_

```c
AsyncReadStream& asio::detail::read_op< AsyncReadStream, MutableBufferSequence, MutableBufferIterator, CompletionCondition, ReadHandler >::stream_
```


###  buffers_

```c
asio::detail::consuming_buffers<mutable_buffer, MutableBufferSequence, MutableBufferIterator> asio::detail::read_op< AsyncReadStream, MutableBufferSequence, MutableBufferIterator, CompletionCondition, ReadHandler >::buffers_
```


###  start_

```c
int asio::detail::read_op< AsyncReadStream, MutableBufferSequence, MutableBufferIterator, CompletionCondition, ReadHandler >::start_
```


###  handler_

```c
ReadHandler asio::detail::read_op< AsyncReadStream, MutableBufferSequence, MutableBufferIterator, CompletionCondition, ReadHandler >::handler_
```


### read_op()



```c
asio::detail::read_op< AsyncReadStream, MutableBufferSequence, MutableBufferIterator, CompletionCondition, ReadHandler >::read_op(AsyncReadStream &stream, const MutableBufferSequence &buffers, CompletionCondition completion_condition, ReadHandler &handler)
```

!!! summary "引数"
	- AsyncReadStream & `stream` 
	- constMutableBufferSequence & `buffers` 
	- CompletionCondition `completion_condition` 
	- ReadHandler & `handler` 



### operator()()



```c
void asio::detail::read_op< AsyncReadStream, MutableBufferSequence, MutableBufferIterator, CompletionCondition, ReadHandler >::operator()(const asio::error_code &ec, std::size_t bytes_transferred, int start=0)
```

!!! summary "引数"
	- const& `ec` 
	- std::size_t `bytes_transferred` 
	- int `start` 



