# ChoreoOutputSet



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_choreo_output_set.html)

## メンバー

### ChoreoOutputSet()



```c
ChoreoOutputSet::ChoreoOutputSet()
```



### ~ChoreoOutputSet()



```c
ChoreoOutputSet::~ChoreoOutputSet()
```



### put()



```c
void ChoreoOutputSet::put(const char *name, const char *path, const char *variable)
```

!!! summary "引数"
	- constchar * `name` 
	- constchar * `path` 
	- constchar * `variable` 



### get()



```c
const ChoreoOutput * ChoreoOutputSet::get(const char *name) const
```

!!! summary "引数"
	- constchar * `name` 

!!! note "戻り値"
	const*



### isEmpty()



```c
bool ChoreoOutputSet::isEmpty() const
```

!!! note "戻り値"
	bool



### getFirstOutput()



```c
const ChoreoOutput* ChoreoOutputSet::getFirstOutput() const
```

!!! note "戻り値"
	const*



