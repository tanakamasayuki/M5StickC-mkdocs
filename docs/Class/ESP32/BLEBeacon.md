# BLEBeacon

Representation of a beacon. See: 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_beacon.html)

## メンバー

###  manufacturerId

```c
uint16_t BLEBeacon::manufacturerId
```


###  subType

```c
uint8_t BLEBeacon::subType
```


###  subTypeLength

```c
uint8_t BLEBeacon::subTypeLength
```


###  proximityUUID

```c
uint8_t BLEBeacon::proximityUUID[16]
```


###  major

```c
uint16_t BLEBeacon::major
```


###  minor

```c
uint16_t BLEBeacon::minor
```


###  signalPower

```c
int8_t BLEBeacon::signalPower
```


### BLEBeacon()



```c
BLEBeacon::BLEBeacon()
```



### getData()



```c
std::string BLEBeacon::getData()
```

!!! note "戻り値"
	std::string



### getMajor()



```c
uint16_t BLEBeacon::getMajor()
```

!!! note "戻り値"
	uint16_t



### getMinor()



```c
uint16_t BLEBeacon::getMinor()
```

!!! note "戻り値"
	uint16_t



### getManufacturerId()



```c
uint16_t BLEBeacon::getManufacturerId()
```

!!! note "戻り値"
	uint16_t



### getProximityUUID()



```c
BLEUUID BLEBeacon::getProximityUUID()
```

!!! note "戻り値"
	BLEUUID



### getSignalPower()



```c
int8_t BLEBeacon::getSignalPower()
```

!!! note "戻り値"
	int8_t



### setData()


Set the raw data for the beacon record. 
```c
void BLEBeacon::setData(std::string data)
```

!!! summary "引数"
	- std::string `data` 



### setMajor()



```c
void BLEBeacon::setMajor(uint16_t major)
```

!!! summary "引数"
	- uint16_t `major` 



### setMinor()



```c
void BLEBeacon::setMinor(uint16_t minor)
```

!!! summary "引数"
	- uint16_t `minor` 



### setManufacturerId()



```c
void BLEBeacon::setManufacturerId(uint16_t manufacturerId)
```

!!! summary "引数"
	- uint16_t `manufacturerId` 



### setProximityUUID()



```c
void BLEBeacon::setProximityUUID(BLEUUID uuid)
```

!!! summary "引数"
	- BLEUUID `uuid` 



### setSignalPower()



```c
void BLEBeacon::setSignalPower(int8_t signalPower)
```

!!! summary "引数"
	- int8_t `signalPower` 



