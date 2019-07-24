# CPlay_CapacitiveSensor

Class that stores state and functions for the capacitive sensor on CircuitPlayground boards 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_c_play___capacitive_sensor.html)

## メンバー

### CPlay_CapacitiveSensor()
Function that handles the creation and setup of instances


```c
CPlay_CapacitiveSensor::CPlay_CapacitiveSensor(uint8_t sendPin=0, uint8_t receivePin=0)
```

!!! summary "引数"
	- uint8_t `sendPin` send pin for the sensor 
	- uint8_t `receivePin` the receiving pin for the sensor 



### capacitiveSensorRaw()
get a raw sensor reading


```c
long CPlay_CapacitiveSensor::capacitiveSensorRaw(uint8_t samples)
```

!!! summary "引数"
	- uint8_t `samples` the number of samples to take 

!!! note "戻り値"
	long -1 for error, -2 for timeout, other values are a raw sensor reading 



### capacitiveSensor()
get a capacitive sensor reading


```c
long CPlay_CapacitiveSensor::capacitiveSensor(uint8_t samples)
```

!!! summary "引数"
	- uint8_t `samples` number of samples to take 

!!! note "戻り値"
	long the sensor reading 



### set_CS_Timeout_Millis()
set the sensor timeout


```c
void CPlay_CapacitiveSensor::set_CS_Timeout_Millis(unsigned long timeout_millis)
```

!!! summary "引数"
	- unsigned long `timeout_millis` the number of milliseconds to set the timeout to 



### reset_CS_AutoCal()
reset the auto calibration


```c
void CPlay_CapacitiveSensor::reset_CS_AutoCal()
```



### set_CS_AutocaL_Millis()
set the auto-calibration time


```c
void CPlay_CapacitiveSensor::set_CS_AutocaL_Millis(unsigned long autoCal_millis)
```

!!! summary "引数"
	- unsigned long `autoCal_millis` the desired calibration time in milliseconds 



