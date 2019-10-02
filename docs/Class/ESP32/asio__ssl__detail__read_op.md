# asio::ssl::detail::read_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1detail_1_1read__op.html)

## メンバー

### read_op()



```c
asio::ssl::detail::read_op< MutableBufferSequence >::read_op(const MutableBufferSequence &buffers)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` 



### operator()()



```c
engine::want asio::ssl::detail::read_op< MutableBufferSequence >::operator()(engine &eng, asio::error_code &ec, std::size_t &bytes_transferred) const
```

!!! summary "引数"
	- engine& `eng` 
	- asio::error_code& `ec` 
	- std::size_t & `bytes_transferred` 

!!! note "戻り値"
	engine::want



### call_handler()



```c
void asio::ssl::detail::read_op< MutableBufferSequence >::call_handler(Handler &handler, const asio::error_code &ec, const std::size_t &bytes_transferred) const
```

!!! summary "引数"
	- Handler & `handler` 
	- const& `ec` 
	- conststd::size_t & `bytes_transferred` 



