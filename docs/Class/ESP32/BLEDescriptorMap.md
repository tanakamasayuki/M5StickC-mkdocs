# BLEDescriptorMap

A management structure for BLE descriptors. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_descriptor_map.html)

## メンバー

### setByUUID()
Set the descriptor by UUID.


```c
void BLEDescriptorMap::setByUUID(const char *uuid, BLEDescriptor *pDescriptor)
```

!!! summary "引数"
	- constchar * `uuid` The uuid of the descriptor. 
	- BLEDescriptor* `pDescriptor` 



### setByUUID()
Set the descriptor by UUID.


```c
void BLEDescriptorMap::setByUUID(BLEUUID uuid, BLEDescriptor *pDescriptor)
```

!!! summary "引数"
	- BLEUUID `uuid` The uuid of the descriptor. 
	- BLEDescriptor* `pDescriptor` 



### setByHandle()
Set the descriptor by handle.


```c
void BLEDescriptorMap::setByHandle(uint16_t handle, BLEDescriptor *pDescriptor)
```

!!! summary "引数"
	- uint16_t `handle` The handle of the descriptor. 
	- BLEDescriptor* `pDescriptor` 



### getByUUID()
Return the descriptor by UUID.


```c
BLEDescriptor * BLEDescriptorMap::getByUUID(const char *uuid)
```

!!! summary "引数"
	- constchar * `uuid` 

!!! note "戻り値"
	BLEDescriptor* The descriptor. If not present, then nullptr is returned. 



### getByUUID()
Return the descriptor by UUID.


```c
BLEDescriptor * BLEDescriptorMap::getByUUID(BLEUUID uuid)
```

!!! summary "引数"
	- BLEUUID `uuid` 

!!! note "戻り値"
	BLEDescriptor* The descriptor. If not present, then nullptr is returned. 



### getByHandle()
Return the descriptor by handle.


```c
BLEDescriptor * BLEDescriptorMap::getByHandle(uint16_t handle)
```

!!! summary "引数"
	- uint16_t `handle` The handle to look up the descriptor. 

!!! note "戻り値"
	BLEDescriptor* The descriptor. 



### toString()
Return a string representation of the descriptor map.



```c
std::string BLEDescriptorMap::toString()
```

!!! note "戻り値"
	std::string A string representation of the descriptor map. 



### handleGATTServerEvent()



```c
void BLEDescriptorMap::handleGATTServerEvent(esp_gatts_cb_event_t event, esp_gatt_if_t gatts_if, esp_ble_gatts_cb_param_t *param)
```

!!! summary "引数"
	- esp_gatts_cb_event_t `event` 
	- esp_gatt_if_t `gatts_if` 
	- esp_ble_gatts_cb_param_t* `param` 



### getFirst()
Get the first descriptor in the map.



```c
BLEDescriptor * BLEDescriptorMap::getFirst()
```

!!! note "戻り値"
	BLEDescriptor* The first descriptor in the map. 



### getNext()
Get the next descriptor in the map.



```c
BLEDescriptor * BLEDescriptorMap::getNext()
```

!!! note "戻り値"
	BLEDescriptor* The next descriptor in the map. 



