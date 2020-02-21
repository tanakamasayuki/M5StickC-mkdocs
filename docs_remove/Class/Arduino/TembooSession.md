# TembooSession



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_temboo_session.html)

## メンバー

### TembooSession()



```c
TembooSession::TembooSession(Client &client, IPAddress serverAddr=INADDR_NONE, uint16_t port=80)
```

!!! summary "引数"
	- Client& `client` 
	- IPAddress `serverAddr` 
	- uint16_t `port` 



### executeChoreo()



```c
int TembooSession::executeChoreo(const char *accountName, const char *appKeyName, const char *appKeyValue, const char *path, const ChoreoInputSet &inputSet, const ChoreoInputExpressionSet &expressionSet, const ChoreoSensorInputSet &sensorSet, const ChoreoOutputSet &outputSet, const ChoreoPreset &preset, const ChoreoDevice &deviceType, const ChoreoDevice &deviceName)
```

!!! summary "引数"
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
void TembooSession::setTime(unsigned long currentTime)
```

!!! summary "引数"
	- unsigned long `currentTime` 



### getTime()



```c
unsigned long TembooSession::getTime()
```

!!! note "戻り値"
	unsigned long



