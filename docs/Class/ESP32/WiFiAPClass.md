# WiFiAPClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_wi_fi_a_p_class.html)

## メンバー

### softAP()



```c
bool WiFiAPClass::softAP(const char *ssid, const char *passphrase=NULL, int channel=1, int ssid_hidden=0, int max_connection=4)
```

!!! summary "引数"
	- constchar * `ssid` Pointer to the SSID (max 63 char). 
	- constchar * `passphrase` (for WPA2 min 8 char, for open use NULL) 
	- int `channel` WiFi channel number, 1 - 13. 
	- int `ssid_hidden` Network cloaking (0 = broadcast SSID, 1 = hide SSID) 
	- int `max_connection` Max simultaneous connected clients, 1 - 4. 

!!! note "戻り値"
	bool



### softAPConfig()



```c
bool WiFiAPClass::softAPConfig(IPAddress local_ip, IPAddress gateway, IPAddress subnet)
```

!!! summary "引数"
	- IPAddress `local_ip` access point IP 
	- IPAddress `gateway` gateway IP 
	- IPAddress `subnet` subnet mask 

!!! note "戻り値"
	bool



### softAPdisconnect()



```c
bool WiFiAPClass::softAPdisconnect(bool wifioff=false)
```

!!! summary "引数"
	- bool `wifioff` disable mode? 

!!! note "戻り値"
	bool one value of wl_status_t enum 



### softAPgetStationNum()


Get the count of the Station / client that are connected to the softAP interface 

```c
uint8_t WiFiAPClass::softAPgetStationNum()
```

!!! note "戻り値"
	uint8_t Stations count 



### softAPIP()


Get the softAP interface IP address. 

```c
IPAddress WiFiAPClass::softAPIP()
```

!!! note "戻り値"
	IPAddress  softAP IP 



### softAPBroadcastIP()


Get the softAP broadcast IP address. 

```c
IPAddress WiFiAPClass::softAPBroadcastIP()
```

!!! note "戻り値"
	IPAddress  softAP broadcastIP 



### softAPNetworkID()


Get the softAP network ID. 

```c
IPAddress WiFiAPClass::softAPNetworkID()
```

!!! note "戻り値"
	IPAddress  softAP networkID 



### softAPSubnetCIDR()


Get the softAP subnet CIDR. 

```c
uint8_t WiFiAPClass::softAPSubnetCIDR()
```

!!! note "戻り値"
	uint8_t uint8_t softAP subnetCIDR 



### softAPenableIpV6()


Enable IPv6 on the softAP interface. 

```c
bool WiFiAPClass::softAPenableIpV6()
```

!!! note "戻り値"
	bool true on success 



### softAPIPv6()


Get the softAP interface IPv6 address. 

```c
IPv6Address WiFiAPClass::softAPIPv6()
```

!!! note "戻り値"
	IPv6Address  softAP IPv6 



### softAPgetHostname()


Get the softAP interface Host name. 

```c
const char * WiFiAPClass::softAPgetHostname()
```

!!! note "戻り値"
	constchar * char array hostname 



### softAPsetHostname()



```c
bool WiFiAPClass::softAPsetHostname(const char *hostname)
```

!!! summary "引数"
	- constchar * `hostname` pointer to const string 

!!! note "戻り値"
	bool true on success 



### softAPmacAddress()



```c
uint8_t * WiFiAPClass::softAPmacAddress(uint8_t *mac)
```

!!! summary "引数"
	- uint8_t* `mac` pointer to uint8_t array with length WL_MAC_ADDR_LENGTH 

!!! note "戻り値"
	uint8_t* pointer to uint8_t* 



### softAPmacAddress()


Get the softAP interface MAC address. 

```c
String WiFiAPClass::softAPmacAddress(void)
```

!!! note "戻り値"
	String String mac 



