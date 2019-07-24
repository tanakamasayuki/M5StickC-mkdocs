# BLEDescriptor

A model of a BLE descriptor. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_descriptor.html)

## メンバー

### BLEDescriptor()
constructor.


```c
BLEDescriptor::BLEDescriptor(const char *uuid, uint16_t max_len=100)
```

!!! summary "引数"
	- constchar * `uuid` 
	- uint16_t `max_len` 



### BLEDescriptor()
constructor.


```c
BLEDescriptor::BLEDescriptor(BLEUUID uuid, uint16_t max_len=100)
```

!!! summary "引数"
	- BLEUUID `uuid` 
	- uint16_t `max_len` 



### ~BLEDescriptor()
destructor.


```c
BLEDescriptor::~BLEDescriptor()
```



### getHandle()
Get the BLE handle for this descriptor.



```c
uint16_t BLEDescriptor::getHandle()
```

!!! note "戻り値"
	uint16_t The handle for this descriptor. 



### getLength()
Get the length of the value of this descriptor.



```c
size_t BLEDescriptor::getLength()
```

!!! note "戻り値"
	size_t The length (in bytes) of the value of this descriptor. 



### getUUID()
Get the UUID of the descriptor.


```c
BLEUUID BLEDescriptor::getUUID()
```

!!! note "戻り値"
	BLEUUID



### getValue()
Get the value of this descriptor.



```c
uint8_t * BLEDescriptor::getValue()
```

!!! note "戻り値"
	uint8_t* A pointer to the value of this descriptor. 



### handleGATTServerEvent()
Handle GATT server events for the descripttor.


```c
void BLEDescriptor::handleGATTServerEvent(esp_gatts_cb_event_t event, esp_gatt_if_t gatts_if, esp_ble_gatts_cb_param_t *param)
```

!!! summary "引数"
	- esp_gatts_cb_event_t `event` 
	- esp_gatt_if_t `gatts_if` 
	- esp_ble_gatts_cb_param_t* `param` 



### setAccessPermissions()



```c
void BLEDescriptor::setAccessPermissions(esp_gatt_perm_t perm)
```

!!! summary "引数"
	- esp_gatt_perm_t `perm` 



### setCallbacks()
Set the callback handlers for this descriptor.


```c
void BLEDescriptor::setCallbacks(BLEDescriptorCallbacks *pCallbacks)
```

!!! summary "引数"
	- BLEDescriptorCallbacks* `pCallbacks` An instance of a callback structure used to define any callbacks for the descriptor. 



### setValue()
Set the value of the descriptor.


```c
void BLEDescriptor::setValue(uint8_t *data, size_t size)
```

!!! summary "引数"
	- uint8_t* `data` The data to set for the descriptor. 
	- size_t `size` 



### setValue()
Set the value of the descriptor.


```c
void BLEDescriptor::setValue(std::string value)
```

!!! summary "引数"
	- std::string `value` The value of the descriptor in string form. 



### toString()
Return a string representation of the descriptor.



```c
std::string BLEDescriptor::toString()
```

!!! note "戻り値"
	std::string A string representation of the descriptor. 



