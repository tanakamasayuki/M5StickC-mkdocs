# asio::detail::write_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1write__op.html)

## メンバー

###  stream_

```c
AsyncWriteStream& asio::detail::write_op< AsyncWriteStream, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::stream_
```


###  buffers_

```c
asio::detail::consuming_buffers<const_buffer, ConstBufferSequence, ConstBufferIterator> asio::detail::write_op< AsyncWriteStream, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::buffers_
```


###  start_

```c
int asio::detail::write_op< AsyncWriteStream, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::start_
```


###  handler_

```c
WriteHandler asio::detail::write_op< AsyncWriteStream, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::handler_
```


### write_op()



```c
asio::detail::write_op< AsyncWriteStream, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::write_op(AsyncWriteStream &stream, const ConstBufferSequence &buffers, CompletionCondition completion_condition, WriteHandler &handler)
```

!!! summary "引数"
	- AsyncWriteStream & `stream` 
	- constConstBufferSequence & `buffers` 
	- CompletionCondition `completion_condition` 
	- WriteHandler & `handler` 



### operator()()



```c
void asio::detail::write_op< AsyncWriteStream, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::operator()(const asio::error_code &ec, std::size_t bytes_transferred, int start=0)
```

!!! summary "引数"
	- const& `ec` 
	- std::size_t `bytes_transferred` 
	- int `start` 



