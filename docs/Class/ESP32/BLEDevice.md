# BLEDevice



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_device.html)

## メンバー

###  m_appId

```c
uint16_t BLEDevice::m_appId
```


###  m_localMTU

```c
uint16_t BLEDevice::m_localMTU
```


###  m_securityLevel

```c
esp_ble_sec_act_t BLEDevice::m_securityLevel
```


###  m_customGapHandler

```c
gap_event_handler BLEDevice::m_customGapHandler
```


###  m_customGattcHandler

```c
gattc_event_handler BLEDevice::m_customGattcHandler
```


###  m_customGattsHandler

```c
gatts_event_handler BLEDevice::m_customGattsHandler
```


### createClient()
Create a new instance of a client.



```c
BLEClient * BLEDevice::createClient()
```

!!! note "戻り値"
	BLEClient* A new instance of the client. 



### createServer()
Create a new instance of a server.



```c
BLEServer * BLEDevice::createServer()
```

!!! note "戻り値"
	BLEServer* A new instance of the server. 



### getAddress()
Get the BLE device address.



```c
BLEAddress BLEDevice::getAddress()
```

!!! note "戻り値"
	BLEAddress The BLE device address. 



### getScan()
Retrieve the Scan object that we use for scanning.



```c
BLEScan * BLEDevice::getScan()
```

!!! note "戻り値"
	BLEScan* The scanning object reference. This is a singleton object. The caller should not try and release/delete it. 



### getValue()
Get the value of a characteristic of a service on a remote device.


```c
std::string BLEDevice::getValue(BLEAddress bdAddress, BLEUUID serviceUUID, BLEUUID characteristicUUID)
```

!!! summary "引数"
	- BLEAddress `bdAddress` 
	- BLEUUID `serviceUUID` 
	- BLEUUID `characteristicUUID` 

!!! note "戻り値"
	std::string



### init()
Initialize the BLE environment.


```c
void BLEDevice::init(std::string deviceName)
```

!!! summary "引数"
	- std::string `deviceName` The device name of the device. 



### setPower()
Set the transmission power. The power level can be one of:



```c
void BLEDevice::setPower(esp_power_level_t powerLevel)
```

!!! summary "引数"
	- esp_power_level_t `powerLevel` 



### setValue()
Set the value of a characteristic of a service on a remote device.


```c
void BLEDevice::setValue(BLEAddress bdAddress, BLEUUID serviceUUID, BLEUUID characteristicUUID, std::string value)
```

!!! summary "引数"
	- BLEAddress `bdAddress` 
	- BLEUUID `serviceUUID` 
	- BLEUUID `characteristicUUID` 
	- std::string `value` 



### toString()
Return a string representation of the nature of this device.



```c
std::string BLEDevice::toString()
```

!!! note "戻り値"
	std::string A string representation of the nature of this device. 



### whiteListAdd()
Add an entry to the BLE white list.


```c
void BLEDevice::whiteListAdd(BLEAddress address)
```

!!! summary "引数"
	- BLEAddress `address` The address to add to the white list. 



### whiteListRemove()
Remove an entry from the BLE white list.


```c
void BLEDevice::whiteListRemove(BLEAddress address)
```

!!! summary "引数"
	- BLEAddress `address` The address to remove from the white list. 



### setEncryptionLevel()



```c
void BLEDevice::setEncryptionLevel(esp_ble_sec_act_t level)
```

!!! summary "引数"
	- esp_ble_sec_act_t `level` 



### setSecurityCallbacks()



```c
void BLEDevice::setSecurityCallbacks(BLESecurityCallbacks *pCallbacks)
```

!!! summary "引数"
	- BLESecurityCallbacks* `pCallbacks` 



### setMTU()



```c
esp_err_t BLEDevice::setMTU(uint16_t mtu)
```

!!! summary "引数"
	- uint16_t `mtu` 

!!! note "戻り値"
	esp_err_t



### getMTU()



```c
uint16_t BLEDevice::getMTU()
```

!!! note "戻り値"
	uint16_t



### getInitialized()



```c
bool BLEDevice::getInitialized()
```

!!! note "戻り値"
	bool



### getAdvertising()



```c
BLEAdvertising * BLEDevice::getAdvertising()
```

!!! note "戻り値"
	BLEAdvertising*



### startAdvertising()



```c
void BLEDevice::startAdvertising()
```



### getPeerDevices()



```c
std::map< uint16_t, conn_status_t > BLEDevice::getPeerDevices(bool client)
```

!!! summary "引数"
	- bool `client` 

!!! note "戻り値"
	std::map< ,  >



### addPeerDevice()



```c
void BLEDevice::addPeerDevice(void *peer, bool is_client, uint16_t conn_id)
```

!!! summary "引数"
	- void * `peer` 
	- bool `is_client` 
	- uint16_t `conn_id` 



### updatePeerDevice()



```c
void BLEDevice::updatePeerDevice(void *peer, bool _client, uint16_t conn_id)
```

!!! summary "引数"
	- void * `peer` 
	- bool `_client` 
	- uint16_t `conn_id` 



### removePeerDevice()



```c
void BLEDevice::removePeerDevice(uint16_t conn_id, bool client)
```

!!! summary "引数"
	- uint16_t `conn_id` 
	- bool `client` 



### getClientByGattIf()



```c
BLEClient * BLEDevice::getClientByGattIf(uint16_t conn_id)
```

!!! summary "引数"
	- uint16_t `conn_id` 

!!! note "戻り値"
	BLEClient*



### setCustomGapHandler()



```c
void BLEDevice::setCustomGapHandler(gap_event_handler handler)
```

!!! summary "引数"
	- gap_event_handler `handler` 



### setCustomGattcHandler()



```c
void BLEDevice::setCustomGattcHandler(gattc_event_handler handler)
```

!!! summary "引数"
	- gattc_event_handler `handler` 



### setCustomGattsHandler()



```c
void BLEDevice::setCustomGattsHandler(gatts_event_handler handler)
```

!!! summary "引数"
	- gatts_event_handler `handler` 



### deinit()
de-Initialize the BLE environment.


```c
void BLEDevice::deinit(bool release_memory=false)
```

!!! summary "引数"
	- bool `release_memory` release the internal BT stack memory 



