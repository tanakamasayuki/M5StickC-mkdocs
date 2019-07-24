# BLEValue

The model of a BLE value. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_value.html)

## メンバー

### BLEValue()



```c
BLEValue::BLEValue()
```



### addPart()
Add a message part to the accumulation. The accumulation is a growing set of data that is added to until a commit or cancel.


```c
void BLEValue::addPart(std::string part)
```

!!! summary "引数"
	- std::string `part` A message part being added. 



### addPart()
Add a message part to the accumulation. The accumulation is a growing set of data that is added to until a commit or cancel.


```c
void BLEValue::addPart(uint8_t *pData, size_t length)
```

!!! summary "引数"
	- uint8_t* `pData` A message part being added. 
	- size_t `length` The number of bytes being added. 



### cancel()
Cancel the current accumulation.


```c
void BLEValue::cancel()
```



### commit()
Commit the current accumulation. When writing a value, we may find that we write it in "parts" meaning that the writes come in in pieces of the overall message. After the last part has been received, we may perform a commit which means that we now have the complete message and commit the change as a unit.


```c
void BLEValue::commit()
```



### getData()
Get a pointer to the data.



```c
uint8_t * BLEValue::getData()
```

!!! note "戻り値"
	uint8_t* A pointer to the data. 



### getLength()
Get the length of the data in bytes.



```c
size_t BLEValue::getLength()
```

!!! note "戻り値"
	size_t The length of the data in bytes. 



### getReadOffset()
Get the read offset.



```c
uint16_t BLEValue::getReadOffset()
```

!!! note "戻り値"
	uint16_t The read offset into the read. 



### getValue()
Get the current value.


```c
std::string BLEValue::getValue()
```

!!! note "戻り値"
	std::string



### setReadOffset()
Set the read offset


```c
void BLEValue::setReadOffset(uint16_t readOffset)
```

!!! summary "引数"
	- uint16_t `readOffset` The offset into the read. 



### setValue()
Set the current value.


```c
void BLEValue::setValue(std::string value)
```

!!! summary "引数"
	- std::string `value` 



### setValue()
Set the current value.


```c
void BLEValue::setValue(uint8_t *pData, size_t length)
```

!!! summary "引数"
	- uint8_t* `pData` The data for the current value. 
	- size_t `length` 



