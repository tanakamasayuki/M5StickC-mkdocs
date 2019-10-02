# WiFiClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_wi_fi_class.html)

## メンバー







### printDiag()



```c
void WiFiClass::printDiag(Print &dest)
```

!!! summary "引数"
	- Print& `dest` 



### channel()


Return the current channel associated with the network 

```c
int32_t WiFiGenericClass::channel(void)
```

!!! note "戻り値"
	int32_t channel (1-13) 



### SSID()


Return the current SSID associated with the network 

```c
String WiFiSTAClass::SSID() const
```

!!! note "戻り値"
	String SSID 



### RSSI()


Return the current network RSSI. 

```c
int8_t WiFiSTAClass::RSSI()
```

!!! note "戻り値"
	int8_t RSSI value 



### BSSID()


Return the current bssid / mac associated with the network if configured 

```c
uint8_t * WiFiSTAClass::BSSID()
```

!!! note "戻り値"
	uint8_t* bssid uint8_t * 



### BSSIDstr()


Return the current bssid / mac associated with the network if configured 

```c
String WiFiSTAClass::BSSIDstr()
```

!!! note "戻り値"
	String String bssid mac 



### SSID()



```c
String WiFiScanClass::SSID(uint8_t networkItem)
```

!!! note "戻り値"
	String ssid string of the specified item on the networks scanned list 



### encryptionType()



```c
wifi_auth_mode_t WiFiScanClass::encryptionType(uint8_t networkItem)
```

!!! note "戻り値"
	wifi_auth_mode_t encryption type (enum wl_enc_type) of the specified item on the networks scanned list 



### RSSI()



```c
int32_t WiFiScanClass::RSSI(uint8_t networkItem)
```

!!! note "戻り値"
	int32_t signed value of RSSI of the specified item on the networks scanned list 



### BSSID()



```c
uint8_t * WiFiScanClass::BSSID(uint8_t networkItem)
```

!!! note "戻り値"
	uint8_t* uint8_t * MAC / BSSID of scanned wifi 



### BSSIDstr()



```c
String WiFiScanClass::BSSIDstr(uint8_t networkItem)
```

!!! note "戻り値"
	String String MAC / BSSID of scanned wifi 



### channel()



```c
int32_t WiFiScanClass::channel(uint8_t networkItem)
```

!!! note "戻り値"
	int32_t



