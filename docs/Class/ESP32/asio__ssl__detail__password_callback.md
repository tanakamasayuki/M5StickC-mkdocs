# asio::ssl::detail::password_callback



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1detail_1_1password__callback.html)

## メンバー

### password_callback()



```c
asio::ssl::detail::password_callback< PasswordCallback >::password_callback(PasswordCallback callback)
```

!!! summary "引数"
	- PasswordCallback `callback` 



### call()



```c
virtual std::string asio::ssl::detail::password_callback< PasswordCallback >::call(std::size_t size, context_base::password_purpose purpose)
```

!!! summary "引数"
	- std::size_t `size` 
	- context_base::password_purpose `purpose` 

!!! note "戻り値"
	std::string



