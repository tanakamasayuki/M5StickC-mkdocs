# TembooOneWire



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_temboo_one_wire.html)

## メンバー

### TembooOneWire()



```c
TembooOneWire::TembooOneWire(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 



### reset()



```c
uint8_t TembooOneWire::reset(void)
```

!!! note "戻り値"
	uint8_t



### select()



```c
void TembooOneWire::select(const uint8_t rom[8])
```

!!! summary "引数"
	- constuint8_t `rom` 



### skip()



```c
void TembooOneWire::skip(void)
```



### write()



```c
void TembooOneWire::write(uint8_t v, uint8_t power=0)
```

!!! summary "引数"
	- uint8_t `v` 
	- uint8_t `power` 



### write_bytes()



```c
void TembooOneWire::write_bytes(const uint8_t *buf, uint16_t count, bool power=0)
```

!!! summary "引数"
	- constuint8_t * `buf` 
	- uint16_t `count` 
	- bool `power` 



### read()



```c
uint8_t TembooOneWire::read(void)
```

!!! note "戻り値"
	uint8_t



### read_bytes()



```c
void TembooOneWire::read_bytes(uint8_t *buf, uint16_t count)
```

!!! summary "引数"
	- uint8_t * `buf` 
	- uint16_t `count` 



### write_bit()



```c
void TembooOneWire::write_bit(uint8_t v)
```

!!! summary "引数"
	- uint8_t `v` 



### read_bit()



```c
uint8_t TembooOneWire::read_bit(void)
```

!!! note "戻り値"
	uint8_t



### depower()



```c
void TembooOneWire::depower(void)
```



### reset_search()



```c
void TembooOneWire::reset_search()
```



### target_search()



```c
void TembooOneWire::target_search(uint8_t family_code)
```

!!! summary "引数"
	- uint8_t `family_code` 



### search()



```c
uint8_t TembooOneWire::search(uint8_t *newAddr, bool search_mode=true)
```

!!! summary "引数"
	- uint8_t * `newAddr` 
	- bool `search_mode` 

!!! note "戻り値"
	uint8_t



### crc8()



```c
uint8_t TembooOneWire::crc8(const uint8_t *addr, uint8_t len)
```

!!! summary "引数"
	- constuint8_t * `addr` 
	- uint8_t `len` 

!!! note "戻り値"
	uint8_t



### check_crc16()



```c
bool TembooOneWire::check_crc16(const uint8_t *input, uint16_t len, const uint8_t *inverted_crc, uint16_t crc=0)
```

!!! summary "引数"
	- constuint8_t * `input` 
	- uint16_t `len` 
	- constuint8_t * `inverted_crc` 
	- uint16_t `crc` 

!!! note "戻り値"
	bool



### crc16()



```c
uint16_t TembooOneWire::crc16(const uint8_t *input, uint16_t len, uint16_t crc=0)
```

!!! summary "引数"
	- constuint8_t * `input` 
	- uint16_t `len` 
	- uint16_t `crc` 

!!! note "戻り値"
	uint16_t



