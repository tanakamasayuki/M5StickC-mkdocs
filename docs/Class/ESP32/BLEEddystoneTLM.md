# BLEEddystoneTLM

Representation of a beacon. See: 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_eddystone_t_l_m.html)

## メンバー

###  frameType

```c
uint8_t BLEEddystoneTLM::frameType
```


###  version

```c
uint8_t BLEEddystoneTLM::version
```


###  volt

```c
uint16_t BLEEddystoneTLM::volt
```


###  temp

```c
uint16_t BLEEddystoneTLM::temp
```


###  advCount

```c
uint32_t BLEEddystoneTLM::advCount
```


###  tmil

```c
uint32_t BLEEddystoneTLM::tmil
```


### BLEEddystoneTLM()



```c
BLEEddystoneTLM::BLEEddystoneTLM()
```



### getData()



```c
std::string BLEEddystoneTLM::getData()
```

!!! note "戻り値"
	std::string



### getUUID()



```c
BLEUUID BLEEddystoneTLM::getUUID()
```

!!! note "戻り値"
	BLEUUID



### getVersion()



```c
uint8_t BLEEddystoneTLM::getVersion()
```

!!! note "戻り値"
	uint8_t



### getVolt()



```c
uint16_t BLEEddystoneTLM::getVolt()
```

!!! note "戻り値"
	uint16_t



### getTemp()



```c
float BLEEddystoneTLM::getTemp()
```

!!! note "戻り値"
	float



### getCount()



```c
uint32_t BLEEddystoneTLM::getCount()
```

!!! note "戻り値"
	uint32_t



### getTime()



```c
uint32_t BLEEddystoneTLM::getTime()
```

!!! note "戻り値"
	uint32_t



### toString()



```c
std::string BLEEddystoneTLM::toString()
```

!!! note "戻り値"
	std::string



### setData()


Set the raw data for the beacon record. 
```c
void BLEEddystoneTLM::setData(std::string data)
```

!!! summary "引数"
	- std::string `data` 



### setUUID()



```c
void BLEEddystoneTLM::setUUID(BLEUUID l_uuid)
```

!!! summary "引数"
	- BLEUUID `l_uuid` 



### setVersion()



```c
void BLEEddystoneTLM::setVersion(uint8_t version)
```

!!! summary "引数"
	- uint8_t `version` 



### setVolt()



```c
void BLEEddystoneTLM::setVolt(uint16_t volt)
```

!!! summary "引数"
	- uint16_t `volt` 



### setTemp()



```c
void BLEEddystoneTLM::setTemp(float temp)
```

!!! summary "引数"
	- float `temp` 



### setCount()



```c
void BLEEddystoneTLM::setCount(uint32_t advCount)
```

!!! summary "引数"
	- uint32_t `advCount` 



### setTime()



```c
void BLEEddystoneTLM::setTime(uint32_t tmil)
```

!!! summary "引数"
	- uint32_t `tmil` 



