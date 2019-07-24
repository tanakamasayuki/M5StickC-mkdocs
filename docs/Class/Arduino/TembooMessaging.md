# TembooMessaging



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_temboo_messaging.html)

## メンバー

### TembooMessaging()



```c
TembooMessaging::TembooMessaging(TembooSensor **sensors, int pinTableSize)
```

!!! summary "引数"
	- TembooSensor** `sensors` 
	- int `pinTableSize` 



### begin()



```c
void TembooMessaging::begin()
```



### setAccountName()



```c
void TembooMessaging::setAccountName(const String &accountName)
```

!!! summary "引数"
	- constString & `accountName` 



### setAccountName()



```c
void TembooMessaging::setAccountName(const char *accountName)
```

!!! summary "引数"
	- constchar * `accountName` 



### setAppKeyName()



```c
void TembooMessaging::setAppKeyName(const String &appKeyName)
```

!!! summary "引数"
	- constString & `appKeyName` 



### setAppKeyName()



```c
void TembooMessaging::setAppKeyName(const char *appKeyName)
```

!!! summary "引数"
	- constchar * `appKeyName` 



### setAppKey()



```c
void TembooMessaging::setAppKey(const String &appKey)
```

!!! summary "引数"
	- constString & `appKey` 



### setAppKey()



```c
void TembooMessaging::setAppKey(const char *appKey)
```

!!! summary "引数"
	- constchar * `appKey` 



### setDeviceID()



```c
void TembooMessaging::setDeviceID(const String &appKey)
```

!!! summary "引数"
	- constString & `appKey` 



### setDeviceID()



```c
void TembooMessaging::setDeviceID(const char *appKey)
```

!!! summary "引数"
	- constchar * `appKey` 



### initiateConnection()



```c
int TembooMessaging::initiateConnection()
```

!!! note "戻り値"
	int



### poll()



```c
WSMessageRequest TembooMessaging::poll()
```

!!! note "戻り値"
	WSMessageRequest



### sendData()



```c
void TembooMessaging::sendData(int pin, float pinVal)
```

!!! summary "引数"
	- int `pin` 
	- float `pinVal` 



### updatePinValue()



```c
void TembooMessaging::updatePinValue(int pinNum, int pinVal)
```

!!! summary "引数"
	- int `pinNum` 
	- int `pinVal` 



### retrievePinValue()



```c
int TembooMessaging::retrievePinValue(int pinNum)
```

!!! summary "引数"
	- int `pinNum` 

!!! note "戻り値"
	int



### addTembooSensor()



```c
int TembooMessaging::addTembooSensor(TembooSensor *sensor)
```

!!! summary "引数"
	- TembooSensor* `sensor` 

!!! note "戻り値"
	int



### setSensorsToDefaultState()



```c
void TembooMessaging::setSensorsToDefaultState()
```



### isConnected()



```c
bool TembooMessaging::isConnected()
```

!!! note "戻り値"
	bool



### sendData()



```c
void TembooMessaging::sendData(int pin, int pinVal, bool requestResponse=false)
```

!!! summary "引数"
	- int `pin` 
	- int `pinVal` 
	- bool `requestResponse` 



