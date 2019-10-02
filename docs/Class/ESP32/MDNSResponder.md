# MDNSResponder



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_m_d_n_s_responder.html)

## メンバー

### MDNSResponder()



```c
MDNSResponder::MDNSResponder()
```



### ~MDNSResponder()



```c
MDNSResponder::~MDNSResponder()
```



### begin()



```c
bool MDNSResponder::begin(const char *hostName)
```

!!! summary "引数"
	- constchar * `hostName` 

!!! note "戻り値"
	bool



### end()



```c
void MDNSResponder::end()
```



### setInstanceName()



```c
void MDNSResponder::setInstanceName(String name)
```

!!! summary "引数"
	- String `name` 



### setInstanceName()



```c
void MDNSResponder::setInstanceName(const char *name)
```

!!! summary "引数"
	- constchar * `name` 



### setInstanceName()



```c
void MDNSResponder::setInstanceName(char *name)
```

!!! summary "引数"
	- char * `name` 



### addService()



```c
void MDNSResponder::addService(char *service, char *proto, uint16_t port)
```

!!! summary "引数"
	- char * `service` 
	- char * `proto` 
	- uint16_t `port` 



### addService()



```c
void MDNSResponder::addService(const char *service, const char *proto, uint16_t port)
```

!!! summary "引数"
	- constchar * `service` 
	- constchar * `proto` 
	- uint16_t `port` 



### addService()



```c
void MDNSResponder::addService(String service, String proto, uint16_t port)
```

!!! summary "引数"
	- String `service` 
	- String `proto` 
	- uint16_t `port` 



### addServiceTxt()



```c
bool MDNSResponder::addServiceTxt(char *name, char *proto, char *key, char *value)
```

!!! summary "引数"
	- char * `name` 
	- char * `proto` 
	- char * `key` 
	- char * `value` 

!!! note "戻り値"
	bool



### addServiceTxt()



```c
void MDNSResponder::addServiceTxt(const char *name, const char *proto, const char *key, const char *value)
```

!!! summary "引数"
	- constchar * `name` 
	- constchar * `proto` 
	- constchar * `key` 
	- constchar * `value` 



### addServiceTxt()



```c
void MDNSResponder::addServiceTxt(String name, String proto, String key, String value)
```

!!! summary "引数"
	- String `name` 
	- String `proto` 
	- String `key` 
	- String `value` 



### enableArduino()



```c
void MDNSResponder::enableArduino(uint16_t port=3232, bool auth=false)
```

!!! summary "引数"
	- uint16_t `port` 
	- bool `auth` 



### disableArduino()



```c
void MDNSResponder::disableArduino()
```



### enableWorkstation()



```c
void MDNSResponder::enableWorkstation(wifi_interface_t interface=ESP_IF_WIFI_STA)
```

!!! summary "引数"
	- wifi_interface_t `interface` 



### disableWorkstation()



```c
void MDNSResponder::disableWorkstation()
```



### queryHost()



```c
IPAddress MDNSResponder::queryHost(char *host, uint32_t timeout=2000)
```

!!! summary "引数"
	- char * `host` 
	- uint32_t `timeout` 

!!! note "戻り値"
	IPAddress



### queryHost()



```c
IPAddress MDNSResponder::queryHost(const char *host, uint32_t timeout=2000)
```

!!! summary "引数"
	- constchar * `host` 
	- uint32_t `timeout` 

!!! note "戻り値"
	IPAddress



### queryHost()



```c
IPAddress MDNSResponder::queryHost(String host, uint32_t timeout=2000)
```

!!! summary "引数"
	- String `host` 
	- uint32_t `timeout` 

!!! note "戻り値"
	IPAddress



### queryService()



```c
int MDNSResponder::queryService(char *service, char *proto)
```

!!! summary "引数"
	- char * `service` 
	- char * `proto` 

!!! note "戻り値"
	int



### queryService()



```c
int MDNSResponder::queryService(const char *service, const char *proto)
```

!!! summary "引数"
	- constchar * `service` 
	- constchar * `proto` 

!!! note "戻り値"
	int



### queryService()



```c
int MDNSResponder::queryService(String service, String proto)
```

!!! summary "引数"
	- String `service` 
	- String `proto` 

!!! note "戻り値"
	int



### hostname()



```c
String MDNSResponder::hostname(int idx)
```

!!! summary "引数"
	- int `idx` 

!!! note "戻り値"
	String



### IP()



```c
IPAddress MDNSResponder::IP(int idx)
```

!!! summary "引数"
	- int `idx` 

!!! note "戻り値"
	IPAddress



### IPv6()



```c
IPv6Address MDNSResponder::IPv6(int idx)
```

!!! summary "引数"
	- int `idx` 

!!! note "戻り値"
	IPv6Address



### port()



```c
uint16_t MDNSResponder::port(int idx)
```

!!! summary "引数"
	- int `idx` 

!!! note "戻り値"
	uint16_t



### numTxt()



```c
int MDNSResponder::numTxt(int idx)
```

!!! summary "引数"
	- int `idx` 

!!! note "戻り値"
	int



### hasTxt()



```c
bool MDNSResponder::hasTxt(int idx, const char *key)
```

!!! summary "引数"
	- int `idx` 
	- constchar * `key` 

!!! note "戻り値"
	bool



### txt()



```c
String MDNSResponder::txt(int idx, const char *key)
```

!!! summary "引数"
	- int `idx` 
	- constchar * `key` 

!!! note "戻り値"
	String



### txt()



```c
String MDNSResponder::txt(int idx, int txtIdx)
```

!!! summary "引数"
	- int `idx` 
	- int `txtIdx` 

!!! note "戻り値"
	String



