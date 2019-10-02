# TransportTraits



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_transport_traits.html)

## メンバー

### ~TransportTraits()



```c
virtual TransportTraits::~TransportTraits()
```



### create()



```c
virtual std::unique_ptr<WiFiClient> TransportTraits::create()
```

!!! note "戻り値"
	WiFiClientstd::unique_ptr<  >



### verify()



```c
virtual bool TransportTraits::verify(WiFiClient &client, const char *host)
```

!!! summary "引数"
	- WiFiClient& `client` 
	- constchar * `host` 

!!! note "戻り値"
	bool



