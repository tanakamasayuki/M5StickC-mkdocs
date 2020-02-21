# ChoreoSensorInputSet



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_choreo_sensor_input_set.html)

## メンバー

### ChoreoSensorInputSet()



```c
ChoreoSensorInputSet::ChoreoSensorInputSet()
```



### ~ChoreoSensorInputSet()



```c
ChoreoSensorInputSet::~ChoreoSensorInputSet()
```



### put()



```c
void ChoreoSensorInputSet::put(const char *name, int value, const char *sensorConversion, const char *rawLow, const char *rawHigh, const char *scaleLow, const char *scaleHigh, const char *calibration)
```

!!! summary "引数"
	- constchar * `name` 
	- int `value` 
	- constchar * `sensorConversion` 
	- constchar * `rawLow` 
	- constchar * `rawHigh` 
	- constchar * `scaleLow` 
	- constchar * `scaleHigh` 
	- constchar * `calibration` 



### get()



```c
const char * ChoreoSensorInputSet::get(const char *name) const
```

!!! summary "引数"
	- constchar * `name` 

!!! note "戻り値"
	constchar *



### isEmpty()



```c
bool ChoreoSensorInputSet::isEmpty() const
```

!!! note "戻り値"
	bool



### getFirstInput()



```c
const ChoreoSensorInput* ChoreoSensorInputSet::getFirstInput() const
```

!!! note "戻り値"
	const*



