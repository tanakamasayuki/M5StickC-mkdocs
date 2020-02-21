# asio::ssl::rfc2818_verification



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1rfc2818__verification.html)

## メンバー



### rfc2818_verification()
Constructor.


```c
asio::ssl::rfc2818_verification::rfc2818_verification(const std::string &host)
```

!!! summary "引数"
	- const& `host` 



### operator()()
Perform certificate verification.


```c
ASIO_DECL bool asio::ssl::rfc2818_verification::operator()(bool preverified, verify_context &ctx) const
```

!!! summary "引数"
	- bool `preverified` 
	- verify_context& `ctx` 

!!! note "戻り値"
	ASIO_DECL



