# BLESecurity



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_security.html)

## メンバー

### BLESecurity()



```c
BLESecurity::BLESecurity()
```



### ~BLESecurity()



```c
BLESecurity::~BLESecurity()
```



### setAuthenticationMode()



```c
void BLESecurity::setAuthenticationMode(esp_ble_auth_req_t auth_req)
```

!!! summary "引数"
	- esp_ble_auth_req_t `auth_req` 



### setCapability()
Set our device IO capability to let end user perform authorization either by displaying or entering generated 6-digits pin code


```c
void BLESecurity::setCapability(esp_ble_io_cap_t iocap)
```

!!! summary "引数"
	- esp_ble_io_cap_t `iocap` 



### setInitEncryptionKey()
Init encryption key by server


```c
void BLESecurity::setInitEncryptionKey(uint8_t init_key)
```

!!! summary "引数"
	- uint8_t `init_key` 



### setRespEncryptionKey()
Init encryption key by client


```c
void BLESecurity::setRespEncryptionKey(uint8_t resp_key)
```

!!! summary "引数"
	- uint8_t `resp_key` 



### setKeySize()



```c
void BLESecurity::setKeySize(uint8_t key_size=16)
```

!!! summary "引数"
	- uint8_t `key_size` 



### esp_key_type_to_str()
Debug function to display what keys are exchanged by peers


```c
char * BLESecurity::esp_key_type_to_str(esp_ble_key_type_t key_type)
```

!!! summary "引数"
	- esp_ble_key_type_t `key_type` 

!!! note "戻り値"
	char *



