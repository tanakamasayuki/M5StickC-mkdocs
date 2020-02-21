# SpacebrewYun



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_spacebrew_yun.html)

## メンバー















### SpacebrewYun()



```c
SpacebrewYun::SpacebrewYun(const String &, const String &)
```

!!! summary "引数"
	- constString & `` 



### addPublish()



```c
void SpacebrewYun::addPublish(const String &, const String &)
```

!!! summary "引数"
	- constString & `` 



### addSubscribe()



```c
void SpacebrewYun::addSubscribe(const String &, const String &)
```

!!! summary "引数"
	- constString & `` 



### connect()



```c
void SpacebrewYun::connect(String, int)
```

!!! summary "引数"
	- int `` 



### connect()



```c
void SpacebrewYun::connect()
```



### connect()



```c
void SpacebrewYun::connect(String _server)
```

!!! summary "引数"
	- String `_server` 



### monitor()



```c
void SpacebrewYun::monitor()
```



### onMessage()



```c
void SpacebrewYun::onMessage()
```



### onConfirm()



```c
void SpacebrewYun::onConfirm()
```



### connected()



```c
boolean SpacebrewYun::connected()
```

!!! note "戻り値"
	boolean



### send()



```c
void SpacebrewYun::send(const String &, const String &)
```

!!! summary "引数"
	- constString & `` 



### send()



```c
void SpacebrewYun::send(const String &name, char *value)
```

!!! summary "引数"
	- constString & `name` 
	- char * `value` 



### send()



```c
void SpacebrewYun::send(const String &name, bool value)
```

!!! summary "引数"
	- constString & `name` 
	- bool `value` 



### send()



```c
void SpacebrewYun::send(const String &name, int value)
```

!!! summary "引数"
	- constString & `name` 
	- int `value` 



### send()



```c
void SpacebrewYun::send(const String &name, long value)
```

!!! summary "引数"
	- constString & `name` 
	- long `value` 



### send()



```c
void SpacebrewYun::send(const String &name, float value)
```

!!! summary "引数"
	- constString & `name` 
	- float `value` 



### verbose()



```c
void SpacebrewYun::verbose(boolean)
```

!!! summary "引数"
	- boolean `` 



### onOpen()



```c
void SpacebrewYun::onOpen(OnSBOpen function)
```

!!! summary "引数"
	- OnSBOpen `function` 



### onClose()



```c
void SpacebrewYun::onClose(OnSBClose function)
```

!!! summary "引数"
	- OnSBClose `function` 



### onRangeMessage()



```c
void SpacebrewYun::onRangeMessage(OnRangeMessage function)
```

!!! summary "引数"
	- OnRangeMessage `function` 



### onStringMessage()



```c
void SpacebrewYun::onStringMessage(OnStringMessage function)
```

!!! summary "引数"
	- OnStringMessage `function` 



### onBooleanMessage()



```c
void SpacebrewYun::onBooleanMessage(OnBooleanMessage function)
```

!!! summary "引数"
	- OnBooleanMessage `function` 



### onCustomMessage()



```c
void SpacebrewYun::onCustomMessage(OnCustomMessage function)
```

!!! summary "引数"
	- OnCustomMessage `function` 



### onError()



```c
void SpacebrewYun::onError(OnSBError function)
```

!!! summary "引数"
	- OnSBError `function` 



