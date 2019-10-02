# HTTPUpdate



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_h_t_t_p_update.html)

## メンバー

### HTTPUpdate()



```c
HTTPUpdate::HTTPUpdate(void)
```



### HTTPUpdate()



```c
HTTPUpdate::HTTPUpdate(int httpClientTimeout)
```

!!! summary "引数"
	- int `httpClientTimeout` 



### ~HTTPUpdate()



```c
HTTPUpdate::~HTTPUpdate(void)
```



### rebootOnUpdate()



```c
void HTTPUpdate::rebootOnUpdate(bool reboot)
```

!!! summary "引数"
	- bool `reboot` 



### setLedPin()



```c
void HTTPUpdate::setLedPin(int ledPin=-1, uint8_t ledOn=HIGH)
```

!!! summary "引数"
	- int `ledPin` 
	- uint8_t `ledOn` 



### update()



```c
HTTPUpdateResult HTTPUpdate::update(WiFiClient &client, const String &url, const String &currentVersion="")
```

!!! summary "引数"
	- WiFiClient& `client` 
	- constString & `url` 
	- constString & `currentVersion` 

!!! note "戻り値"
	t_httpUpdate_return



### update()



```c
HTTPUpdateResult HTTPUpdate::update(WiFiClient &client, const String &host, uint16_t port, const String &uri="/", const String &currentVersion="")
```

!!! summary "引数"
	- WiFiClient& `client` 
	- constString & `host` 
	- uint16_t `port` 
	- constString & `uri` 
	- constString & `currentVersion` 

!!! note "戻り値"
	t_httpUpdate_return



### updateSpiffs()



```c
HTTPUpdateResult HTTPUpdate::updateSpiffs(WiFiClient &client, const String &url, const String &currentVersion="")
```

!!! summary "引数"
	- WiFiClient& `client` 
	- constString & `url` 
	- constString & `currentVersion` 

!!! note "戻り値"
	t_httpUpdate_return



### getLastError()


return error code as int 

```c
int HTTPUpdate::getLastError(void)
```

!!! note "戻り値"
	int int error code 



### getLastErrorString()


return error code as String 

```c
String HTTPUpdate::getLastErrorString(void)
```

!!! note "戻り値"
	String String error 



