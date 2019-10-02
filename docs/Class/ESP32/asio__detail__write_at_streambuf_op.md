# asio::detail::write_at_streambuf_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1write__at__streambuf__op.html)

## メンバー

###  streambuf_

```c
asio::basic_streambuf<Allocator>& asio::detail::write_at_streambuf_op< Allocator, WriteHandler >::streambuf_
```


###  handler_

```c
WriteHandler asio::detail::write_at_streambuf_op< Allocator, WriteHandler >::handler_
```


### write_at_streambuf_op()



```c
asio::detail::write_at_streambuf_op< Allocator, WriteHandler >::write_at_streambuf_op(asio::basic_streambuf< Allocator > &streambuf, WriteHandler &handler)
```

!!! summary "引数"
	- asio::basic_streambuf< Allocator > & `streambuf` 
	- WriteHandler & `handler` 



### operator()()



```c
void asio::detail::write_at_streambuf_op< Allocator, WriteHandler >::operator()(const asio::error_code &ec, const std::size_t bytes_transferred)
```

!!! summary "引数"
	- const& `ec` 
	- conststd::size_t `bytes_transferred` 



