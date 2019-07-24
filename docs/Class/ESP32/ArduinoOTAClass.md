# ArduinoOTAClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_arduino_o_t_a_class.html)

## メンバー







### ArduinoOTAClass()



```c
ArduinoOTAClass::ArduinoOTAClass()
```



### ~ArduinoOTAClass()



```c
ArduinoOTAClass::~ArduinoOTAClass()
```



### setPort()



```c
ArduinoOTAClass & ArduinoOTAClass::setPort(uint16_t port)
```

!!! summary "引数"
	- uint16_t `port` 

!!! note "戻り値"
	ArduinoOTAClass&



### setHostname()



```c
ArduinoOTAClass & ArduinoOTAClass::setHostname(const char *hostname)
```

!!! summary "引数"
	- constchar * `hostname` 

!!! note "戻り値"
	ArduinoOTAClass&



### getHostname()



```c
String ArduinoOTAClass::getHostname()
```

!!! note "戻り値"
	String



### setPassword()



```c
ArduinoOTAClass & ArduinoOTAClass::setPassword(const char *password)
```

!!! summary "引数"
	- constchar * `password` 

!!! note "戻り値"
	ArduinoOTAClass&



### setPasswordHash()



```c
ArduinoOTAClass & ArduinoOTAClass::setPasswordHash(const char *password)
```

!!! summary "引数"
	- constchar * `password` 

!!! note "戻り値"
	ArduinoOTAClass&



### setRebootOnSuccess()



```c
ArduinoOTAClass & ArduinoOTAClass::setRebootOnSuccess(bool reboot)
```

!!! summary "引数"
	- bool `reboot` 

!!! note "戻り値"
	ArduinoOTAClass&



### setMdnsEnabled()



```c
ArduinoOTAClass & ArduinoOTAClass::setMdnsEnabled(bool enabled)
```

!!! summary "引数"
	- bool `enabled` 

!!! note "戻り値"
	ArduinoOTAClass&



### onStart()



```c
ArduinoOTAClass & ArduinoOTAClass::onStart(THandlerFunction fn)
```

!!! summary "引数"
	- THandlerFunction `fn` 

!!! note "戻り値"
	ArduinoOTAClass&



### onEnd()



```c
ArduinoOTAClass & ArduinoOTAClass::onEnd(THandlerFunction fn)
```

!!! summary "引数"
	- THandlerFunction `fn` 

!!! note "戻り値"
	ArduinoOTAClass&



### onError()



```c
ArduinoOTAClass & ArduinoOTAClass::onError(THandlerFunction_Error fn)
```

!!! summary "引数"
	- THandlerFunction_Error `fn` 

!!! note "戻り値"
	ArduinoOTAClass&



### onProgress()



```c
ArduinoOTAClass & ArduinoOTAClass::onProgress(THandlerFunction_Progress fn)
```

!!! summary "引数"
	- THandlerFunction_Progress `fn` 

!!! note "戻り値"
	ArduinoOTAClass&



### begin()



```c
void ArduinoOTAClass::begin()
```



### end()



```c
void ArduinoOTAClass::end()
```



### handle()



```c
void ArduinoOTAClass::handle()
```



### getCommand()



```c
int ArduinoOTAClass::getCommand()
```

!!! note "戻り値"
	int



### setTimeout()



```c
void ArduinoOTAClass::setTimeout(int timeoutInMillis)
```

!!! summary "引数"
	- int `timeoutInMillis` 



