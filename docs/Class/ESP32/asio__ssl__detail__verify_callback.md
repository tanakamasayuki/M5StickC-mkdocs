# asio::ssl::detail::verify_callback



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1detail_1_1verify__callback.html)

## メンバー

### verify_callback()



```c
asio::ssl::detail::verify_callback< VerifyCallback >::verify_callback(VerifyCallback callback)
```

!!! summary "引数"
	- VerifyCallback `callback` 



### call()



```c
virtual bool asio::ssl::detail::verify_callback< VerifyCallback >::call(bool preverified, verify_context &ctx)
```

!!! summary "引数"
	- bool `preverified` 
	- verify_context& `ctx` 

!!! note "戻り値"
	bool



