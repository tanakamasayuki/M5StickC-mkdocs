# asio::ssl::detail::buffered_handshake_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1detail_1_1buffered__handshake__op.html)

## メンバー

### buffered_handshake_op()



```c
asio::ssl::detail::buffered_handshake_op< ConstBufferSequence >::buffered_handshake_op(stream_base::handshake_type type, const ConstBufferSequence &buffers)
```

!!! summary "引数"
	- stream_base::handshake_type `type` 
	- constConstBufferSequence & `buffers` 



### operator()()



```c
engine::want asio::ssl::detail::buffered_handshake_op< ConstBufferSequence >::operator()(engine &eng, asio::error_code &ec, std::size_t &bytes_transferred) const
```

!!! summary "引数"
	- engine& `eng` 
	- asio::error_code& `ec` 
	- std::size_t & `bytes_transferred` 

!!! note "戻り値"
	engine::want



### call_handler()



```c
void asio::ssl::detail::buffered_handshake_op< ConstBufferSequence >::call_handler(Handler &handler, const asio::error_code &ec, const std::size_t &bytes_transferred) const
```

!!! summary "引数"
	- Handler & `handler` 
	- const& `ec` 
	- conststd::size_t & `bytes_transferred` 



