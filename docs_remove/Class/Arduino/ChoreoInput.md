# ChoreoInput



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_choreo_input.html)

## メンバー

### ChoreoInput()



```c
ChoreoInput::ChoreoInput(ChoreoInput *prev, const char *name, const char *value)
```

!!! summary "引数"
	- ChoreoInput* `prev` 
	- constchar * `name` 
	- constchar * `value` 



### getName()



```c
const char* ChoreoInput::getName() const
```

!!! note "戻り値"
	constchar *



### getValue()



```c
const char* ChoreoInput::getValue() const
```

!!! note "戻り値"
	constchar *



### setValue()



```c
void ChoreoInput::setValue(const char *value)
```

!!! summary "引数"
	- constchar * `value` 



### getNext()



```c
ChoreoInput* ChoreoInput::getNext() const
```

!!! note "戻り値"
	ChoreoInput*



