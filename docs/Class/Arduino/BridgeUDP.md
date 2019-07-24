# BridgeUDP



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_bridge_u_d_p.html)

## メンバー

### BridgeUDP()



```c
BridgeUDP::BridgeUDP(BridgeClass &_b=Bridge)
```

!!! summary "引数"
	- BridgeClass& `_b` 



### begin()



```c
uint8_t BridgeUDP::begin(uint16_t)
```

!!! summary "引数"
	- uint16_t `` 

!!! note "戻り値"
	uint8_t



### stop()



```c
void BridgeUDP::stop()
```



### beginPacket()



```c
int BridgeUDP::beginPacket(IPAddress ip, uint16_t port)
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### beginPacket()



```c
int BridgeUDP::beginPacket(const char *host, uint16_t port)
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### beginBroadcastPacket()



```c
int BridgeUDP::beginBroadcastPacket(uint16_t port)
```

!!! summary "引数"
	- uint16_t `port` 

!!! note "戻り値"
	int



### endPacket()



```c
int BridgeUDP::endPacket()
```

!!! note "戻り値"
	int



### write()



```c
virtual size_t BridgeUDP::write(uint8_t d)
```

!!! summary "引数"
	- uint8_t `d` 

!!! note "戻り値"
	size_t



### write()



```c
size_t BridgeUDP::write(const uint8_t *buffer, size_t size)
```

!!! summary "引数"
	- constuint8_t * `buffer` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### parsePacket()



```c
int BridgeUDP::parsePacket()
```

!!! note "戻り値"
	int



### available()



```c
virtual int BridgeUDP::available()
```

!!! note "戻り値"
	int



### read()



```c
int BridgeUDP::read()
```

!!! note "戻り値"
	int



### read()



```c
int BridgeUDP::read(unsigned char *buffer, size_t len)
```

!!! summary "引数"
	- unsigned char * `buffer` 
	- size_t `len` 

!!! note "戻り値"
	int



### read()



```c
virtual int BridgeUDP::read(char *buffer, size_t len)
```

!!! summary "引数"
	- char * `buffer` 
	- size_t `len` 

!!! note "戻り値"
	int



### peek()



```c
int BridgeUDP::peek()
```

!!! note "戻り値"
	int



### flush()



```c
virtual void BridgeUDP::flush()
```



### remoteIP()



```c
IPAddress BridgeUDP::remoteIP()
```

!!! note "戻り値"
	IPAddress



### remotePort()



```c
uint16_t BridgeUDP::remotePort()
```

!!! note "戻り値"
	uint16_t



### write()



```c
virtual size_t Print::write(uint8_t)=0
```

!!! note "戻り値"
	size_t



### write()



```c
size_t Print::write(const char *str)
```

!!! note "戻り値"
	size_t



### write()



```c
size_t Print::write(const uint8_t *buffer, size_t size)
```

!!! note "戻り値"
	size_t



### write()



```c
size_t Print::write(const char *buffer, size_t size)
```

!!! note "戻り値"
	size_t



