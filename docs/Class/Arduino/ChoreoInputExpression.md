# ChoreoInputExpression



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_choreo_input_expression.html)

## メンバー

### ChoreoInputExpression()



```c
ChoreoInputExpression::ChoreoInputExpression(ChoreoInputExpression *prev, const char *name, const char *value)
```

!!! summary "引数"
	- ChoreoInputExpression* `prev` 
	- constchar * `name` 
	- constchar * `value` 



### getName()



```c
const char* ChoreoInputExpression::getName() const
```

!!! note "戻り値"
	constchar *



### getValue()



```c
const char* ChoreoInputExpression::getValue() const
```

!!! note "戻り値"
	constchar *



### setValue()



```c
void ChoreoInputExpression::setValue(const char *value)
```

!!! summary "引数"
	- constchar * `value` 



### getNext()



```c
ChoreoInputExpression* ChoreoInputExpression::getNext() const
```

!!! note "戻り値"
	ChoreoInputExpression*



