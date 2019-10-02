# WiFiClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_wi_fi_class.html)

## メンバー

###  _state

```c
int16_t WiFiClass::_state
```


###  _server_port

```c
uint16_t WiFiClass::_server_port
```






### WiFiClass()



```c
WiFiClass::WiFiClass()
```



### begin()



```c
int WiFiClass::begin(char *ssid)
```

!!! summary "引数"
	- char * `ssid` 

!!! note "戻り値"
	int



### begin()



```c
int WiFiClass::begin(char *ssid, uint8_t key_idx, const char *key)
```

!!! summary "引数"
	- char * `ssid` 
	- uint8_t `key_idx` 
	- constchar * `key` 

!!! note "戻り値"
	int



### begin()



```c
int WiFiClass::begin(char *ssid, const char *passphrase)
```

!!! summary "引数"
	- char * `ssid` 
	- constchar * `passphrase` 

!!! note "戻り値"
	int



### config()



```c
void WiFiClass::config(IPAddress local_ip)
```

!!! summary "引数"
	- IPAddress `local_ip` 



### config()



```c
void WiFiClass::config(IPAddress local_ip, IPAddress dns_server)
```

!!! summary "引数"
	- IPAddress `local_ip` 
	- IPAddress `dns_server` 



### config()



```c
void WiFiClass::config(IPAddress local_ip, IPAddress dns_server, IPAddress gateway)
```

!!! summary "引数"
	- IPAddress `local_ip` 
	- IPAddress `dns_server` 
	- IPAddress `gateway` 



### config()



```c
void WiFiClass::config(IPAddress local_ip, IPAddress dns_server, IPAddress gateway, IPAddress subnet)
```

!!! summary "引数"
	- IPAddress `local_ip` 
	- IPAddress `dns_server` 
	- IPAddress `gateway` 
	- IPAddress `subnet` 



### setDNS()



```c
void WiFiClass::setDNS(IPAddress dns_server1)
```

!!! summary "引数"
	- IPAddress `dns_server1` 



### setDNS()



```c
void WiFiClass::setDNS(IPAddress dns_server1, IPAddress dns_server2)
```

!!! summary "引数"
	- IPAddress `dns_server1` 
	- IPAddress `dns_server2` 



### disconnect()



```c
int WiFiClass::disconnect(void)
```

!!! note "戻り値"
	int



### macAddress()



```c
uint8_t * WiFiClass::macAddress(uint8_t *mac)
```

!!! summary "引数"
	- uint8_t * `mac` 

!!! note "戻り値"
	uint8_t *



### localIP()



```c
IPAddress WiFiClass::localIP()
```

!!! note "戻り値"
	IPAddress



### subnetMask()



```c
IPAddress WiFiClass::subnetMask()
```

!!! note "戻り値"
	IPAddress



### gatewayIP()



```c
IPAddress WiFiClass::gatewayIP()
```

!!! note "戻り値"
	IPAddress



### SSID()



```c
char * WiFiClass::SSID()
```

!!! note "戻り値"
	char *



### BSSID()



```c
uint8_t * WiFiClass::BSSID(uint8_t *bssid)
```

!!! summary "引数"
	- uint8_t * `bssid` 

!!! note "戻り値"
	uint8_t *



### RSSI()



```c
int32_t WiFiClass::RSSI()
```

!!! note "戻り値"
	int32_t



### encryptionType()



```c
uint8_t WiFiClass::encryptionType()
```

!!! note "戻り値"
	uint8_t



### scanNetworks()



```c
int8_t WiFiClass::scanNetworks()
```

!!! note "戻り値"
	int8_t



### SSID()



```c
char * WiFiClass::SSID(uint8_t networkItem)
```

!!! summary "引数"
	- uint8_t `networkItem` 

!!! note "戻り値"
	char *



### encryptionType()



```c
uint8_t WiFiClass::encryptionType(uint8_t networkItem)
```

!!! summary "引数"
	- uint8_t `networkItem` 

!!! note "戻り値"
	uint8_t



### RSSI()



```c
int32_t WiFiClass::RSSI(uint8_t networkItem)
```

!!! summary "引数"
	- uint8_t `networkItem` 

!!! note "戻り値"
	int32_t



### status()



```c
uint8_t WiFiClass::status()
```

!!! note "戻り値"
	uint8_t



### hostByName()



```c
int WiFiClass::hostByName(const char *aHostname, IPAddress &aResult)
```

!!! summary "引数"
	- constchar * `aHostname` 
	- IPAddress& `aResult` 

!!! note "戻り値"
	int



### getSocket()



```c
uint8_t WiFiClass::getSocket()
```

!!! note "戻り値"
	uint8_t



### firmwareVersion()



```c
char * WiFiClass::firmwareVersion()
```

!!! note "戻り値"
	char *



