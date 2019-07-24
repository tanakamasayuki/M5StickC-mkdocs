# BLEAdvertisementData

Advertisement data set by the programmer to be published by the BLE server. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_advertisement_data.html)

## メンバー

### setAppearance()
Set the appearance.


```c
void BLEAdvertisementData::setAppearance(uint16_t appearance)
```

!!! summary "引数"
	- uint16_t `appearance` The appearance code value.



### setCompleteServices()
Set the complete services.


```c
void BLEAdvertisementData::setCompleteServices(BLEUUID uuid)
```

!!! summary "引数"
	- BLEUUID `uuid` The single service to advertise. 



### setFlags()
Set the advertisement flags.


```c
void BLEAdvertisementData::setFlags(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 



### setManufacturerData()
Set manufacturer specific data.


```c
void BLEAdvertisementData::setManufacturerData(std::string data)
```

!!! summary "引数"
	- std::string `data` Manufacturer data. 



### setName()
Set the name.


```c
void BLEAdvertisementData::setName(std::string name)
```

!!! summary "引数"
	- std::string `name` 



### setPartialServices()
Set the partial services.


```c
void BLEAdvertisementData::setPartialServices(BLEUUID uuid)
```

!!! summary "引数"
	- BLEUUID `uuid` The single service to advertise. 



### setServiceData()
Set the service data (UUID + data)


```c
void BLEAdvertisementData::setServiceData(BLEUUID uuid, std::string data)
```

!!! summary "引数"
	- BLEUUID `uuid` The UUID to set with the service data. Size of UUID will be used. 
	- std::string `data` The data to be associated with the service data advert. 



### setShortName()
Set the short name.


```c
void BLEAdvertisementData::setShortName(std::string name)
```

!!! summary "引数"
	- std::string `name` 



### addData()
Add data to the payload to be advertised.


```c
void BLEAdvertisementData::addData(std::string data)
```

!!! summary "引数"
	- std::string `data` The data to be added to the payload. 



### getPayload()
Retrieve the payload that is to be advertised.



```c
std::string BLEAdvertisementData::getPayload()
```

!!! note "戻り値"
	std::string The payload that is to be advertised. 



