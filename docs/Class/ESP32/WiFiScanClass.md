# WiFiScanClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_wi_fi_scan_class.html)

## メンバー

### scanNetworks()



```c
int16_t WiFiScanClass::scanNetworks(bool async=false, bool show_hidden=false, bool passive=false, uint32_t max_ms_per_chan=300)
```

!!! summary "引数"
	- bool `async` run in async mode 
	- bool `show_hidden` show hidden networks 
	- bool `passive` 
	- uint32_t `max_ms_per_chan` 

!!! note "戻り値"
	int16_t Number of discovered networks 



### scanComplete()


called to get the scan state in Async mode 

```c
int16_t WiFiScanClass::scanComplete()
```

!!! note "戻り値"
	int16_t scan result or status -1 if scan not fin -2 if scan not triggered 



### scanDelete()


delete last scan result from RAM 
```c
void WiFiScanClass::scanDelete()
```



### getNetworkInfo()



```c
bool WiFiScanClass::getNetworkInfo(uint8_t networkItem, String &ssid, uint8_t &encryptionType, int32_t &RSSI, uint8_t *&BSSID, int32_t &channel)
```

!!! summary "引数"
	- uint8_t `networkItem` uint8_t 
	- String & `ssid` const char** 
	- uint8_t& `encryptionType` uint8_t * 
	- int32_t& `RSSI` int32_t * 
	- uint8_t*& `BSSID` uint8_t ** 
	- int32_t& `channel` int32_t * 

!!! note "戻り値"
	bool (true if ok) 



### SSID()



```c
String WiFiScanClass::SSID(uint8_t networkItem)
```

!!! summary "引数"
	- uint8_t `networkItem` 

!!! note "戻り値"
	String ssid string of the specified item on the networks scanned list 



### encryptionType()



```c
wifi_auth_mode_t WiFiScanClass::encryptionType(uint8_t networkItem)
```

!!! summary "引数"
	- uint8_t `networkItem` 

!!! note "戻り値"
	wifi_auth_mode_t encryption type (enum wl_enc_type) of the specified item on the networks scanned list 



### RSSI()



```c
int32_t WiFiScanClass::RSSI(uint8_t networkItem)
```

!!! summary "引数"
	- uint8_t `networkItem` 

!!! note "戻り値"
	int32_t signed value of RSSI of the specified item on the networks scanned list 



### BSSID()



```c
uint8_t * WiFiScanClass::BSSID(uint8_t networkItem)
```

!!! summary "引数"
	- uint8_t `networkItem` 

!!! note "戻り値"
	uint8_t* uint8_t * MAC / BSSID of scanned wifi 



### BSSIDstr()



```c
String WiFiScanClass::BSSIDstr(uint8_t networkItem)
```

!!! summary "引数"
	- uint8_t `networkItem` 

!!! note "戻り値"
	String String MAC / BSSID of scanned wifi 



### channel()



```c
int32_t WiFiScanClass::channel(uint8_t networkItem)
```

!!! summary "引数"
	- uint8_t `networkItem` 

!!! note "戻り値"
	int32_t



### getScanInfoByIndex()



```c
static void* WiFiScanClass::getScanInfoByIndex(int i)
```

!!! summary "引数"
	- int `i` 

!!! note "戻り値"
	void *



### _scanDone()



```c
void WiFiScanClass::_scanDone()
```



