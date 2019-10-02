# asio::detail::read_at_streambuf_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1read__at__streambuf__op.html)

## メンバー

###  device_

```c
AsyncRandomAccessReadDevice& asio::detail::read_at_streambuf_op< AsyncRandomAccessReadDevice, Allocator, CompletionCondition, ReadHandler >::device_
```


###  offset_

```c
uint64_t asio::detail::read_at_streambuf_op< AsyncRandomAccessReadDevice, Allocator, CompletionCondition, ReadHandler >::offset_
```


###  streambuf_

```c
asio::basic_streambuf<Allocator>& asio::detail::read_at_streambuf_op< AsyncRandomAccessReadDevice, Allocator, CompletionCondition, ReadHandler >::streambuf_
```


###  start_

```c
int asio::detail::read_at_streambuf_op< AsyncRandomAccessReadDevice, Allocator, CompletionCondition, ReadHandler >::start_
```


###  total_transferred_

```c
std::size_t asio::detail::read_at_streambuf_op< AsyncRandomAccessReadDevice, Allocator, CompletionCondition, ReadHandler >::total_transferred_
```


###  handler_

```c
ReadHandler asio::detail::read_at_streambuf_op< AsyncRandomAccessReadDevice, Allocator, CompletionCondition, ReadHandler >::handler_
```


### read_at_streambuf_op()



```c
asio::detail::read_at_streambuf_op< AsyncRandomAccessReadDevice, Allocator, CompletionCondition, ReadHandler >::read_at_streambuf_op(AsyncRandomAccessReadDevice &device, uint64_t offset, basic_streambuf< Allocator > &streambuf, CompletionCondition completion_condition, ReadHandler &handler)
```

!!! summary "引数"
	- AsyncRandomAccessReadDevice & `device` 
	- uint64_t `offset` 
	- basic_streambuf< Allocator > & `streambuf` 
	- CompletionCondition `completion_condition` 
	- ReadHandler & `handler` 



### operator()()



```c
void asio::detail::read_at_streambuf_op< AsyncRandomAccessReadDevice, Allocator, CompletionCondition, ReadHandler >::operator()(const asio::error_code &ec, std::size_t bytes_transferred, int start=0)
```

!!! summary "引数"
	- const& `ec` 
	- std::size_t `bytes_transferred` 
	- int `start` 



