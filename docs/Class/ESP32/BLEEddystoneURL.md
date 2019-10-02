# BLEEddystoneURL

Representation of a beacon. See: 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_eddystone_u_r_l.html)

## メンバー

###  frameType

```c
uint8_t BLEEddystoneURL::frameType
```


###  advertisedTxPower

```c
int8_t BLEEddystoneURL::advertisedTxPower
```


###  url

```c
uint8_t BLEEddystoneURL::url[16]
```


### BLEEddystoneURL()



```c
BLEEddystoneURL::BLEEddystoneURL()
```



### getData()



```c
std::string BLEEddystoneURL::getData()
```

!!! note "戻り値"
	std::string



### getUUID()



```c
BLEUUID BLEEddystoneURL::getUUID()
```

!!! note "戻り値"
	BLEUUID



### getPower()



```c
int8_t BLEEddystoneURL::getPower()
```

!!! note "戻り値"
	int8_t



### getURL()



```c
std::string BLEEddystoneURL::getURL()
```

!!! note "戻り値"
	std::string



### getDecodedURL()



```c
std::string BLEEddystoneURL::getDecodedURL()
```

!!! note "戻り値"
	std::string



### setData()


Set the raw data for the beacon record. 
```c
void BLEEddystoneURL::setData(std::string data)
```

!!! summary "引数"
	- std::string `data` 



### setUUID()



```c
void BLEEddystoneURL::setUUID(BLEUUID l_uuid)
```

!!! summary "引数"
	- BLEUUID `l_uuid` 



### setPower()



```c
void BLEEddystoneURL::setPower(int8_t advertisedTxPower)
```

!!! summary "引数"
	- int8_t `advertisedTxPower` 



### setURL()



```c
void BLEEddystoneURL::setURL(std::string url)
```

!!! summary "引数"
	- std::string `url` 



