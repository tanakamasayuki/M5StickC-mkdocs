# TembooChoreo



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_temboo_choreo.html)

## メンバー

### TembooChoreo()



```c
TembooChoreo::TembooChoreo(Client &client)
```

!!! summary "引数"
	- Client& `client` 



### begin()



```c
void TembooChoreo::begin()
```



### setAccountName()



```c
void TembooChoreo::setAccountName(const String &accountName)
```

!!! summary "引数"
	- constString & `accountName` 



### setAccountName()



```c
void TembooChoreo::setAccountName(const char *accountName)
```

!!! summary "引数"
	- constchar * `accountName` 



### setAppKeyName()



```c
void TembooChoreo::setAppKeyName(const String &appKeyName)
```

!!! summary "引数"
	- constString & `appKeyName` 



### setAppKeyName()



```c
void TembooChoreo::setAppKeyName(const char *appKeyName)
```

!!! summary "引数"
	- constchar * `appKeyName` 



### setAppKey()



```c
void TembooChoreo::setAppKey(const String &appKey)
```

!!! summary "引数"
	- constString & `appKey` 



### setAppKey()



```c
void TembooChoreo::setAppKey(const char *appKey)
```

!!! summary "引数"
	- constchar * `appKey` 



### setChoreo()



```c
void TembooChoreo::setChoreo(const String &choreoPath)
```

!!! summary "引数"
	- constString & `choreoPath` 



### setChoreo()



```c
void TembooChoreo::setChoreo(const char *choreoPath)
```

!!! summary "引数"
	- constchar * `choreoPath` 



### setSavedInputs()



```c
void TembooChoreo::setSavedInputs(const String &savedInputsName)
```

!!! summary "引数"
	- constString & `savedInputsName` 



### setSavedInputs()



```c
void TembooChoreo::setSavedInputs(const char *savedInputsName)
```

!!! summary "引数"
	- constchar * `savedInputsName` 



### setCredential()



```c
void TembooChoreo::setCredential(const String &credentialName)
```

!!! summary "引数"
	- constString & `credentialName` 



### setCredential()



```c
void TembooChoreo::setCredential(const char *credentialName)
```

!!! summary "引数"
	- constchar * `credentialName` 



### setProfile()



```c
void TembooChoreo::setProfile(const String &profileName)
```

!!! summary "引数"
	- constString & `profileName` 



### setProfile()



```c
void TembooChoreo::setProfile(const char *profileName)
```

!!! summary "引数"
	- constchar * `profileName` 



### setDeviceType()



```c
void TembooChoreo::setDeviceType(const String &deviceType)
```

!!! summary "引数"
	- constString & `deviceType` 



### setDeviceType()



```c
void TembooChoreo::setDeviceType(const char *deviceType)
```

!!! summary "引数"
	- constchar * `deviceType` 



### setDeviceName()



```c
void TembooChoreo::setDeviceName(const String &deviceName)
```

!!! summary "引数"
	- constString & `deviceName` 



### setDeviceName()



```c
void TembooChoreo::setDeviceName(const char *deviceName)
```

!!! summary "引数"
	- constchar * `deviceName` 



### addInput()



```c
void TembooChoreo::addInput(const String &inputName, const String &inputValue)
```

!!! summary "引数"
	- constString & `inputName` 
	- constString & `inputValue` 



### addInput()



```c
void TembooChoreo::addInput(const char *inputName, const char *inputValue)
```

!!! summary "引数"
	- constchar * `inputName` 
	- constchar * `inputValue` 



### addInput()



```c
void TembooChoreo::addInput(const char *inputName, const String &inputValue)
```

!!! summary "引数"
	- constchar * `inputName` 
	- constString & `inputValue` 



### addInput()



```c
void TembooChoreo::addInput(const String &inputName, const char *inputValue)
```

!!! summary "引数"
	- constString & `inputName` 
	- constchar * `inputValue` 



### addInputWithSensor()



```c
void TembooChoreo::addInputWithSensor(const String &inputName, const String &inputValue)
```

!!! summary "引数"
	- constString & `inputName` 
	- constString & `inputValue` 



### addInputWithSensor()



```c
void TembooChoreo::addInputWithSensor(const char *inputName, const String &inputValue)
```

!!! summary "引数"
	- constchar * `inputName` 
	- constString & `inputValue` 



### addInputWithSensor()



```c
void TembooChoreo::addInputWithSensor(const char *inputName, const char *inputValue)
```

!!! summary "引数"
	- constchar * `inputName` 
	- constchar * `inputValue` 



### addInputExpression()



```c
void TembooChoreo::addInputExpression(const String &inputName, const String &inputValue)
```

!!! summary "引数"
	- constString & `inputName` 
	- constString & `inputValue` 



### addInputExpression()



```c
void TembooChoreo::addInputExpression(const char *inputName, const String &inputValue)
```

!!! summary "引数"
	- constchar * `inputName` 
	- constString & `inputValue` 



### addInputExpression()



```c
void TembooChoreo::addInputExpression(const char *inputName, const char *inputValue)
```

!!! summary "引数"
	- constchar * `inputName` 
	- constchar * `inputValue` 



### addSensorValue()



```c
void TembooChoreo::addSensorValue(const char *sensorName, int sensorValue, const char *conversion)
```

!!! summary "引数"
	- constchar * `sensorName` 
	- int `sensorValue` 
	- constchar * `conversion` 



### addSensorValue()



```c
void TembooChoreo::addSensorValue(const char *sensorName, int sensorValue)
```

