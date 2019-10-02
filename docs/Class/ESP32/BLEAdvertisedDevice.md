# BLEAdvertisedDevice

A representation of a BLE advertised device found by a scan. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_advertised_device.html)

## メンバー

### BLEAdvertisedDevice()



```c
BLEAdvertisedDevice::BLEAdvertisedDevice()
```



### getAddress()
Get the address.



```c
BLEAddress BLEAdvertisedDevice::getAddress()
```

!!! note "戻り値"
	BLEAddress



### getAppearance()
Get the appearance.



```c
uint16_t BLEAdvertisedDevice::getAppearance()
```

!!! note "戻り値"
	uint16_t



### getManufacturerData()
Get the manufacturer data.



```c
std::string BLEAdvertisedDevice::getManufacturerData()
```

!!! note "戻り値"
	std::string The manufacturer data of the advertised device. 



### getName()
Get the name.



```c
std::string BLEAdvertisedDevice::getName()
```

!!! note "戻り値"
	std::string The name of the advertised device. 



### getRSSI()
Get the RSSI.



```c
int BLEAdvertisedDevice::getRSSI()
```

!!! note "戻り値"
	int The RSSI of the advertised device. 



### getScan()
Get the scan object that created this advertisement.



```c
BLEScan * BLEAdvertisedDevice::getScan()
```

!!! note "戻り値"
	BLEScan* The scan object. 



### getServiceData()
Get the service data.



```c
std::string BLEAdvertisedDevice::getServiceData()
```

!!! note "戻り値"
	std::string The ServiceData of the advertised device. 



### getServiceDataUUID()
Get the service data UUID.



```c
BLEUUID BLEAdvertisedDevice::getServiceDataUUID()
```

!!! note "戻り値"
	BLEUUID The service data UUID. 



### getServiceUUID()
Get the Service UUID.



```c
BLEUUID BLEAdvertisedDevice::getServiceUUID()
```

!!! note "戻り値"
	BLEUUID The Service UUID of the advertised device. 



### getTXPower()
Get the TX Power.



```c
int8_t BLEAdvertisedDevice::getTXPower()
```

!!! note "戻り値"
	int8_t The TX Power of the advertised device. 



### getPayload()



```c
uint8_t * BLEAdvertisedDevice::getPayload()
```

!!! note "戻り値"
	uint8_t*



### getPayloadLength()



```c
size_t BLEAdvertisedDevice::getPayloadLength()
```

!!! note "戻り値"
	size_t



### getAddressType()



```c
esp_ble_addr_type_t BLEAdvertisedDevice::getAddressType()
```

!!! note "戻り値"
	esp_ble_addr_type_t



### setAddressType()



```c
void BLEAdvertisedDevice::setAddressType(esp_ble_addr_type_t type)
```

!!! summary "引数"
	- esp_ble_addr_type_t `type` 



### isAdvertisingService()
Check advertised serviced for existence required UUID



```c
bool BLEAdvertisedDevice::isAdvertisingService(BLEUUID uuid)
```

!!! summary "引数"
	- BLEUUID `uuid` 

!!! note "戻り値"
	bool Return true if service is advertised 



### haveAppearance()
Does this advertisement have an appearance value?



```c
bool BLEAdvertisedDevice::haveAppearance()
```

!!! note "戻り値"
	bool True if there is an appearance value present. 



### haveManufacturerData()
Does this advertisement have manufacturer data?



```c
bool BLEAdvertisedDevice::haveManufacturerData()
```

!!! note "戻り値"
	bool True if there is manufacturer data present. 



### haveName()
Does this advertisement have a name value?



```c
bool BLEAdvertisedDevice::haveName()
```

!!! note "戻り値"
	bool True if there is a name value present. 



### haveRSSI()
Does this advertisement have a signal strength value?



```c
bool BLEAdvertisedDevice::haveRSSI()
```

!!! note "戻り値"
	bool True if there is a signal strength value present. 



### haveServiceData()
Does this advertisement have a service data value?



```c
bool BLEAdvertisedDevice::haveServiceData()
```

!!! note "戻り値"
	bool True if there is a service data value present. 



### haveServiceUUID()
Does this advertisement have a service UUID value?



```c
bool BLEAdvertisedDevice::haveServiceUUID()
```

!!! note "戻り値"
	bool True if there is a service UUID value present. 



### haveTXPower()
Does this advertisement have a transmission power value?



```c
bool BLEAdvertisedDevice::haveTXPower()
```

!!! note "戻り値"
	bool True if there is a transmission power value present. 



### toString()
Create a string representation of this device.



```c
std::string BLEAdvertisedDevice::toString()
```

!!! note "戻り値"
	std::string A string representation of this device. 



