# BLEClient

A model of a BLE client. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_client.html)

## メンバー

###  m_appId

```c
uint16_t BLEClient::m_appId
```


### BLEClient()



```c
BLEClient::BLEClient()
```



### ~BLEClient()
Destructor.


```c
BLEClient::~BLEClient()
```



### connect()


Add overloaded function to ease connect to peer device with not public address 
```c
bool BLEClient::connect(BLEAdvertisedDevice *device)
```

!!! summary "引数"
	- BLEAdvertisedDevice* `device` 

!!! note "戻り値"
	bool



### connect()
Connect to the partner (BLE ).


```c
bool BLEClient::connect(BLEAddress address, esp_ble_addr_type_t type=BLE_ADDR_TYPE_PUBLIC)
```

!!! summary "引数"
	- BLEAddress `address` The address of the partner. 
	- esp_ble_addr_type_t `type` 

!!! note "戻り値"
	bool True on success. 



### disconnect()
Disconnect from the peer.



```c
void BLEClient::disconnect()
```



### getPeerAddress()
Retrieve the address of the peer.

Returns the Bluetooth device address of the BLE peer to which this client is connected. 
```c
BLEAddress BLEClient::getPeerAddress()
```

!!! note "戻り値"
	BLEAddress



### getRssi()
Ask the BLE server for the RSSI value.



```c
int BLEClient::getRssi()
```

!!! note "戻り値"
	int The RSSI value. 



### getServices()
Ask the remote BLE server for its services. A BLE  exposes a set of services for its partners. Here we ask the server for its set of services and wait until we have received them all.



```c
std::map< std::string, BLERemoteService * > * BLEClient::getServices()
```

!!! note "戻り値"
	std::map< ,  * > * N/A 



### getService()
Get the service BLE Remote Service instance corresponding to the uuid.


```c
BLERemoteService * BLEClient::getService(const char *uuid)
```

!!! summary "引数"
	- constchar * `uuid` The UUID of the service being sought. 

!!! note "戻り値"
	BLERemoteService* A reference to the Service or nullptr if don't know about it. 



### getService()
Get the service object corresponding to the uuid.


```c
BLERemoteService * BLEClient::getService(BLEUUID uuid)
```

!!! summary "引数"
	- BLEUUID `uuid` The UUID of the service being sought. 

!!! note "戻り値"
	BLERemoteService* A reference to the Service or nullptr if don't know about it. 



### getValue()
Get the value of a specific characteristic associated with a specific service.


```c
std::string BLEClient::getValue(BLEUUID serviceUUID, BLEUUID characteristicUUID)
```

!!! summary "引数"
	- BLEUUID `serviceUUID` The service that owns the characteristic. 
	- BLEUUID `characteristicUUID` The characteristic whose value we wish to read. 

!!! note "戻り値"
	std::string



### handleGAPEvent()
Handle a received GAP event.


```c
void BLEClient::handleGAPEvent(esp_gap_ble_cb_event_t event, esp_ble_gap_cb_param_t *param)
```

!!! summary "引数"
	- esp_gap_ble_cb_event_t `event` 
	- esp_ble_gap_cb_param_t* `param` 



### isConnected()
Are we connected to a partner?



```c
bool BLEClient::isConnected()
```

!!! note "戻り値"
	bool True if we are connected and false if we are not connected. 



### setClientCallbacks()
Set the callbacks that will be invoked.


```c
void BLEClient::setClientCallbacks(BLEClientCallbacks *pClientCallbacks)
```

!!! summary "引数"
	- BLEClientCallbacks* `pClientCallbacks` 



### setValue()
Set the value of a specific characteristic associated with a specific service.


```c
void BLEClient::setValue(BLEUUID serviceUUID, BLEUUID characteristicUUID, std::string value)
```

!!! summary "引数"
	- BLEUUID `serviceUUID` The service that owns the characteristic. 
	- BLEUUID `characteristicUUID` The characteristic whose value we wish to write. 
	- std::string `value` 



### toString()
Return a string representation of this client.



```c
std::string BLEClient::toString()
```

!!! note "戻り値"
	std::string A string representation of this client. 



### getConnId()



```c
uint16_t BLEClient::getConnId()
```

!!! note "戻り値"
	uint16_t



### getGattcIf()



```c
esp_gatt_if_t BLEClient::getGattcIf()
```

!!! note "戻り値"
	esp_gatt_if_t



### getMTU()



```c
uint16_t BLEClient::getMTU()
```

!!! note "戻り値"
	uint16_t



