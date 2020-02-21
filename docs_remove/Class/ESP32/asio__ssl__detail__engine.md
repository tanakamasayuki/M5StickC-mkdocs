# asio::ssl::detail::engine



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1detail_1_1engine.html)

## メンバー



### engine()



```c
ASIO_DECL asio::ssl::detail::engine::engine(SSL_CTX *context)
```

!!! summary "引数"
	- SSL_CTX* `context` 

!!! note "戻り値"
	ASIO_DECL



### ~engine()



```c
ASIO_DECL asio::ssl::detail::engine::~engine()
```

!!! note "戻り値"
	ASIO_DECL



### native_handle()



```c
ASIO_DECL SSL* asio::ssl::detail::engine::native_handle()
```

!!! note "戻り値"
	ASIO_DECL*



### set_verify_mode()



```c
ASIO_DECL asio::error_code asio::ssl::detail::engine::set_verify_mode(verify_mode v, asio::error_code &ec)
```

!!! summary "引数"
	- verify_mode `v` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### set_verify_depth()



```c
ASIO_DECL asio::error_code asio::ssl::detail::engine::set_verify_depth(int depth, asio::error_code &ec)
```

!!! summary "引数"
	- int `depth` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### set_verify_callback()



```c
ASIO_DECL asio::error_code asio::ssl::detail::engine::set_verify_callback(verify_callback_base *callback, asio::error_code &ec)
```

!!! summary "引数"
	- verify_callback_base* `callback` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### handshake()



```c
ASIO_DECL want asio::ssl::detail::engine::handshake(stream_base::handshake_type type, asio::error_code &ec)
```

!!! summary "引数"
	- stream_base::handshake_type `type` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### shutdown()



```c
ASIO_DECL want asio::ssl::detail::engine::shutdown(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### write()



```c
ASIO_DECL want asio::ssl::detail::engine::write(const asio::const_buffer &data, asio::error_code &ec, std::size_t &bytes_transferred)
```

!!! summary "引数"
	- const& `data` 
	- asio::error_code& `ec` 
	- std::size_t & `bytes_transferred` 

!!! note "戻り値"
	ASIO_DECL



### read()



```c
ASIO_DECL want asio::ssl::detail::engine::read(const asio::mutable_buffer &data, asio::error_code &ec, std::size_t &bytes_transferred)
```

!!! summary "引数"
	- const& `data` 
	- asio::error_code& `ec` 
	- std::size_t & `bytes_transferred` 

!!! note "戻り値"
	ASIO_DECL



### get_output()



```c
ASIO_DECL asio::mutable_buffer asio::ssl::detail::engine::get_output(const asio::mutable_buffer &data)
```

!!! summary "引数"
	- const& `data` 

!!! note "戻り値"
	ASIO_DECL



### put_input()



```c
ASIO_DECL asio::const_buffer asio::ssl::detail::engine::put_input(const asio::const_buffer &data)
```

!!! summary "引数"
	- const& `data` 

!!! note "戻り値"
	ASIO_DECL



### map_error_code()



```c
ASIO_DECL const asio::error_code& asio::ssl::detail::engine::map_error_code(asio::error_code &ec) const
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL&



