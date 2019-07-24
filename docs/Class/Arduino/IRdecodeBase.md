# IRdecodeBase



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_i_rdecode_base.html)

## メンバー

###  protocolNum

```c
uint8_t IRdecodeBase::protocolNum
```


###  value

```c
uint32_t IRdecodeBase::value
```


###  address

```c
uint16_t IRdecodeBase::address
```


###  bits

```c
uint8_t IRdecodeBase::bits
```


###  ignoreHeader

```c
bool IRdecodeBase::ignoreHeader
```


### IRdecodeBase()



```c
IRdecodeBase::IRdecodeBase(void)
```



### decodeGeneric()



```c
bool IRdecodeBase::decodeGeneric(uint8_t expectedLength, uint16_t headMark, uint16_t headSpace, uint16_t markData, uint16_t spaceOne, uint16_t spaceZero)
```

!!! summary "引数"
	- uint8_t `expectedLength` 
	- uint16_t `headMark` 
	- uint16_t `headSpace` 
	- uint16_t `markData` 
	- uint16_t `spaceOne` 
	- uint16_t `spaceZero` 

!!! note "戻り値"
	bool



### dumpResults()



```c
void IRdecodeBase::dumpResults(bool verbose=true)
```

!!! summary "引数"
	- bool `verbose` 



### MATCH()



```c
bool IRdecodeBase::MATCH(int16_t val, int16_t expected)
```

!!! summary "引数"
	- int16_t `val` 
	- int16_t `expected` 

!!! note "戻り値"
	bool



### ABS_MATCH()



```c
bool IRdecodeBase::ABS_MATCH(int16_t val, int16_t expected, int16_t tolerance)
```

!!! summary "引数"
	- int16_t `val` 
	- int16_t `expected` 
	- int16_t `tolerance` 

!!! note "戻り値"
	bool



