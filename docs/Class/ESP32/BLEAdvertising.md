# BLEAdvertising

Perform and manage BLE advertising. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_advertising.html)

## メンバー

### BLEAdvertising()
Construct a default advertising object.


```c
BLEAdvertising::BLEAdvertising()
```



### addServiceUUID()
Add a service uuid to exposed list of services.


```c
void BLEAdvertising::addServiceUUID(BLEUUID serviceUUID)
```

!!! summary "引数"
	- BLEUUID `serviceUUID` The UUID of the service to expose. 



### addServiceUUID()
Add a service uuid to exposed list of services.


```c
void BLEAdvertising::addServiceUUID(const char *serviceUUID)
```

!!! summary "引数"
	- constchar * `serviceUUID` The string representation of the service to expose. 



### start()
Start advertising. Start advertising.



```c
void BLEAdvertising::start()
```



### stop()
Stop advertising. Stop advertising.



```c
void BLEAdvertising::stop()
```



### setAppearance()
Set the device appearance in the advertising data. The appearance attribute is of type 0x19. The codes for distinct appearances can be found here: .


```c
void BLEAdvertising::setAppearance(uint16_t appearance)
```

!!! summary "引数"
	- uint16_t `appearance` The appearance of the device in the advertising data. 



### setMaxInterval()



```c
void BLEAdvertising::setMaxInterval(uint16_t maxinterval)
```

!!! summary "引数"
	- uint16_t `maxinterval` 



### setMinInterval()



```c
void BLEAdvertising::setMinInterval(uint16_t mininterval)
```

!!! summary "引数"
	- uint16_t `mininterval` 



### setAdvertisementData()
Set the advertisement data that is to be published in a regular advertisement.


```c
void BLEAdvertising::setAdvertisementData(BLEAdvertisementData &advertisementData)
```

!!! summary "引数"
	- BLEAdvertisementData& `advertisementData` The data to be advertised. 



### setScanFilter()
Set the filtering for the scan filter.


```c
void BLEAdvertising::setScanFilter(bool scanRequertWhitelistOnly, bool connectWhitelistOnly)
```

!!! summary "引数"
	- bool `scanRequertWhitelistOnly` 
	- bool `connectWhitelistOnly` If true, only allow connections from those on the white list. 



### setScanResponseData()
Set the advertisement data that is to be published in a scan response.


```c
void BLEAdvertising::setScanResponseData(BLEAdvertisementData &advertisementData)
```

!!! summary "引数"
	- BLEAdvertisementData& `advertisementData` The data to be advertised. 



### setPrivateAddress()



```c
void BLEAdvertising::setPrivateAddress(esp_ble_addr_type_t type=BLE_ADDR_TYPE_RANDOM)
```

!!! summary "引数"
	- esp_ble_addr_type_t `type` 



### setDeviceAddress()
Set BLE address.


```c
void BLEAdvertising::setDeviceAddress(esp_bd_addr_t addr, esp_ble_addr_type_t type=BLE_ADDR_TYPE_RANDOM)
```

!!! summary "引数"
	- esp_bd_addr_t `addr` 
	- esp_ble_addr_type_t `type` 



### handleGAPEvent()



```c
void BLEAdvertising::handleGAPEvent(esp_gap_ble_cb_event_t event, esp_ble_gap_cb_param_t *param)
```

!!! summary "引数"
	- esp_gap_ble_cb_event_t `event` 
	- esp_ble_gap_cb_param_t* `param` 



### setMinPreferred()



```c
void BLEAdvertising::setMinPreferred(uint16_t)
```

!!! summary "引数"
	- uint16_t `` 



### setMaxPreferred()



```c
void BLEAdvertising::setMaxPreferred(uint16_t)
```

!!! summary "引数"
	- uint16_t `` 



### setScanResponse()



```c
void BLEAdvertising::setScanResponse(bool)
```

!!! summary "引数"
	- bool `` 



