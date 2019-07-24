# ChoreoOutput



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_choreo_output.html)

## メンバー

### ChoreoOutput()



```c
ChoreoOutput::ChoreoOutput(ChoreoOutput *prev, const char *name, const char *path, const char *var)
```

!!! summary "引数"
	- ChoreoOutput* `prev` 
	- constchar * `name` 
	- constchar * `path` 
	- constchar * `var` 



### getName()



```c
const char* ChoreoOutput::getName() const
```

!!! note "戻り値"
	constchar *



### getPath()



```c
const char* ChoreoOutput::getPath() const
```

!!! note "戻り値"
	constchar *



### getVariable()



```c
const char* ChoreoOutput::getVariable() const
```

!!! note "戻り値"
	constchar *



### setPath()



```c
void ChoreoOutput::setPath(const char *path)
```

!!! summary "引数"
	- constchar * `path` 



### setVariable()



```c
void ChoreoOutput::setVariable(const char *variable)
```

!!! summary "引数"
	- constchar * `variable` 



### getNext()



```c
ChoreoOutput* ChoreoOutput::getNext() const
```

!!! note "戻り値"
	ChoreoOutput*



