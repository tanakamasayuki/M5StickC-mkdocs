# DataFormatter



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_data_formatter.html)

## メンバー

### DataFormatter()



```c
DataFormatter::DataFormatter(const ChoreoInputSet *inputSet, const ChoreoInputExpressionSet *expressionSet, const ChoreoSensorInputSet *sensorSet, const ChoreoOutputSet *outputSet, const ChoreoPreset *preset, const ChoreoDevice *device, const ChoreoDevice *deviceName)
```

!!! summary "引数"
	- const* `inputSet` 
	- const* `expressionSet` 
	- const* `sensorSet` 
	- const* `outputSet` 
	- const* `preset` 
	- const* `device` 
	- const* `deviceName` 



### hasNext()



```c
bool DataFormatter::hasNext()
```

!!! note "戻り値"
	bool



### next()



```c
char DataFormatter::next()
```

!!! note "戻り値"
	char



### reset()



```c
void DataFormatter::reset()
```



