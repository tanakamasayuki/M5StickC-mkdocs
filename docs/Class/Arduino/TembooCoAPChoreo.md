# TembooCoAPChoreo



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_temboo_co_a_p_choreo.html)

## メンバー



### TembooCoAPChoreo()



```c
TembooCoAPChoreo::TembooCoAPChoreo(TembooCoAPClient &client)
```

!!! summary "引数"
	- TembooCoAPClient& `client` 



### ~TembooCoAPChoreo()



```c
TembooCoAPChoreo::~TembooCoAPChoreo()
```



### begin()



```c
void TembooCoAPChoreo::begin()
```



### setAccountName()



```c
void TembooCoAPChoreo::setAccountName(const String &accountName)
```

!!! summary "引数"
	- constString & `accountName` 



### setAccountName()



```c
void TembooCoAPChoreo::setAccountName(const char *accountName)
```

!!! summary "引数"
	- constchar * `accountName` 



### setAppKeyName()



```c
void TembooCoAPChoreo::setAppKeyName(const String &appKeyName)
```

!!! summary "引数"
	- constString & `appKeyName` 



### setAppKeyName()



```c
void TembooCoAPChoreo::setAppKeyName(const char *appKeyName)
```

!!! summary "引数"
	- constchar * `appKeyName` 



### setAppKey()



```c
void TembooCoAPChoreo::setAppKey(const String &appKey)
```

!!! summary "引数"
	- constString & `appKey` 



### setAppKey()



```c
void TembooCoAPChoreo::setAppKey(const char *appKey)
```

!!! summary "引数"
	- constchar * `appKey` 



### setChoreo()



```c
void TembooCoAPChoreo::setChoreo(const String &choreoPath)
```

!!! summary "引数"
	- constString & `choreoPath` 



### setChoreo()



```c
void TembooCoAPChoreo::setChoreo(const char *choreoPath)
```

!!! summary "引数"
	- constchar * `choreoPath` 



### setSavedInputs()



```c
void TembooCoAPChoreo::setSavedInputs(const String &savedInputsName)
```

!!! summary "引数"
	- constString & `savedInputsName` 



### setSavedInputs()



```c
void TembooCoAPChoreo::setSavedInputs(const char *savedInputsName)
```

!!! summary "引数"
	- constchar * `savedInputsName` 



### setCredential()



```c
void TembooCoAPChoreo::setCredential(const String &credentialName)
```

!!! summary "引数"
	- constString & `credentialName` 



### setCredential()



```c
void TembooCoAPChoreo::setCredential(const char *credentialName)
```

!!! summary "引数"
	- constchar * `credentialName` 



### setProfile()



```c
void TembooCoAPChoreo::setProfile(const String &profileName)
```

!!! summary "引数"
	- constString & `profileName` 



### setProfile()



```c
void TembooCoAPChoreo::setProfile(const char *profileName)
```

!!! summary "引数"
	- constchar * `profileName` 



### addInput()



```c
void TembooCoAPChoreo::addInput(const String &inputName, const String &inputValue)
```

!!! summary "引数"
	- constString & `inputName` 
	- constString & `inputValue` 



### addInput()



```c
void TembooCoAPChoreo::addInput(const char *inputName, const char *inputValue)
```

!!! summary "引数"
	- constchar * `inputName` 
	- constchar * `inputValue` 



### addInput()



```c
void TembooCoAPChoreo::addInput(const char *inputName, const String &inputValue)
```

!!! summary "引数"
	- constchar * `inputName` 
	- constString & `inputValue` 



### addInput()



```c
void TembooCoAPChoreo::addInput(const String &inputName, const char *inputValue)
```

!!! summary "引数"
	- constString & `inputName` 
	- constchar * `inputValue` 



### addOutputFilter()



```c
void TembooCoAPChoreo::addOutputFilter(const char *filterName, const char *filterPath, const char *variableName)
```

!!! summary "引数"
	- constchar * `filterName` 
	- constchar * `filterPath` 
	- constchar * `variableName` 



### addOutputFilter()



```c
void TembooCoAPChoreo::addOutputFilter(const String &filterName, const char *filterPath, const char *variableName)
```

!!! summary "引数"
	- constString & `filterName` 
	- constchar * `filterPath` 
	- constchar * `variableName` 



### addOutputFilter()



```c
void TembooCoAPChoreo::addOutputFilter(const char *filterName, const String &filterPath, const char *variableName)
```

!!! summary "引数"
	- constchar * `filterName` 
	- constString & `filterPath` 
	- constchar * `variableName` 



### addOutputFilter()



```c
void TembooCoAPChoreo::addOutputFilter(const String &filterName, const String &filterPath, const char *variableName)
```

!!! summary "引数"
	- constString & `filterName` 
	- constString & `filterPath` 
	- constchar * `variableName` 



### addOutputFilter()



```c
void TembooCoAPChoreo::addOutputFilter(const char *filterName, const char *filterPath, const String &variableName)
```

!!! summary "引数"
	- constchar * `filterName` 
	- constchar * `filterPath` 
	- constString & `variableName` 



### addOutputFilter()



```c
void TembooCoAPChoreo::addOutputFilter(const String &filterName, const char *filterPath, const String &variableName)
```

!!! summary "引数"
	- constString & `filterName` 
	- constchar * `filterPath` 
	- constString & `variableName` 



### addOutputFilter()



```c
void TembooCoAPChoreo::addOutputFilter(const char *filterName, const String &filterPath, const String &variableName)
```

!!! summary "引数"
	- constchar * `filterName` 
	- constString & `filterPath` 
	- constString & `variableName` 



### addOutputFilter()



```c
void TembooCoAPChoreo::addOutputFilter(const String &filterName, const String &filterPath, const String &variableName)
```

!!! summary "引数"
	- constString & `filterName` 
	- constString & `filterPath` 
	- constString & `variableName` 



### run()



```c
int TembooCoAPChoreo::run(uint16_t timeoutSecs=DEFAULT_CHOREO_TIMEOUT)
```

!!! summary "引数"
	- uint16_t `timeoutSecs` 

!!! note "戻り値"
	int



### getResponseData()



```c
char* TembooCoAPChoreo::getResponseData()
```

!!! note "戻り値"
	char *



### getHTTPResponseCode()



```c
char* TembooCoAPChoreo::getHTTPResponseCode()
```

!!! note "戻り値"
	char *



### close()



```c
void TembooCoAPChoreo::close()
```



### available()



```c
int TembooCoAPChoreo::available()
```

!!! note "戻り値"
	int



### read()



```c
int TembooCoAPChoreo::read()
```

!!! note "戻り値"
	int



### peek()



```c
int TembooCoAPChoreo::peek()
```

!!! note "戻り値"
	int



### flush()



```c
void TembooCoAPChoreo::flush()
```



### write()



```c
size_t TembooCoAPChoreo::write(uint8_t data)
```

!!! summary "引数"
	- uint8_t `data` 

!!! note "戻り値"
	size_t



