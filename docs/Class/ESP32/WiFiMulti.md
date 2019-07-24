# WiFiMulti



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_wi_fi_multi.html)

## メンバー

### WiFiMulti()



```c
WiFiMulti::WiFiMulti()
```



### ~WiFiMulti()



```c
WiFiMulti::~WiFiMulti()
```



### addAP()



```c
bool WiFiMulti::addAP(const char *ssid, const char *passphrase=NULL)
```

!!! summary "引数"
	- constchar * `ssid` 
	- constchar * `passphrase` 

!!! note "戻り値"
	bool



### run()



```c
uint8_t WiFiMulti::run(uint32_t connectTimeout=5000)
```

!!! summary "引数"
	- uint32_t `connectTimeout` 

!!! note "戻り値"
	uint8_t



