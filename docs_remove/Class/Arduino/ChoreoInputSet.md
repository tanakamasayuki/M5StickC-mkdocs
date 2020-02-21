# ChoreoInputSet



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_choreo_input_set.html)

## メンバー

### ChoreoInputSet()



```c
ChoreoInputSet::ChoreoInputSet()
```



### ~ChoreoInputSet()



```c
ChoreoInputSet::~ChoreoInputSet()
```



### put()



```c
void ChoreoInputSet::put(const char *name, const char *value)
```

!!! summary "引数"
	- constchar * `name` 
	- constchar * `value` 



### get()



```c
const char * ChoreoInputSet::get(const char *name) const
```

!!! summary "引数"
	- constchar * `name` 

!!! note "戻り値"
	constchar *



### isEmpty()



```c
bool ChoreoInputSet::isEmpty() const
```

!!! note "戻り値"
	bool



### getFirstInput()



```c
const ChoreoInput* ChoreoInputSet::getFirstInput() const
```

!!! note "戻り値"
	const*



