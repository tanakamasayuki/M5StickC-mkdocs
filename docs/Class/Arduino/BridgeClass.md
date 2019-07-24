# BridgeClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_bridge_class.html)

## メンバー

###  TRANSFER_TIMEOUT

```c
const uint16_t BridgeClass::TRANSFER_TIMEOUT
```


### BridgeClass()



```c
BridgeClass::BridgeClass(Stream &_stream)
```

!!! summary "引数"
	- Stream& `_stream` 



### begin()



```c
void BridgeClass::begin()
```



### end()



```c
void BridgeClass::end()
```



### put()



```c
void BridgeClass::put(const char *key, const char *value)
```

!!! summary "引数"
	- constchar * `key` 
	- constchar * `value` 



### put()



```c
void BridgeClass::put(const String &key, const String &value)
```

!!! summary "引数"
	- constString & `key` 
	- constString & `value` 



### get()



```c
unsigned int BridgeClass::get(const char *key, uint8_t *buff, unsigned int size)
```

!!! summary "引数"
	- constchar * `key` 
	- uint8_t * `buff` 
	- unsigned int `size` 

!!! note "戻り値"
	unsigned int



### get()



```c
unsigned int BridgeClass::get(const char *key, char *value, unsigned int maxlen)
```

!!! summary "引数"
	- constchar * `key` 
	- char * `value` 
	- unsigned int `maxlen` 

!!! note "戻り値"
	unsigned int



### transfer()



```c
uint16_t BridgeClass::transfer(const uint8_t *buff1, uint16_t len1, const uint8_t *buff2, uint16_t len2, const uint8_t *buff3, uint16_t len3, uint8_t *rxbuff, uint16_t rxlen)
```

!!! summary "引数"
	- constuint8_t * `buff1` 
	- uint16_t `len1` 
	- constuint8_t * `buff2` 
	- uint16_t `len2` 
	- constuint8_t * `buff3` 
	- uint16_t `len3` 
	- uint8_t * `rxbuff` 
	- uint16_t `rxlen` 

!!! note "戻り値"
	uint16_t



### transfer()



```c
uint16_t BridgeClass::transfer(const uint8_t *buff1, uint16_t len1)
```

!!! summary "引数"
	- constuint8_t * `buff1` 
	- uint16_t `len1` 

!!! note "戻り値"
	uint16_t



### transfer()



```c
uint16_t BridgeClass::transfer(const uint8_t *buff1, uint16_t len1, uint8_t *rxbuff, uint16_t rxlen)
```

!!! summary "引数"
	- constuint8_t * `buff1` 
	- uint16_t `len1` 
	- uint8_t * `rxbuff` 
	- uint16_t `rxlen` 

!!! note "戻り値"
	uint16_t



### transfer()



```c
uint16_t BridgeClass::transfer(const uint8_t *buff1, uint16_t len1, const uint8_t *buff2, uint16_t len2, uint8_t *rxbuff, uint16_t rxlen)
```

!!! summary "引数"
	- constuint8_t * `buff1` 
	- uint16_t `len1` 
	- constuint8_t * `buff2` 
	- uint16_t `len2` 
	- uint8_t * `rxbuff` 
	- uint16_t `rxlen` 

!!! note "戻り値"
	uint16_t



### getBridgeVersion()



```c
uint16_t BridgeClass::getBridgeVersion()
```

!!! note "戻り値"
	uint16_t



