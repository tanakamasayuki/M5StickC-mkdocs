# TembooCoAPSession



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_temboo_co_a_p_session.html)

## メンバー



### TembooCoAPSession()



```c
TembooCoAPSession::TembooCoAPSession(TembooCoAPClient &client)
```

!!! summary "引数"
	- TembooCoAPClient& `client` 



### executeChoreo()



```c
int TembooCoAPSession::executeChoreo(uint16_t requestId, const char *accountName, const char *appKeyName, const char *appKeyValue, const char *path, const ChoreoInputSet &inputSet, const ChoreoInputExpressionSet &expressionSet, const ChoreoSensorInputSet &sensorSet, const ChoreoOutputSet &outputSet, const ChoreoPreset &preset, const ChoreoDevice &deviceType, const ChoreoDevice &deviceName)
```

!!! summary "引数"
	- uint16_t `requestId` 
	- constchar * `accountName` 
	- constchar * `appKeyName` 
	- constchar * `appKeyValue` 
	- constchar * `path` 
	- const& `inputSet` 
	- const& `expressionSet` 
	- const& `sensorSet` 
	- const& `outputSet` 
	- const& `preset` 
	- const& `deviceType` 
	- const& `deviceName` 

!!! note "戻り値"
	int



### setTime()



```c
void TembooCoAPSession::setTime(unsigned long currentTime)
```

!!! summary "引数"
	- unsigned long `currentTime` 



### getTime()



```c
unsigned long TembooCoAPSession::getTime()
```

!!! note "戻り値"
	unsigned long



