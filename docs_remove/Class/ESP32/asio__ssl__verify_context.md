# asio::ssl::verify_context



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1verify__context.html)

## メンバー



### verify_context()
Constructor.


```c
asio::ssl::verify_context::verify_context(native_handle_type handle)
```

!!! summary "引数"
	- native_handle_type `handle` 



### native_handle()
Get the underlying implementation in the native type.

This function may be used to obtain the underlying implementation of the context. This is intended to allow access to context functionality that is not otherwise provided. 
```c
native_handle_type asio::ssl::verify_context::native_handle()
```

!!! note "戻り値"
	native_handle_type



