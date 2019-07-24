# BLECharacteristicMap

A data mapping used to manage the set of BLE characteristics known to the server. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_characteristic_map.html)

## メンバー

### setByUUID()



```c
void BLECharacteristicMap::setByUUID(BLECharacteristic *pCharacteristic, const char *uuid)
```

!!! summary "引数"
	- BLECharacteristic* `pCharacteristic` 
	- constchar * `uuid` 



### setByUUID()
Set the characteristic by UUID.


```c
void BLECharacteristicMap::setByUUID(BLECharacteristic *pCharacteristic, BLEUUID uuid)
```

!!! summary "引数"
	- BLECharacteristic* `pCharacteristic` 
	- BLEUUID `uuid` The uuid of the characteristic. 



### setByHandle()
Set the characteristic by handle.


```c
void BLECharacteristicMap::setByHandle(uint16_t handle, BLECharacteristic *pCharacteristic)
```

!!! summary "引数"
	- uint16_t `handle` The handle of the characteristic. 
	- BLECharacteristic* `pCharacteristic` 



### getByUUID()
Return the characteristic by UUID.


```c
BLECharacteristic * BLECharacteristicMap::getByUUID(const char *uuid)
```

!!! summary "引数"
	- constchar * `uuid` 

!!! note "戻り値"
	BLECharacteristic* The characteristic. 



### getByUUID()
Return the characteristic by UUID.


```c
BLECharacteristic * BLECharacteristicMap::getByUUID(BLEUUID uuid)
```

!!! summary "引数"
	- BLEUUID `uuid` 

!!! note "戻り値"
	BLECharacteristic* The characteristic. 



### getByHandle()
Return the characteristic by handle.


```c
BLECharacteristic * BLECharacteristicMap::getByHandle(uint16_t handle)
```

!!! summary "引数"
	- uint16_t `handle` The handle to look up the characteristic. 

!!! note "戻り値"
	BLECharacteristic* The characteristic. 



### getFirst()
Get the first characteristic in the map.



```c
BLECharacteristic * BLECharacteristicMap::getFirst()
```

!!! note "戻り値"
	BLECharacteristic* The first characteristic in the map. 



### getNext()
Get the next characteristic in the map.



```c
BLECharacteristic * BLECharacteristicMap::getNext()
```

!!! note "戻り値"
	BLECharacteristic* The next characteristic in the map. 



### toString()
Return a string representation of the characteristic map.



```c
std::string BLECharacteristicMap::toString()
```

!!! note "戻り値"
	std::string A string representation of the characteristic map. 



### handleGATTServerEvent()
Pass the GATT server event onwards to each of the characteristics found in the mapping


```c
void BLECharacteristicMap::handleGATTServerEvent(esp_gatts_cb_event_t event, esp_gatt_if_t gatts_if, esp_ble_gatts_cb_param_t *param)
```

!!! summary "引数"
	- esp_gatts_cb_event_t `event` 
	- esp_gatt_if_t `gatts_if` 
	- esp_ble_gatts_cb_param_t* `param` 



