# TembooMQTTChoreo



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_temboo_m_q_t_t_choreo.html)

## メンバー

### TembooMQTTChoreo()



```c
TembooMQTTChoreo::TembooMQTTChoreo(TembooMQTTClient &client)
```

!!! summary "引数"
	- TembooMQTTClient& `client` 



### ~TembooMQTTChoreo()



```c
TembooMQTTChoreo::~TembooMQTTChoreo()
```



### begin()



```c
void TembooMQTTChoreo::begin()
```



### setAccountName()



```c
void TembooMQTTChoreo::setAccountName(const String &accountName)
```

!!! summary "引数"
	- constString & `accountName` 



### setAccountName()



```c
void TembooMQTTChoreo::setAccountName(const char *accountName)
```

!!! summary "引数"
	- constchar * `accountName` 



### setAppKeyName()



```c
void TembooMQTTChoreo::setAppKeyName(const String &appKeyName)
```

!!! summary "引数"
	- constString & `appKeyName` 



### setAppKeyName()



```c
void TembooMQTTChoreo::setAppKeyName(const char *appKeyName)
```

!!! summary "引数"
	- constchar * `appKeyName` 



### setAppKey()



```c
void TembooMQTTChoreo::setAppKey(const String &appKey)
```

!!! summary "引数"
	- constString & `appKey` 



### setAppKey()



```c
void TembooMQTTChoreo::setAppKey(const char *appKey)
```

!!! summary "引数"
	- constchar * `appKey` 



### setChoreo()



```c
void TembooMQTTChoreo::setChoreo(const String &choreoPath)
```

!!! summary "引数"
	- constString & `choreoPath` 



### setChoreo()



```c
void TembooMQTTChoreo::setChoreo(const char *choreoPath)
```

!!! summary "引数"
	- constchar * `choreoPath` 



### setSavedInputs()



```c
void TembooMQTTChoreo::setSavedInputs(const String &savedInputsName)
```

!!! summary "引数"
	- constString & `savedInputsName` 



### setSavedInputs()



```c
void TembooMQTTChoreo::setSavedInputs(const char *savedInputsName)
```

!!! summary "引数"
	- constchar * `savedInputsName` 



### setCredential()



```c
void TembooMQTTChoreo::setCredential(const String &credentialName)
```

!!! summary "引数"
	- constString & `credentialName` 



### setCredential()



```c
void TembooMQTTChoreo::setCredential(const char *credentialName)
```

!!! summary "引数"
	- constchar * `credentialName` 



### setProfile()



```c
void TembooMQTTChoreo::setProfile(const String &profileName)
```

!!! summary "引数"
	- constString & `profileName` 



### setProfile()



```c
void TembooMQTTChoreo::setProfile(const char *profileName)
```

!!! summary "引数"
	- constchar * `profileName` 



### addInput()



```c
void TembooMQTTChoreo::addInput(const String &inputName, const String &inputValue)
```

!!! summary "引数"
	- constString & `inputName` 
	- constString & `inputValue` 



### addInput()



```c
void TembooMQTTChoreo::addInput(const char *inputName, const char *inputValue)
```

!!! summary "引数"
	- constchar * `inputName` 
	- constchar * `inputValue` 



### addInput()



```c
void TembooMQTTChoreo::addInput(const char *inputName, const String &inputValue)
```

!!! summary "引数"
	- constchar * `inputName` 
	- constString & `inputValue` 



### addInput()



```c
void TembooMQTTChoreo::addInput(const String &inputName, const char *inputValue)
```

!!! summary "引数"
	- constString & `inputName` 
	- constchar * `inputValue` 



### addOutputFilter()



```c
void TembooMQTTChoreo::addOutputFilter(const char *filterName, const char *filterPath, const char *variableName)
```

!!! summary "引数"
	- constchar * `filterName` 
	- constchar * `filterPath` 
	- constchar * `variableName` 



### addOutputFilter()



```c
void TembooMQTTChoreo::addOutputFilter(const String &filterName, const char *filterPath, const char *variableName)
```

!!! summary "引数"
	- constString & `filterName` 
	- constchar * `filterPath` 
	- constchar * `variableName` 



### addOutputFilter()



```c
void TembooMQTTChoreo::addOutputFilter(const char *filterName, const String &filterPath, const char *variableName)
```

!!! summary "引数"
	- constchar * `filterName` 
	- constString & `filterPath` 
	- constchar * `variableName` 



### addOutputFilter()



```c
void TembooMQTTChoreo::addOutputFilter(const String &filterName, const String &filterPath, const char *variableName)
```

!!! summary "引数"
	- constString & `filterName` 
	- constString & `filterPath` 
	- constchar * `variableName` 



### addOutputFilter()



```c
void TembooMQTTChoreo::addOutputFilter(const char *filterName, const char *filterPath, const String &variableName)
```

!!! summary "引数"
	- constchar * `filterName` 
	- constchar * `filterPath` 
	- constString & `variableName` 



### addOutputFilter()



```c
void TembooMQTTChoreo::addOutputFilter(const String &filterName, const char *filterPath, const String &variableName)
```

!!! summary "引数"
	- constString & `filterName` 
	- constchar * `filterPath` 
	- constString & `variableName` 



### addOutputFilter()



```c
void TembooMQTTChoreo::addOutputFilter(const char *filterName, const String &filterPath, const String &variableName)
```

!!! summary "引数"
	- constchar * `filterName` 
	- constString & `filterPath` 
	- constString & `variableName` 



### addOutputFilter()



```c
void TembooMQTTChoreo::addOutputFilter(const String &filterName, const String &filterPath, const String &variableName)
```

!!! summary "引数"
	- constString & `filterName` 
	- constString & `filterPath` 
	- constString & `variableName` 



### run()



```c
int TembooMQTTChoreo::run(uint16_t timeoutSecs)
```

!!! summary "引数"
	- uint16_t `timeoutSecs` 

!!! note "戻り値"
	int



### getResponseData()



```c
char* TembooMQTTChoreo::getResponseData()
```

!!! note "戻り値"
	char *



### getHTTPResponseCode()



```c
char* TembooMQTTChoreo::getHTTPResponseCode()
```

!!! note "戻り値"
	char *



### close()



```c
void TembooMQTTChoreo::close()
```



### available()



```c
int TembooMQTTChoreo::available()
```

!!! note "戻り値"
	int



### read()



```c
int TembooMQTTChoreo::read()
```

!!! note "戻り値"
	int



### peek()



```c
int TembooMQTTChoreo::peek()
```

!!! note "戻り値"
	int



### flush()



```c
void TembooMQTTChoreo::flush()
```



### write()



```c
size_t TembooMQTTChoreo::write(uint8_t data)
```

!!! summary "引数"
	- uint8_t `data` 

!!! note "戻り値"
	size_t



