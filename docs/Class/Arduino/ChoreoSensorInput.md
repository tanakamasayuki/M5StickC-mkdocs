# ChoreoSensorInput



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_choreo_sensor_input.html)

## メンバー

### ChoreoSensorInput()



```c
ChoreoSensorInput::ChoreoSensorInput(ChoreoSensorInput *prev, const char *name, int value, const char *sensorConversion, const char *rawLow, const char *rawHigh, const char *scaleLow, const char *scaleHigh, const char *calibration)
```

!!! summary "引数"
	- ChoreoSensorInput* `prev` 
	- constchar * `name` 
	- int `value` 
	- constchar * `sensorConversion` 
	- constchar * `rawLow` 
	- constchar * `rawHigh` 
	- constchar * `scaleLow` 
	- constchar * `scaleHigh` 
	- constchar * `calibration` 



### getName()



```c
const char* ChoreoSensorInput::getName() const
```

!!! note "戻り値"
	constchar *



### getValue()



```c
const char* ChoreoSensorInput::getValue() const
```

!!! note "戻り値"
	constchar *



### getConversion()



```c
const char* ChoreoSensorInput::getConversion() const
```

!!! note "戻り値"
	constchar *



### getRawLow()



```c
const char* ChoreoSensorInput::getRawLow() const
```

!!! note "戻り値"
	constchar *



### getRawHigh()



```c
const char* ChoreoSensorInput::getRawHigh() const
```

!!! note "戻り値"
	constchar *



### getScaleLow()



```c
const char* ChoreoSensorInput::getScaleLow() const
```

!!! note "戻り値"
	constchar *



### getScaleHigh()



```c
const char* ChoreoSensorInput::getScaleHigh() const
```

!!! note "戻り値"
	constchar *



### getCalibration()



```c
const char* ChoreoSensorInput::getCalibration() const
```

!!! note "戻り値"
	constchar *



### setValue()



```c
void ChoreoSensorInput::setValue(int value)
```

!!! summary "引数"
	- int `value` 



### setConversion()



```c
void ChoreoSensorInput::setConversion(const char *conversion)
```

!!! summary "引数"
	- constchar * `conversion` 



### setRawLow()



```c
void ChoreoSensorInput::setRawLow(const char *value)
```

!!! summary "引数"
	- constchar * `value` 



### setRawHigh()



```c
void ChoreoSensorInput::setRawHigh(const char *value)
```

!!! summary "引数"
	- constchar * `value` 



### setScaleLow()



```c
void ChoreoSensorInput::setScaleLow(const char *value)
```

!!! summary "引数"
	- constchar * `value` 



### setScaleHigh()



```c
void ChoreoSensorInput::setScaleHigh(const char *value)
```

!!! summary "引数"
	- constchar * `value` 



### setCalibration()



```c
void ChoreoSensorInput::setCalibration(const char *value)
```

!!! summary "引数"
	- constchar * `value` 



### getNext()



```c
ChoreoSensorInput* ChoreoSensorInput::getNext() const
```

!!! note "戻り値"
	ChoreoSensorInput*



