# WiFiSTAClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_wi_fi_s_t_a_class.html)

## メンバー

### begin()



```c
wl_status_t WiFiSTAClass::begin(const char *ssid, const char *passphrase=NULL, int32_t channel=0, const uint8_t *bssid=NULL, bool connect=true)
```

!!! summary "引数"
	- constchar * `ssid` const char* Pointer to the SSID string. 
	- constchar * `passphrase` const char * Optional. Passphrase. Valid characters in a passphrase must be between ASCII 32-126 (decimal). 
	- int32_t `channel` Optional. Channel of AP 
	- const* `bssid` uint8_t[6] Optional. BSSID / MAC of AP 
	- bool `connect` Optional. call connect 

!!! note "戻り値"
	wl_status_t 



### begin()



```c
wl_status_t WiFiSTAClass::begin(char *ssid, char *passphrase=NULL, int32_t channel=0, const uint8_t *bssid=NULL, bool connect=true)
```

!!! summary "引数"
	- char * `ssid` 
	- char * `passphrase` 
	- int32_t `channel` 
	- const* `bssid` 
	- bool `connect` 

!!! note "戻り値"
	wl_status_t



### begin()


Use to connect to SDK config. 

```c
wl_status_t WiFiSTAClass::begin()
```

!!! note "戻り値"
	wl_status_t wl_status_t 



### config()



```c
bool WiFiSTAClass::config(IPAddress local_ip, IPAddress gateway, IPAddress subnet, IPAddress dns1=(uint32_t) 0x00000000, IPAddress dns2=(uint32_t) 0x00000000)
```

!!! summary "引数"
	- IPAddress `local_ip` Static ip configuration 
	- IPAddress `gateway` Static gateway configuration 
	- IPAddress `subnet` Static Subnet mask 
	- IPAddress `dns1` Static DNS server 1 
	- IPAddress `dns2` Static DNS server 2 

!!! note "戻り値"
	bool



### reconnect()


will force a disconnect an then start reconnecting to AP 

```c
bool WiFiSTAClass::reconnect()
```

!!! note "戻り値"
	bool ok 



### disconnect()



```c
bool WiFiSTAClass::disconnect(bool wifioff=false, bool eraseap=false)
```

!!! summary "引数"
	- bool `wifioff` 
	- bool `eraseap` 

!!! note "戻り値"
	bool one value of wl_status_t enum 



### isConnected()


is STA interface connected? 

```c
bool WiFiSTAClass::isConnected()
```

!!! note "戻り値"
	bool true if STA is connected to an AD 



### setAutoConnect()



```c
bool WiFiSTAClass::setAutoConnect(bool autoConnect)
```

!!! summary "引数"
	- bool `autoConnect` bool 

!!! note "戻り値"
	bool if saved 



### getAutoConnect()


Checks if ESP32 station mode will connect to AP automatically or not when it is powered on. 

```c
bool WiFiSTAClass::getAutoConnect()
```

!!! note "戻り値"
	bool auto connect 



### setAutoReconnect()



```c
bool WiFiSTAClass::setAutoReconnect(bool autoReconnect)
```

!!! summary "引数"
	- bool `autoReconnect` 

!!! note "戻り値"
	bool



### getAutoReconnect()



```c
bool WiFiSTAClass::getAutoReconnect()
```

!!! note "戻り値"
	bool



### waitForConnectResult()


Wait for WiFi connection to reach a result returns the status reached or disconnect if STA is off 

```c
uint8_t WiFiSTAClass::waitForConnectResult()
```

!!! note "戻り値"
	uint8_t wl_status_t 



### localIP()


Get the station interface IP address. 

```c
IPAddress WiFiSTAClass::localIP()
```

!!! note "戻り値"
	IPAddress  station IP 



### macAddress()



```c
uint8_t * WiFiSTAClass::macAddress(uint8_t *mac)
```

!!! summary "引数"
	- uint8_t* `mac` pointer to uint8_t array with length WL_MAC_ADDR_LENGTH 

!!! note "戻り値"
	uint8_t* pointer to uint8_t * 



### macAddress()


Get the station interface MAC address. 

```c
String WiFiSTAClass::macAddress()
```

!!! note "戻り値"
	String String mac 



### subnetMask()


Get the interface subnet mask address. 

```c
IPAddress WiFiSTAClass::subnetMask()
```

!!! note "戻り値"
	IPAddress  subnetMask 



### gatewayIP()


Get the gateway ip address. 

```c
IPAddress WiFiSTAClass::gatewayIP()
```

!!! note "戻り値"
	IPAddress  gatewayIP 



### dnsIP()



```c
IPAddress WiFiSTAClass::dnsIP(uint8_t dns_no=0)
```

!!! summary "引数"
	- uint8_t `dns_no` 

!!! note "戻り値"
	IPAddress  DNS  IP 



### enableIpV6()


Enable IPv6 on the station interface. 

```c
bool WiFiSTAClass::enableIpV6()
```

!!! note "戻り値"
	bool true on success 



### localIPv6()


Get the station interface IPv6 address. 

```c
IPv6Address WiFiSTAClass::localIPv6()
```

!!! note "戻り値"
	IPv6Address  



### getHostname()


Get the station interface Host name. 

```c
const char * WiFiSTAClass::getHostname()
```

!!! note "戻り値"
	constchar * char array hostname 



### setHostname()



```c
bool WiFiSTAClass::setHostname(const char *hostname)
```

!!! summary "引数"
	- constchar * `hostname` pointer to const string 

!!! note "戻り値"
	bool true on success 



### SSID()


Return the current SSID associated with the network 

```c
String WiFiSTAClass::SSID() const
```

!!! note "戻り値"
	String SSID 



### psk()


Return the current pre shared key associated with the network 

```c
String WiFiSTAClass::psk() const
```

!!! note "戻り値"
	String psk string 



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



### RSSI()


Return the current network RSSI. 

```c
int8_t WiFiSTAClass::RSSI()
```

!!! note "戻り値"
	int8_t RSSI value 



### beginSmartConfig()



```c
bool WiFiSTAClass::beginSmartConfig()
```

!!! note "戻り値"
	bool



### stopSmartConfig()



```c
bool WiFiSTAClass::stopSmartConfig()
```

!!! note "戻り値"
	bool



### smartConfigDone()



```c
bool WiFiSTAClass::smartConfigDone()
```

!!! note "戻り値"
	bool



### status()


Return Connection status. 

```c
wl_status_t WiFiSTAClass::status()
```

!!! note "戻り値"
	wl_status_t one of the value defined in wl_status_t 



### _setStatus()



```c
void WiFiSTAClass::_setStatus(wl_status_t status)
```

!!! summary "引数"
	- wl_status_t `status` 



