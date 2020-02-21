# asio::ssl::detail::verify_callback_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1detail_1_1verify__callback__base.html)

## メンバー

### ~verify_callback_base()



```c
virtual asio::ssl::detail::verify_callback_base::~verify_callback_base()
```



### call()



```c
virtual bool asio::ssl::detail::verify_callback_base::call(bool preverified, verify_context &ctx)=0
```

!!! summary "引数"
	- bool `preverified` 
	- verify_context& `ctx` 

!!! note "戻り値"
	bool



