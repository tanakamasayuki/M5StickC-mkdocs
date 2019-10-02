# BLEHIDDevice



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_h_i_d_device.html)

## メンバー

### BLEHIDDevice()



```c
BLEHIDDevice::BLEHIDDevice(BLEServer *)
```

!!! summary "引数"
	- BLEServer* `` 



### ~BLEHIDDevice()



```c
BLEHIDDevice::~BLEHIDDevice()
```



### reportMap()



```c
void BLEHIDDevice::reportMap(uint8_t *map, uint16_t)
```

!!! summary "引数"
	- uint8_t* `map` 
	- uint16_t `` 



### startServices()



```c
void BLEHIDDevice::startServices()
```



### deviceInfo()



```c
BLEService * BLEHIDDevice::deviceInfo()
```

!!! note "戻り値"
	BLEService*



### hidService()



```c
BLEService * BLEHIDDevice::hidService()
```

!!! note "戻り値"
	BLEService*



### batteryService()



```c
BLEService * BLEHIDDevice::batteryService()
```

!!! note "戻り値"
	BLEService*



### manufacturer()



```c
BLECharacteristic * BLEHIDDevice::manufacturer()
```

!!! note "戻り値"
	BLECharacteristic*



### manufacturer()



```c
void BLEHIDDevice::manufacturer(std::string name)
```

!!! summary "引数"
	- std::string `name` 



### pnp()



```c
void BLEHIDDevice::pnp(uint8_t sig, uint16_t vid, uint16_t pid, uint16_t version)
```

!!! summary "引数"
	- uint8_t `sig` 
	- uint16_t `vid` 
	- uint16_t `pid` 
	- uint16_t `version` 



### hidInfo()



```c
void BLEHIDDevice::hidInfo(uint8_t country, uint8_t flags)
```

!!! summary "引数"
	- uint8_t `country` 
	- uint8_t `flags` 



### setBatteryLevel()



```c
void BLEHIDDevice::setBatteryLevel(uint8_t level)
```

!!! summary "引数"
	- uint8_t `level` 



### hidControl()



```c
BLECharacteristic * BLEHIDDevice::hidControl()
```

!!! note "戻り値"
	BLECharacteristic*



### inputReport()



```c
BLECharacteristic * BLEHIDDevice::inputReport(uint8_t reportID)
```

!!! summary "引数"
	- uint8_t `reportID` 

!!! note "戻り値"
	BLECharacteristic*



### outputReport()



```c
BLECharacteristic * BLEHIDDevice::outputReport(uint8_t reportID)
```

!!! summary "引数"
	- uint8_t `reportID` 

!!! note "戻り値"
	BLECharacteristic*



### featureReport()



```c
BLECharacteristic * BLEHIDDevice::featureReport(uint8_t reportID)
```

!!! summary "引数"
	- uint8_t `reportID` 

!!! note "戻り値"
	BLECharacteristic*



### protocolMode()



```c
BLECharacteristic * BLEHIDDevice::protocolMode()
```

!!! note "戻り値"
	BLECharacteristic*



### bootInput()



```c
BLECharacteristic * BLEHIDDevice::bootInput()
```

!!! note "戻り値"
	BLECharacteristic*



### bootOutput()



```c
BLECharacteristic * BLEHIDDevice::bootOutput()
```

!!! note "戻り値"
	BLECharacteristic*



