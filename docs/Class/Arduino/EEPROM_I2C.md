# EEPROM_I2C



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_e_e_p_r_o_m___i2_c.html)

## メンバー

### begin()



```c
void EEPROM_I2C::begin()
```



### writeByte()



```c
void EEPROM_I2C::writeByte(unsigned int eeaddresspage, byte data)
```

!!! summary "引数"
	- unsigned int `eeaddresspage` 
	- byte `data` 



### readByte()



```c
byte EEPROM_I2C::readByte(unsigned int eeaddresspage)
```

!!! summary "引数"
	- unsigned int `eeaddresspage` 

!!! note "戻り値"
	byte



### writePage()



```c
void EEPROM_I2C::writePage(unsigned int eeaddresspage, byte *data, byte length)
```

!!! summary "引数"
	- unsigned int `eeaddresspage` 
	- byte* `data` 
	- byte `length` 



### readBuffer()



```c
void EEPROM_I2C::readBuffer(unsigned int eeaddress, byte *buffer, int length)
```

!!! summary "引数"
	- unsigned int `eeaddress` 
	- byte* `buffer` 
	- int `length` 



