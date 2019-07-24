# BLEService

The model of a BLE service. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_service.html)

## メンバー

###  m_instId

```c
uint8_t BLEService::m_instId
```


### addCharacteristic()
Add a characteristic to the service.


```c
void BLEService::addCharacteristic(BLECharacteristic *pCharacteristic)
```

!!! summary "引数"
	- BLECharacteristic* `pCharacteristic` A pointer to the characteristic to be added. 



### createCharacteristic()
Create a new BLE Characteristic associated with this service.


```c
BLECharacteristic * BLEService::createCharacteristic(const char *uuid, uint32_t properties)
```

!!! summary "引数"
	- constchar * `uuid` - The UUID of the characteristic. 
	- uint32_t `properties` - The properties of the characteristic. 

!!! note "戻り値"
	BLECharacteristic* The new BLE characteristic. 



### createCharacteristic()
Create a new BLE Characteristic associated with this service.


```c
BLECharacteristic * BLEService::createCharacteristic(BLEUUID uuid, uint32_t properties)
```

!!! summary "引数"
	- BLEUUID `uuid` - The UUID of the characteristic. 
	- uint32_t `properties` - The properties of the characteristic. 

!!! note "戻り値"
	BLECharacteristic* The new BLE characteristic. 



### dump()
Dump details of this BLE GATT service.



```c
void BLEService::dump()
```



### executeCreate()
Create the service. Create the service.


```c
void BLEService::executeCreate(BLEServer *pServer)
```

!!! summary "引数"
	- BLEServer* `pServer` 



### executeDelete()
Delete the service. Delete the service.



```c
void BLEService::executeDelete()
```



### getCharacteristic()



```c
BLECharacteristic * BLEService::getCharacteristic(const char *uuid)
```

!!! summary "引数"
	- constchar * `uuid` 

!!! note "戻り値"
	BLECharacteristic*



### getCharacteristic()



```c
BLECharacteristic * BLEService::getCharacteristic(BLEUUID uuid)
```

!!! summary "引数"
	- BLEUUID `uuid` 

!!! note "戻り値"
	BLECharacteristic*



### getUUID()
Get the UUID of the service.



```c
BLEUUID BLEService::getUUID()
```

!!! note "戻り値"
	BLEUUID the UUID of the service. 



### getServer()
Get the BLE server associated with this service.



```c
BLEServer * BLEService::getServer()
```

!!! note "戻り値"
	BLEServer* The  associated with this service. 



### start()
Start the service. Here we wish to start the service which means that we will respond to partner requests about it. Starting a service also means that we can create the corresponding characteristics.



```c
void BLEService::start()
```



### stop()
Stop the service.


```c
void BLEService::stop()
```



### toString()
Return a string representation of this service. A service is defined by:



```c
std::string BLEService::toString()
```

!!! note "戻り値"
	std::string



### getHandle()
Get the handle associated with this service.



```c
uint16_t BLEService::getHandle()
```

!!! note "戻り値"
	uint16_t The handle associated with this service. 



