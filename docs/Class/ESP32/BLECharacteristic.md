# BLECharacteristic

The model of a BLE Characteristic. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_characteristic.html)

## メンバー

###  PROPERTY_READ

```c
const uint32_t BLECharacteristic::PROPERTY_READ
```


###  PROPERTY_WRITE

```c
const uint32_t BLECharacteristic::PROPERTY_WRITE
```


###  PROPERTY_NOTIFY

```c
const uint32_t BLECharacteristic::PROPERTY_NOTIFY
```


###  PROPERTY_BROADCAST

```c
const uint32_t BLECharacteristic::PROPERTY_BROADCAST
```


###  PROPERTY_INDICATE

```c
const uint32_t BLECharacteristic::PROPERTY_INDICATE
```


###  PROPERTY_WRITE_NR

```c
const uint32_t BLECharacteristic::PROPERTY_WRITE_NR
```


###  indicationTimeout

```c
const uint32_t BLECharacteristic::indicationTimeout
```


### BLECharacteristic()
Construct a characteristic


```c
BLECharacteristic::BLECharacteristic(const char *uuid, uint32_t properties=0)
```

!!! summary "引数"
	- constchar * `uuid` - UUID (const char*) for the characteristic. 
	- uint32_t `properties` - Properties for the characteristic. 



### BLECharacteristic()
Construct a characteristic


```c
BLECharacteristic::BLECharacteristic(BLEUUID uuid, uint32_t properties=0)
```

!!! summary "引数"
	- BLEUUID `uuid` - UUID for the characteristic. 
	- uint32_t `properties` - Properties for the characteristic. 



### ~BLECharacteristic()
Destructor.


```c
BLECharacteristic::~BLECharacteristic()
```



### addDescriptor()
Associate a descriptor with this characteristic.


```c
void BLECharacteristic::addDescriptor(BLEDescriptor *pDescriptor)
```

!!! summary "引数"
	- BLEDescriptor* `pDescriptor` 



### getDescriptorByUUID()
Return the BLE Descriptor for the given UUID if associated with this characteristic.


```c
BLEDescriptor * BLECharacteristic::getDescriptorByUUID(const char *descriptorUUID)
```

!!! summary "引数"
	- constchar * `descriptorUUID` The UUID of the descriptor that we wish to retrieve. 

!!! note "戻り値"
	BLEDescriptor* The BLE Descriptor. If no such descriptor is associated with the characteristic, nullptr is returned. 



### getDescriptorByUUID()
Return the BLE Descriptor for the given UUID if associated with this characteristic.


```c
BLEDescriptor * BLECharacteristic::getDescriptorByUUID(BLEUUID descriptorUUID)
```

!!! summary "引数"
	- BLEUUID `descriptorUUID` The UUID of the descriptor that we wish to retrieve. 

!!! note "戻り値"
	BLEDescriptor* The BLE Descriptor. If no such descriptor is associated with the characteristic, nullptr is returned. 



### getUUID()
Get the UUID of the characteristic.



```c
BLEUUID BLECharacteristic::getUUID()
```

!!! note "戻り値"
	BLEUUID The UUID of the characteristic. 



### getValue()
Retrieve the current value of the characteristic.



```c
std::string BLECharacteristic::getValue()
```

!!! note "戻り値"
	std::string A pointer to storage containing the current characteristic value. 



### getData()
Retrieve the current raw data of the characteristic.



```c
uint8_t * BLECharacteristic::getData()
```

!!! note "戻り値"
	uint8_t* A pointer to storage containing the current characteristic data. 



### indicate()
Send an indication. An indication is a transmission of up to the first 20 bytes of the characteristic value. An indication will block waiting a positive confirmation from the client.



```c
void BLECharacteristic::indicate()
```



### notify()
Send a notify. A notification is a transmission of up to the first 20 bytes of the characteristic value. An notification will not block; it is a fire and forget.



```c
void BLECharacteristic::notify(bool is_notification=true)
```

!!! summary "引数"
	- bool `is_notification` 



### setBroadcastProperty()
Set the permission to broadcast. A characteristics has properties associated with it which define what it is capable of doing. One of these is the broadcast flag.


```c
void BLECharacteristic::setBroadcastProperty(bool value)
```

!!! summary "引数"
	- bool `value` The flag value of the property. 



### setCallbacks()
Set the callback handlers for this characteristic.


```c
void BLECharacteristic::setCallbacks(BLECharacteristicCallbacks *pCallbacks)
```

!!! summary "引数"
	- BLECharacteristicCallbacks* `pCallbacks` An instance of a callbacks structure used to define any callbacks for the characteristic. 



### setIndicateProperty()
Set the Indicate property value.


```c
void BLECharacteristic::setIndicateProperty(bool value)
```

!!! summary "引数"
	- bool `value` Set to true if we are to allow indicate messages. 



### setNotifyProperty()
Set the Notify property value.


```c
void BLECharacteristic::setNotifyProperty(bool value)
```

!!! summary "引数"
	- bool `value` Set to true if we are to allow notification messages. 



### setReadProperty()
Set the Read property value.


```c
void BLECharacteristic::setReadProperty(bool value)
```

!!! summary "引数"
	- bool `value` Set to true if we are to allow reads. 



### setValue()
Set the value of the characteristic.


```c
void BLECharacteristic::setValue(uint8_t *data, size_t size)
```

!!! summary "引数"
	- uint8_t* `data` The data to set for the characteristic. 
	- size_t `size` 



### setValue()
Set the value of the characteristic from string data. We set the value of the characteristic from the bytes contained in the string.


```c
void BLECharacteristic::setValue(std::string value)
```

!!! summary "引数"
	- std::string `value` 



### setValue()



```c
void BLECharacteristic::setValue(uint16_t &data16)
```

!!! summary "引数"
	- uint16_t& `data16` 



### setValue()



```c
void BLECharacteristic::setValue(uint32_t &data32)
```

!!! summary "引数"
	- uint32_t& `data32` 



### setValue()



```c
void BLECharacteristic::setValue(int &data32)
```

!!! summary "引数"
	- int & `data32` 



### setValue()



```c
void BLECharacteristic::setValue(float &data32)
```

!!! summary "引数"
	- float & `data32` 



### setValue()



```c
void BLECharacteristic::setValue(double &data64)
```

!!! summary "引数"
	- double & `data64` 



### setWriteProperty()
Set the Write property value.


```c
void BLECharacteristic::setWriteProperty(bool value)
```

!!! summary "引数"
	- bool `value` Set to true if we are to allow writes. 



### setWriteNoResponseProperty()
Set the Write No Response property value.


```c
void BLECharacteristic::setWriteNoResponseProperty(bool value)
```

!!! summary "引数"
	- bool `value` Set to true if we are to allow writes with no response. 



### toString()
Return a string representation of the characteristic.



```c
std::string BLECharacteristic::toString()
```

!!! note "戻り値"
	std::string A string representation of the characteristic. 



### getHandle()
Get the handle of the characteristic.



```c
uint16_t BLECharacteristic::getHandle()
```

!!! note "戻り値"
	uint16_t The handle of the characteristic. 



### setAccessPermissions()



```c
void BLECharacteristic::setAccessPermissions(esp_gatt_perm_t perm)
```

!!! summary "引数"
	- esp_gatt_perm_t `perm` 



