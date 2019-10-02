# asio::ssl::detail::write_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1detail_1_1write__op.html)

## メンバー

### write_op()



```c
asio::ssl::detail::write_op< ConstBufferSequence >::write_op(const ConstBufferSequence &buffers)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` 



### operator()()



```c
engine::want asio::ssl::detail::write_op< ConstBufferSequence >::operator()(engine &eng, asio::error_code &ec, std::size_t &bytes_transferred) const
```

!!! summary "引数"
	- engine& `eng` 
	- asio::error_code& `ec` 
	- std::size_t & `bytes_transferred` 

!!! note "戻り値"
	engine::want



### call_handler()



```c
void asio::ssl::detail::write_op< ConstBufferSequence >::call_handler(Handler &handler, const asio::error_code &ec, const std::size_t &bytes_transferred) const
```

!!! summary "引数"
	- Handler & `handler` 
	- const& `ec` 
	- conststd::size_t & `bytes_transferred` 



