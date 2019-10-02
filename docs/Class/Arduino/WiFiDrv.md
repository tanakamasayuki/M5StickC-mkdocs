# WiFiDrv



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_wi_fi_drv.html)

## メンバー



### wifiDriverInit()



```c
void WiFiDrv::wifiDriverInit()
```



### wifiSetNetwork()



```c
int8_t WiFiDrv::wifiSetNetwork(char *ssid, uint8_t ssid_len)
```

!!! summary "引数"
	- char * `ssid` 
	- uint8_t `ssid_len` 

!!! note "戻り値"
	int8_t



### wifiSetPassphrase()



```c
int8_t WiFiDrv::wifiSetPassphrase(char *ssid, uint8_t ssid_len, const char *passphrase, const uint8_t len)
```

!!! summary "引数"
	- char * `ssid` 
	- uint8_t `ssid_len` 
	- constchar * `passphrase` 
	- constuint8_t `len` 

!!! note "戻り値"
	int8_t



### wifiSetKey()



```c
int8_t WiFiDrv::wifiSetKey(char *ssid, uint8_t ssid_len, uint8_t key_idx, const void *key, const uint8_t len)
```

!!! summary "引数"
	- char * `ssid` 
	- uint8_t `ssid_len` 
	- uint8_t `key_idx` 
	- constvoid * `key` 
	- constuint8_t `len` 

!!! note "戻り値"
	int8_t



### config()



```c
void WiFiDrv::config(uint8_t validParams, uint32_t local_ip, uint32_t gateway, uint32_t subnet)
```

!!! summary "引数"
	- uint8_t `validParams` 
	- uint32_t `local_ip` 
	- uint32_t `gateway` 
	- uint32_t `subnet` 



### setDNS()



```c
void WiFiDrv::setDNS(uint8_t validParams, uint32_t dns_server1, uint32_t dns_server2)
```

!!! summary "引数"
	- uint8_t `validParams` 
	- uint32_t `dns_server1` 
	- uint32_t `dns_server2` 



### disconnect()



```c
int8_t WiFiDrv::disconnect()
```

!!! note "戻り値"
	int8_t



### getConnectionStatus()



```c
uint8_t WiFiDrv::getConnectionStatus()
```

!!! note "戻り値"
	uint8_t



### getMacAddress()



```c
uint8_t * WiFiDrv::getMacAddress()
```

!!! note "戻り値"
	uint8_t *



### getIpAddress()



```c
void WiFiDrv::getIpAddress(IPAddress &ip)
```

!!! summary "引数"
	- IPAddress& `ip` 



### getSubnetMask()



```c
void WiFiDrv::getSubnetMask(IPAddress &mask)
```

!!! summary "引数"
	- IPAddress& `mask` 



### getGatewayIP()



```c
void WiFiDrv::getGatewayIP(IPAddress &ip)
```

!!! summary "引数"
	- IPAddress& `ip` 



### getCurrentSSID()



```c
char * WiFiDrv::getCurrentSSID()
```

!!! note "戻り値"
	char *



### getCurrentBSSID()



```c
uint8_t * WiFiDrv::getCurrentBSSID()
```

!!! note "戻り値"
	uint8_t *



### getCurrentRSSI()



```c
int32_t WiFiDrv::getCurrentRSSI()
```

!!! note "戻り値"
	int32_t



### getCurrentEncryptionType()



```c
uint8_t WiFiDrv::getCurrentEncryptionType()
```

!!! note "戻り値"
	uint8_t



### startScanNetworks()



```c
int8_t WiFiDrv::startScanNetworks()
```

!!! note "戻り値"
	int8_t



### getScanNetworks()



```c
uint8_t WiFiDrv::getScanNetworks()
```

!!! note "戻り値"
	uint8_t



### getSSIDNetoworks()



```c
char * WiFiDrv::getSSIDNetoworks(uint8_t networkItem)
```

!!! summary "引数"
	- uint8_t `networkItem` 

!!! note "戻り値"
	char *



### getRSSINetoworks()



```c
int32_t WiFiDrv::getRSSINetoworks(uint8_t networkItem)
```

!!! summary "引数"
	- uint8_t `networkItem` 

!!! note "戻り値"
	int32_t



### getEncTypeNetowrks()



```c
uint8_t WiFiDrv::getEncTypeNetowrks(uint8_t networkItem)
```

!!! summary "引数"
	- uint8_t `networkItem` 

!!! note "戻り値"
	uint8_t



### getHostByName()



```c
int WiFiDrv::getHostByName(const char *aHostname, IPAddress &aResult)
```

!!! summary "引数"
	- constchar * `aHostname` 
	- IPAddress& `aResult` 

!!! note "戻り値"
	int



### getFwVersion()



```c
char * WiFiDrv::getFwVersion()
```

!!! note "戻り値"
	char *



