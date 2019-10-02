# asio::detail::write_at_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1write__at__op.html)

## メンバー

###  device_

```c
AsyncRandomAccessWriteDevice& asio::detail::write_at_op< AsyncRandomAccessWriteDevice, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::device_
```


###  offset_

```c
uint64_t asio::detail::write_at_op< AsyncRandomAccessWriteDevice, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::offset_
```


###  buffers_

```c
asio::detail::consuming_buffers<const_buffer, ConstBufferSequence, ConstBufferIterator> asio::detail::write_at_op< AsyncRandomAccessWriteDevice, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::buffers_
```


###  start_

```c
int asio::detail::write_at_op< AsyncRandomAccessWriteDevice, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::start_
```


###  handler_

```c
WriteHandler asio::detail::write_at_op< AsyncRandomAccessWriteDevice, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::handler_
```


### write_at_op()



```c
asio::detail::write_at_op< AsyncRandomAccessWriteDevice, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::write_at_op(AsyncRandomAccessWriteDevice &device, uint64_t offset, const ConstBufferSequence &buffers, CompletionCondition completion_condition, WriteHandler &handler)
```

!!! summary "引数"
	- AsyncRandomAccessWriteDevice & `device` 
	- uint64_t `offset` 
	- constConstBufferSequence & `buffers` 
	- CompletionCondition `completion_condition` 
	- WriteHandler & `handler` 



### operator()()



```c
void asio::detail::write_at_op< AsyncRandomAccessWriteDevice, ConstBufferSequence, ConstBufferIterator, CompletionCondition, WriteHandler >::operator()(const asio::error_code &ec, std::size_t bytes_transferred, int start=0)
```

!!! summary "引数"
	- const& `ec` 
	- std::size_t `bytes_transferred` 
	- int `start` 



