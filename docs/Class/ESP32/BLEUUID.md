# BLEUUID

A model of a BLE UUID. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_u_u_i_d.html)

## メンバー

### BLEUUID()
Create a UUID from a string.

This has a length of 36 characters. We need to parse this into 16 bytes.
```c
BLEUUID::BLEUUID(std::string uuid)
```

!!! summary "引数"
	- std::string `uuid` 



### BLEUUID()
Create a UUID from the 16bit value.


```c
BLEUUID::BLEUUID(uint16_t uuid)
```

!!! summary "引数"
	- uint16_t `uuid` The 16bit short form UUID. 



### BLEUUID()
Create a UUID from the 32bit value.


```c
BLEUUID::BLEUUID(uint32_t uuid)
```

!!! summary "引数"
	- uint32_t `uuid` The 32bit short form UUID. 



### BLEUUID()
Create a UUID from the native UUID.


```c
BLEUUID::BLEUUID(esp_bt_uuid_t uuid)
```

!!! summary "引数"
	- esp_bt_uuid_t `uuid` The native UUID. 



### BLEUUID()
Create a UUID from 16 bytes of memory.


```c
BLEUUID::BLEUUID(uint8_t *pData, size_t size, bool msbFirst)
```

!!! summary "引数"
	- uint8_t* `pData` The pointer to the start of the UUID. 
	- size_t `size` The size of the data. 
	- bool `msbFirst` Is the MSB first in pData memory? 



### BLEUUID()
Create a UUID from the ESP32 esp_gat_id_t.


```c
BLEUUID::BLEUUID(esp_gatt_id_t gattId)
```

!!! summary "引数"
	- esp_gatt_id_t `gattId` The data to create the UUID from. 



### BLEUUID()



```c
BLEUUID::BLEUUID()
```



### bitSize()
Get the number of bits in this uuid.



```c
uint8_t BLEUUID::bitSize()
```

!!! note "戻り値"
	uint8_t The number of bits in the UUID. One of 16, 32 or 128. 



### equals()
Compare a UUID against this UUID.


```c
bool BLEUUID::equals(BLEUUID uuid)
```

!!! summary "引数"
	- BLEUUID `uuid` The UUID to compare against. 

!!! note "戻り値"
	bool True if the UUIDs are equal and false otherwise. 



### getNative()
Get the native UUID value.



```c
esp_bt_uuid_t * BLEUUID::getNative()
```

!!! note "戻り値"
	esp_bt_uuid_t * The native UUID value or NULL if not set. 



### to128()
Convert a UUID to its 128 bit representation.

A UUID can be internally represented as 16bit, 32bit or the full 128bit. This method will convert 16 or 32 bit representations to the full 128bit. 
```c
BLEUUID BLEUUID::to128()
```

!!! note "戻り値"
	BLEUUID



### toString()
Get a string representation of the UUID.



```c
std::string BLEUUID::toString()
```

!!! note "戻り値"
	std::string



### fromString()


Create a  from a string of the form: 0xNNNN 0xNNNNNNNN 0x<UUID> NNNN NNNNNNNN <UUID> 
```c
BLEUUID BLEUUID::fromString(std::string uuid)
```

!!! summary "引数"
	- std::string `uuid` 

!!! note "戻り値"
	BLEUUID



