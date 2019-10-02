# BLERemoteCharacteristic

A model of a remote BLE characteristic. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_remote_characteristic.html)

## メンバー

### ~BLERemoteCharacteristic()
Destructor.


```c
BLERemoteCharacteristic::~BLERemoteCharacteristic()
```



### canBroadcast()
Does the characteristic support broadcasting?



```c
bool BLERemoteCharacteristic::canBroadcast()
```

!!! note "戻り値"
	bool True if the characteristic supports broadcasting. 



### canIndicate()
Does the characteristic support indications?



```c
bool BLERemoteCharacteristic::canIndicate()
```

!!! note "戻り値"
	bool True if the characteristic supports indications. 



### canNotify()
Does the characteristic support notifications?



```c
bool BLERemoteCharacteristic::canNotify()
```

!!! note "戻り値"
	bool True if the characteristic supports notifications. 



### canRead()
Does the characteristic support reading?



```c
bool BLERemoteCharacteristic::canRead()
```

!!! note "戻り値"
	bool True if the characteristic supports reading. 



### canWrite()
Does the characteristic support writing?



```c
bool BLERemoteCharacteristic::canWrite()
```

!!! note "戻り値"
	bool True if the characteristic supports writing. 



### canWriteNoResponse()
Does the characteristic support writing with no response?



```c
bool BLERemoteCharacteristic::canWriteNoResponse()
```

!!! note "戻り値"
	bool True if the characteristic supports writing with no response. 



### getDescriptor()
Get the descriptor instance with the given UUID that belongs to this characteristic.


```c
BLERemoteDescriptor * BLERemoteCharacteristic::getDescriptor(BLEUUID uuid)
```

!!! summary "引数"
	- BLEUUID `uuid` The UUID of the descriptor to find. 

!!! note "戻り値"
	BLERemoteDescriptor* The Remote descriptor (if present) or null if not present. 



### getDescriptors()
Retrieve the map of descriptors keyed by UUID.


```c
std::map< std::string, BLERemoteDescriptor * > * BLERemoteCharacteristic::getDescriptors()
```

!!! note "戻り値"
	std::map< ,  * > *



### getHandle()
Get the handle for this characteristic.



```c
uint16_t BLERemoteCharacteristic::getHandle()
```

!!! note "戻り値"
	uint16_t The handle for this characteristic. 



### getUUID()
Get the UUID for this characteristic.



```c
BLEUUID BLERemoteCharacteristic::getUUID()
```

!!! note "戻り値"
	BLEUUID The UUID for this characteristic. 



### readValue()
Read the value of the remote characteristic.



```c
std::string BLERemoteCharacteristic::readValue()
```

!!! note "戻り値"
	std::string The value of the remote characteristic. 



### readUInt8()
Read a byte value



```c
uint8_t BLERemoteCharacteristic::readUInt8()
```

!!! note "戻り値"
	uint8_t The value as a byte 



### readUInt16()
Read an unsigned 16 bit value



```c
uint16_t BLERemoteCharacteristic::readUInt16()
```

!!! note "戻り値"
	uint16_t The unsigned 16 bit value. 



### readUInt32()
Read an unsigned 32 bit value.



```c
uint32_t BLERemoteCharacteristic::readUInt32()
```

!!! note "戻り値"
	uint32_t the unsigned 32 bit value. 



### registerForNotify()
Register for notifications.


```c
void BLERemoteCharacteristic::registerForNotify(notify_callback _callback, bool notifications=true)
```

!!! summary "引数"
	- notify_callback `_callback` 
	- bool `notifications` 



### writeValue()
Write the new value for the characteristic from a data buffer.


```c
void BLERemoteCharacteristic::writeValue(uint8_t *data, size_t length, bool response=false)
```

!!! summary "引数"
	- uint8_t* `data` A pointer to a data buffer. 
	- size_t `length` The length of the data in the data buffer. 
	- bool `response` Whether we require a response from the write. 



### writeValue()
Write the new value for the characteristic.


```c
void BLERemoteCharacteristic::writeValue(std::string newValue, bool response=false)
```

!!! summary "引数"
	- std::string `newValue` The new value to write. 
	- bool `response` Do we expect a response? 



### writeValue()
Write the new value for the characteristic.


```c
void BLERemoteCharacteristic::writeValue(uint8_t newValue, bool response=false)
```

!!! summary "引数"
	- uint8_t `newValue` The new byte value to write. 
	- bool `response` Whether we require a response from the write. 



### toString()
Convert a  to a string representation;



```c
std::string BLERemoteCharacteristic::toString()
```

!!! note "戻り値"
	std::string a String representation. 



### readRawData()
Read raw data from remote characteristic as hex bytes



```c
uint8_t * BLERemoteCharacteristic::readRawData()
```

!!! note "戻り値"
	uint8_t* return pointer data read 



