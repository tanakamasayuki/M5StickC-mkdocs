# BLEAddress

A BLE device address. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_address.html)

## メンバー

### BLEAddress()
Create an address from the native ESP32 representation.


```c
BLEAddress::BLEAddress(esp_bd_addr_t address)
```

!!! summary "引数"
	- esp_bd_addr_t `address` The native representation. 



### BLEAddress()
Create an address from a hex string

A hex string is of the format:  which is 17 characters in length.
```c
BLEAddress::BLEAddress(std::string stringAddress)
```

!!! summary "引数"
	- std::string `stringAddress` The hex representation of the address. 



### equals()
Determine if this address equals another.


```c
bool BLEAddress::equals(BLEAddress otherAddress)
```

!!! summary "引数"
	- BLEAddress `otherAddress` The other address to compare against. 

!!! note "戻り値"
	bool True if the addresses are equal. 



### getNative()
Return the native representation of the address.



```c
esp_bd_addr_t * BLEAddress::getNative()
```

!!! note "戻り値"
	esp_bd_addr_t* The native representation of the address. 



### toString()
Convert a BLE address to a string.



```c
std::string BLEAddress::toString()
```

!!! note "戻り値"
	std::string



