# TLSTraits



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_t_l_s_traits.html)

## メンバー

### TLSTraits()



```c
TLSTraits::TLSTraits(const char *CAcert, const char *clicert=nullptr, const char *clikey=nullptr)
```

!!! summary "引数"
	- constchar * `CAcert` 
	- constchar * `clicert` 
	- constchar * `clikey` 



### create()



```c
std::unique_ptr<WiFiClient> TLSTraits::create() override
```

!!! note "戻り値"
	WiFiClientstd::unique_ptr<  >



### verify()



```c
bool TLSTraits::verify(WiFiClient &client, const char *host) override
```

!!! summary "引数"
	- WiFiClient& `client` 
	- constchar * `host` 

!!! note "戻り値"
	bool



