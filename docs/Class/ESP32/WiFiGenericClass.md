# WiFiGenericClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_wi_fi_generic_class.html)

## メンバー

### WiFiGenericClass()



```c
WiFiGenericClass::WiFiGenericClass()
```



### onEvent()



```c
wifi_event_id_t WiFiGenericClass::onEvent(WiFiEventCb cbEvent, system_event_id_t event=SYSTEM_EVENT_MAX)
```

!!! summary "引数"
	- WiFiEventCb `cbEvent` WiFiEventCb 
	- system_event_id_t `event` optional filter (WIFI_EVENT_MAX is all events) 

!!! note "戻り値"
	wifi_event_id_t



### onEvent()



```c
wifi_event_id_t WiFiGenericClass::onEvent(WiFiEventFuncCb cbEvent, system_event_id_t event=SYSTEM_EVENT_MAX)
```

!!! summary "引数"
	- WiFiEventFuncCb `cbEvent` 
	- system_event_id_t `event` 

!!! note "戻り値"
	wifi_event_id_t



### onEvent()



```c
wifi_event_id_t WiFiGenericClass::onEvent(WiFiEventSysCb cbEvent, system_event_id_t event=SYSTEM_EVENT_MAX)
```

!!! summary "引数"
	- WiFiEventSysCb `cbEvent` 
	- system_event_id_t `event` 

!!! note "戻り値"
	wifi_event_id_t



### removeEvent()



```c
void WiFiGenericClass::removeEvent(WiFiEventCb cbEvent, system_event_id_t event=SYSTEM_EVENT_MAX)
```

!!! summary "引数"
	- WiFiEventCb `cbEvent` WiFiEventCb 
	- system_event_id_t `event` optional filter (WIFI_EVENT_MAX is all events) 



### removeEvent()



```c
void WiFiGenericClass::removeEvent(WiFiEventSysCb cbEvent, system_event_id_t event=SYSTEM_EVENT_MAX)
```

!!! summary "引数"
	- WiFiEventSysCb `cbEvent` 
	- system_event_id_t `event` 



### removeEvent()



```c
void WiFiGenericClass::removeEvent(wifi_event_id_t id)
```

!!! summary "引数"
	- wifi_event_id_t `id` 



### channel()


Return the current channel associated with the network 

```c
int32_t WiFiGenericClass::channel(void)
```

!!! note "戻り値"
	int32_t channel (1-13) 



### persistent()



```c
void WiFiGenericClass::persistent(bool persistent)
```

!!! summary "引数"
	- bool `persistent` 



### enableSTA()



```c
bool WiFiGenericClass::enableSTA(bool enable)
```

!!! summary "引数"
	- bool `enable` bool 

!!! note "戻り値"
	bool ok 



### enableAP()



```c
bool WiFiGenericClass::enableAP(bool enable)
```

!!! summary "引数"
	- bool `enable` bool 

!!! note "戻り値"
	bool ok 



### setSleep()



```c
bool WiFiGenericClass::setSleep(bool enable)
```

!!! summary "引数"
	- bool `enable` bool 

!!! note "戻り値"
	bool ok 



### getSleep()


get modem sleep enabled 

```c
bool WiFiGenericClass::getSleep()
```

!!! note "戻り値"
	bool true if modem sleep is enabled 



### setTxPower()



```c
bool WiFiGenericClass::setTxPower(wifi_power_t power)
```

!!! summary "引数"
	- wifi_power_t `power` enum maximum wifi tx power 

!!! note "戻り値"
	bool ok 



### getTxPower()



```c
wifi_power_t WiFiGenericClass::getTxPower()
```

!!! note "戻り値"
	wifi_power_t



### getStatusBits()



```c
int WiFiGenericClass::getStatusBits()
```

!!! note "戻り値"
	int



### waitStatusBits()



```c
int WiFiGenericClass::waitStatusBits(int bits, uint32_t timeout_ms)
```

!!! summary "引数"
	- int `bits` 
	- uint32_t `timeout_ms` 

!!! note "戻り値"
	int



### mode()



```c
bool WiFiGenericClass::mode(wifi_mode_t)
```

!!! summary "引数"
	- wifi_mode_t `` 

!!! note "戻り値"
	bool



### getMode()


get WiFi mode 

```c
wifi_mode_t WiFiGenericClass::getMode()
```

!!! note "戻り値"
	wifi_mode_t WiFiMode 



### _eventCallback()



```c
esp_err_t WiFiGenericClass::_eventCallback(void *arg, system_event_t *event)
```

!!! summary "引数"
	- void * `arg` 
	- system_event_t* `event` 

!!! note "戻り値"
	esp_err_t



### hostByName()



```c
int WiFiGenericClass::hostByName(const char *aHostname, IPAddress &aResult)
```

!!! summary "引数"
	- constchar * `aHostname` Name to be resolved 
	- IPAddress& `aResult`  structure to store the returned IP address 

!!! note "戻り値"
	int 1 if aIPAddrString was successfully converted to an IP address, else error code 



### calculateNetworkID()



```c
IPAddress WiFiGenericClass::calculateNetworkID(IPAddress ip, IPAddress subnet)
```

!!! summary "引数"
	- IPAddress `ip` 
	- IPAddress `subnet` 

!!! note "戻り値"
	IPAddress



### calculateBroadcast()



```c
IPAddress WiFiGenericClass::calculateBroadcast(IPAddress ip, IPAddress subnet)
```

!!! summary "引数"
	- IPAddress `ip` 
	- IPAddress `subnet` 

!!! note "戻り値"
	IPAddress



### calculateSubnetCIDR()



```c
uint8_t WiFiGenericClass::calculateSubnetCIDR(IPAddress subnetMask)
```

!!! summary "引数"
	- IPAddress `subnetMask` 

!!! note "戻り値"
	uint8_t