!!! summary "引数"
	- constchar * `sensorName` 
	- int `sensorValue` 



### addSensorValue()



```c
void TembooChoreo::addSensorValue(const char *sensorName, int sensorValue, const char *conversion, const char *calibrationValue)
```

!!! summary "引数"
	- constchar * `sensorName` 
	- int `sensorValue` 
	- constchar * `conversion` 
	- constchar * `calibrationValue` 



### addSensorValue()



```c
void TembooChoreo::addSensorValue(const char *sensorName, int sensorValue, const char *rawLow, const char *rawHigh, const char *scaleLow, const char *scaleHigh)
```

!!! summary "引数"
	- constchar * `sensorName` 
	- int `sensorValue` 
	- constchar * `rawLow` 
	- constchar * `rawHigh` 
	- constchar * `scaleLow` 
	- constchar * `scaleHigh` 



### addSensorInput()



```c
void TembooChoreo::addSensorInput(const char *sensorName, int sensorValue, const char *conversion)
```

!!! summary "引数"
	- constchar * `sensorName` 
	- int `sensorValue` 
	- constchar * `conversion` 



### addSensorInput()



```c
void TembooChoreo::addSensorInput(const char *sensorName, int sensorValue)
```

!!! summary "引数"
	- constchar * `sensorName` 
	- int `sensorValue` 



### addSensorInput()



```c
void TembooChoreo::addSensorInput(const char *sensorName, int sensorValue, const char *conversion, const char *calibrationValue)
```

!!! summary "引数"
	- constchar * `sensorName` 
	- int `sensorValue` 
	- constchar * `conversion` 
	- constchar * `calibrationValue` 



### addSensorInput()



```c
void TembooChoreo::addSensorInput(const char *sensorName, int sensorValue, const char *rawLow, const char *rawHigh, const char *scaleLow, const char *scaleHigh)
```

!!! summary "引数"
	- constchar * `sensorName` 
	- int `sensorValue` 
	- constchar * `rawLow` 
	- constchar * `rawHigh` 
	- constchar * `scaleLow` 
	- constchar * `scaleHigh` 



### addOutputFilter()



```c
void TembooChoreo::addOutputFilter(const char *filterName, const char *filterPath, const char *variableName)
```

!!! summary "引数"
	- constchar * `filterName` 
	- constchar * `filterPath` 
	- constchar * `variableName` 



### addOutputFilter()



```c
void TembooChoreo::addOutputFilter(const String &filterName, const char *filterPath, const char *variableName)
```

!!! summary "引数"
	- constString & `filterName` 
	- constchar * `filterPath` 
	- constchar * `variableName` 



### addOutputFilter()



```c
void TembooChoreo::addOutputFilter(const char *filterName, const String &filterPath, const char *variableName)
```

!!! summary "引数"
	- constchar * `filterName` 
	- constString & `filterPath` 
	- constchar * `variableName` 



### addOutputFilter()



```c
void TembooChoreo::addOutputFilter(const String &filterName, const String &filterPath, const char *variableName)
```

!!! summary "引数"
	- constString & `filterName` 
	- constString & `filterPath` 
	- constchar * `variableName` 



### addOutputFilter()



```c
void TembooChoreo::addOutputFilter(const char *filterName, const char *filterPath, const String &variableName)
```

!!! summary "引数"
	- constchar * `filterName` 
	- constchar * `filterPath` 
	- constString & `variableName` 



### addOutputFilter()



```c
void TembooChoreo::addOutputFilter(const String &filterName, const char *filterPath, const String &variableName)
```

!!! summary "引数"
	- constString & `filterName` 
	- constchar * `filterPath` 
	- constString & `variableName` 



### addOutputFilter()



```c
void TembooChoreo::addOutputFilter(const char *filterName, const String &filterPath, const String &variableName)
```

!!! summary "引数"
	- constchar * `filterName` 
	- constString & `filterPath` 
	- constString & `variableName` 



### addOutputFilter()



```c
void TembooChoreo::addOutputFilter(const String &filterName, const String &filterPath, const String &variableName)
```

!!! summary "引数"
	- constString & `filterName` 
	- constString & `filterPath` 
	- constString & `variableName` 



### run()



```c
int TembooChoreo::run()
```

!!! note "戻り値"
	int



### run()



```c
int TembooChoreo::run(uint16_t timeoutSecs)
```

!!! summary "引数"
	- uint16_t `timeoutSecs` 

!!! note "戻り値"
	int



### run()



```c
int TembooChoreo::run(IPAddress addr, uint16_t port)
```

!!! summary "引数"
	- IPAddress `addr` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### run()



```c
int TembooChoreo::run(IPAddress addr, uint16_t port, uint16_t timeoutSecs)
```

!!! summary "引数"
	- IPAddress `addr` 
	- uint16_t `port` 
	- uint16_t `timeoutSecs` 

!!! note "戻り値"
	int



### close()



```c
void TembooChoreo::close()
```



### available()



```c
int TembooChoreo::available()
```

!!! note "戻り値"
	int



### read()



```c
int TembooChoreo::read()
```

!!! note "戻り値"
	int



### peek()



```c
int TembooChoreo::peek()
```

!!! note "戻り値"
	int



### flush()



```c
void TembooChoreo::flush()
```



### write()



```c
size_t TembooChoreo::write(uint8_t data)
```

!!! summary "引数"
	- uint8_t `data` 

!!! note "戻り値"
	size_t



