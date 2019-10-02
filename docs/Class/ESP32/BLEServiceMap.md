# BLEServiceMap

A data structure that manages the BLE servers owned by a BLE server. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_service_map.html)

## メンバー

### getByHandle()
Return the service by handle.


```c
BLEService * BLEServiceMap::getByHandle(uint16_t handle)
```

!!! summary "引数"
	- uint16_t `handle` The handle to look up the service. 

!!! note "戻り値"
	BLEService* The service. 



### getByUUID()
Return the service by UUID.


```c
BLEService * BLEServiceMap::getByUUID(const char *uuid)
```

!!! summary "引数"
	- constchar * `uuid` 

!!! note "戻り値"
	BLEService* The characteristic. 



### getByUUID()
Return the service by UUID.


```c
BLEService * BLEServiceMap::getByUUID(BLEUUID uuid, uint8_t inst_id=0)
```

!!! summary "引数"
	- BLEUUID `uuid` 
	- uint8_t `inst_id` 

!!! note "戻り値"
	BLEService* The characteristic. 



### handleGATTServerEvent()



```c
void BLEServiceMap::handleGATTServerEvent(esp_gatts_cb_event_t event, esp_gatt_if_t gatts_if, esp_ble_gatts_cb_param_t *param)
```

!!! summary "引数"
	- esp_gatts_cb_event_t `event` 
	- esp_gatt_if_t `gatts_if` 
	- esp_ble_gatts_cb_param_t* `param` 



### setByHandle()
Set the service by handle.


```c
void BLEServiceMap::setByHandle(uint16_t handle, BLEService *service)
```

!!! summary "引数"
	- uint16_t `handle` The handle of the service. 
	- BLEService* `service` The service to cache. 



### setByUUID()



```c
void BLEServiceMap::setByUUID(const char *uuid, BLEService *service)
```

!!! summary "引数"
	- constchar * `uuid` 
	- BLEService* `service` 



### setByUUID()
Set the service by UUID.


```c
void BLEServiceMap::setByUUID(BLEUUID uuid, BLEService *service)
```

!!! summary "引数"
	- BLEUUID `uuid` The uuid of the service. 
	- BLEService* `service` 



### toString()
Return a string representation of the service map.



```c
std::string BLEServiceMap::toString()
```

!!! note "戻り値"
	std::string A string representation of the service map. 



### getFirst()
Get the first service in the map.



```c
BLEService * BLEServiceMap::getFirst()
```

!!! note "戻り値"
	BLEService* The first service in the map. 



### getNext()
Get the next service in the map.



```c
BLEService * BLEServiceMap::getNext()
```

!!! note "戻り値"
	BLEService* The next service in the map. 



### removeService()
Removes service from maps.



```c
void BLEServiceMap::removeService(BLEService *service)
```

!!! summary "引数"
	- BLEService* `service` 



### getRegisteredServiceCount()
Returns the amount of registered services



```c
int BLEServiceMap::getRegisteredServiceCount()
```

!!! note "戻り値"
	int amount of registered services 



