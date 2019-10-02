# BLERemoteService

A model of a remote BLE service. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_remote_service.html)

## メンバー

### ~BLERemoteService()



```c
BLERemoteService::~BLERemoteService()
```



### getCharacteristic()
Get the remote characteristic object for the characteristic UUID.


```c
BLERemoteCharacteristic * BLERemoteService::getCharacteristic(const char *uuid)
```

!!! summary "引数"
	- constchar * `uuid` Remote characteristic uuid. 

!!! note "戻り値"
	BLERemoteCharacteristic* Reference to the remote characteristic object. 



### getCharacteristic()
Get the characteristic object for the UUID.


```c
BLERemoteCharacteristic * BLERemoteService::getCharacteristic(BLEUUID uuid)
```

!!! summary "引数"
	- BLEUUID `uuid` Characteristic uuid. 

!!! note "戻り値"
	BLERemoteCharacteristic* Reference to the characteristic object. 



### getCharacteristic()



```c
BLERemoteCharacteristic* BLERemoteService::getCharacteristic(uint16_t uuid)
```

!!! summary "引数"
	- uint16_t `uuid` 

!!! note "戻り値"
	BLERemoteCharacteristic*



### getCharacteristics()
Retrieve a map of all the characteristics of this service.



```c
std::map< std::string, BLERemoteCharacteristic * > * BLERemoteService::getCharacteristics()
```

!!! note "戻り値"
	std::map< ,  * > * A map of all the characteristics of this service. 



### getCharacteristicsByHandle()



```c
std::map<uint16_t, BLERemoteCharacteristic*>* BLERemoteService::getCharacteristicsByHandle()
```

!!! note "戻り値"
	std::map< ,  * > *



### getCharacteristics()
This function is designed to get characteristics map when we have multiple characteristics with the same UUID


```c
void BLERemoteService::getCharacteristics(std::map< uint16_t, BLERemoteCharacteristic * > *pCharacteristicMap)
```

!!! summary "引数"
	- std::map< ,  * > * `pCharacteristicMap` 



### getClient()
Get the client associated with this service.



```c
BLEClient * BLERemoteService::getClient(void)
```

!!! note "戻り値"
	BLEClient* A reference to the client associated with this service. 



### getHandle()



```c
uint16_t BLERemoteService::getHandle()
```

!!! note "戻り値"
	uint16_t



### getUUID()



```c
BLEUUID BLERemoteService::getUUID(void)
```

!!! note "戻り値"
	BLEUUID



### getValue()
Read the value of a characteristic associated with this service.


```c
std::string BLERemoteService::getValue(BLEUUID characteristicUuid)
```

!!! summary "引数"
	- BLEUUID `characteristicUuid` 

!!! note "戻り値"
	std::string



### setValue()
Set the value of a characteristic.


```c
void BLERemoteService::setValue(BLEUUID characteristicUuid, std::string value)
```

!!! summary "引数"
	- BLEUUID `characteristicUuid` The characteristic to set. 
	- std::string `value` The value to set. 



### toString()
Create a string representation of this remote service.



```c
std::string BLERemoteService::toString(void)
```

!!! note "戻り値"
	std::string A string representation of this remote service. 



