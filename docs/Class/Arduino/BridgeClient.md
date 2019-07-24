# BridgeClient



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_bridge_client.html)

## メンバー

### BridgeClient()



```c
BridgeClient::BridgeClient(uint8_t _h, BridgeClass &_b=Bridge)
```

!!! summary "引数"
	- uint8_t `_h` 
	- BridgeClass& `_b` 



### BridgeClient()



```c
BridgeClient::BridgeClient(BridgeClass &_b=Bridge)
```

!!! summary "引数"
	- BridgeClass& `_b` 



### ~BridgeClient()



```c
BridgeClient::~BridgeClient()
```



### available()



```c
int BridgeClient::available()
```

!!! note "戻り値"
	int



### read()



```c
int BridgeClient::read()
```

!!! note "戻り値"
	int



### read()



```c
int BridgeClient::read(uint8_t *buf, size_t size)
```

!!! summary "引数"
	- uint8_t * `buf` 
	- size_t `size` 

!!! note "戻り値"
	int



### peek()



```c
int BridgeClient::peek()
```

!!! note "戻り値"
	int



### write()



```c
size_t BridgeClient::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t BridgeClient::write(const uint8_t *buf, size_t size)
```

!!! summary "引数"
	- constuint8_t * `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### flush()



```c
void BridgeClient::flush()
```



### operator bool()



```c
virtual BridgeClient::operator bool()
```



### operator=()



```c
BridgeClient & BridgeClient::operator=(const BridgeClient &_x)
```

!!! summary "引数"
	- const& `_x` 

!!! note "戻り値"
	BridgeClient&



### stop()



```c
void BridgeClient::stop()
```



### connected()



```c
uint8_t BridgeClient::connected()
```

!!! note "戻り値"
	uint8_t



### connect()



```c
int BridgeClient::connect(IPAddress ip, uint16_t port)
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### connect()



```c
int BridgeClient::connect(const char *host, uint16_t port)
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### connectSSL()



```c
int BridgeClient::connectSSL(const char *host, uint16_t port)
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 

!!! note "戻り値"
	int



