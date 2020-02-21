# ChoreoInputExpressionSet



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_choreo_input_expression_set.html)

## メンバー

### ChoreoInputExpressionSet()



```c
ChoreoInputExpressionSet::ChoreoInputExpressionSet()
```



### ~ChoreoInputExpressionSet()



```c
ChoreoInputExpressionSet::~ChoreoInputExpressionSet()
```



### put()



```c
void ChoreoInputExpressionSet::put(const char *name, const char *value)
```

!!! summary "引数"
	- constchar * `name` 
	- constchar * `value` 



### get()



```c
const char * ChoreoInputExpressionSet::get(const char *name) const
```

!!! summary "引数"
	- constchar * `name` 

!!! note "戻り値"
	constchar *



### isEmpty()



```c
bool ChoreoInputExpressionSet::isEmpty() const
```

!!! note "戻り値"
	bool



### getFirstInput()



```c
const ChoreoInputExpression* ChoreoInputExpressionSet::getFirstInput() const
```

!!! note "戻り値"
	const*



