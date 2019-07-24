# BLERemoteDescriptor

A model of remote BLE descriptor. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_remote_descriptor.html)

## メンバー

### getHandle()
Retrieve the handle associated with this remote descriptor.



```c
uint16_t BLERemoteDescriptor::getHandle()
```

!!! note "戻り値"
	uint16_t The handle associated with this remote descriptor. 



### getRemoteCharacteristic()
Get the characteristic that owns this descriptor.



```c
BLERemoteCharacteristic * BLERemoteDescriptor::getRemoteCharacteristic()
```

!!! note "戻り値"
	BLERemoteCharacteristic* The characteristic that owns this descriptor. 



### getUUID()
Retrieve the UUID associated this remote descriptor.



```c
BLEUUID BLERemoteDescriptor::getUUID()
```

!!! note "戻り値"
	BLEUUID The UUID associated this remote descriptor. 



### readValue()



```c
std::string BLERemoteDescriptor::readValue(void)
```

!!! note "戻り値"
	std::string



### readUInt8()



```c
uint8_t BLERemoteDescriptor::readUInt8(void)
```

!!! note "戻り値"
	uint8_t



### readUInt16()



```c
uint16_t BLERemoteDescriptor::readUInt16(void)
```

!!! note "戻り値"
	uint16_t



### readUInt32()



```c
uint32_t BLERemoteDescriptor::readUInt32(void)
```

!!! note "戻り値"
	uint32_t



### toString()
Return a string representation of this BLE Remote Descriptor. @retun A string representation of this BLE Remote Descriptor.


```c
std::string BLERemoteDescriptor::toString(void)
```

!!! note "戻り値"
	std::string



### writeValue()
Write data to the BLE Remote Descriptor.


```c
void BLERemoteDescriptor::writeValue(uint8_t *data, size_t length, bool response=false)
```

!!! summary "引数"
	- uint8_t* `data` The data to send to the remote descriptor. 
	- size_t `length` The length of the data to send. 
	- bool `response` True if we expect a response. 



### writeValue()
Write data represented as a string to the BLE Remote Descriptor.


```c
void BLERemoteDescriptor::writeValue(std::string newValue, bool response=false)
```

!!! summary "引数"
	- std::string `newValue` The data to send to the remote descriptor. 
	- bool `response` True if we expect a response. 



### writeValue()
Write a byte value to the Descriptor.


```c
void BLERemoteDescriptor::writeValue(uint8_t newValue, bool response=false)
```

!!! summary "引数"
	- uint8_t `newValue` 
	- bool `response` 



