# HMAC



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_h_m_a_c.html)

## メンバー



### HMAC()



```c
HMAC::HMAC()
```



### HMAC()



```c
HMAC::HMAC(const uint8_t *key, uint32_t keyLength)
```

!!! summary "引数"
	- constuint8_t * `key` 
	- uint32_t `keyLength` 



### init()



```c
void HMAC::init(const uint8_t *key, uint32_t keyLength)
```

!!! summary "引数"
	- constuint8_t * `key` 
	- uint32_t `keyLength` 



### process()



```c
void HMAC::process(const uint8_t *msg, uint32_t msgLength)
```

!!! summary "引数"
	- constuint8_t * `msg` 
	- uint32_t `msgLength` 



### finish()



```c
void HMAC::finish(uint8_t *dest)
```

!!! summary "引数"
	- uint8_t * `dest` 



### finishHex()



```c
void HMAC::finishHex(char *dest)
```

!!! summary "引数"
	- char * `dest` 



