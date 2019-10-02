# asio::ssl::detail::password_callback_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1detail_1_1password__callback__base.html)

## メンバー

### ~password_callback_base()



```c
virtual asio::ssl::detail::password_callback_base::~password_callback_base()
```



### call()



```c
virtual std::string asio::ssl::detail::password_callback_base::call(std::size_t size, context_base::password_purpose purpose)=0
```

!!! summary "引数"
	- std::size_t `size` 
	- context_base::password_purpose `purpose` 

!!! note "戻り値"
	std::string



