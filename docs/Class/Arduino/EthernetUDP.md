# EthernetUDP



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_ethernet_u_d_p.html)

## メンバー

### EthernetUDP()



```c
EthernetUDP::EthernetUDP()
```



### begin()



```c
uint8_t EthernetUDP::begin(uint16_t)
```

!!! summary "引数"
	- uint16_t `` 

!!! note "戻り値"
	uint8_t



### beginMulticast()



```c
uint8_t EthernetUDP::beginMulticast(IPAddress, uint16_t)
```

!!! summary "引数"
	- uint16_t `` 

!!! note "戻り値"
	uint8_t



### stop()



```c
void EthernetUDP::stop()
```



### beginPacket()



```c
int EthernetUDP::beginPacket(IPAddress ip, uint16_t port)
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### beginPacket()



```c
int EthernetUDP::beginPacket(const char *host, uint16_t port)
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### endPacket()



```c
int EthernetUDP::endPacket()
```

!!! note "戻り値"
	int



### write()



```c
size_t EthernetUDP::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t EthernetUDP::write(const uint8_t *buffer, size_t size)
```

!!! summary "引数"
	- constuint8_t * `buffer` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### parsePacket()



```c
int EthernetUDP::parsePacket()
```

!!! note "戻り値"
	int



### available()



```c
int EthernetUDP::available()
```

!!! note "戻り値"
	int



### read()



```c
int EthernetUDP::read()
```

!!! note "戻り値"
	int



### read()



```c
int EthernetUDP::read(unsigned char *buffer, size_t len)
```

!!! summary "引数"
	- unsigned char * `buffer` 
	- size_t `len` 

!!! note "戻り値"
	int



### read()



```c
virtual int EthernetUDP::read(char *buffer, size_t len)
```

!!! summary "引数"
	- char * `buffer` 
	- size_t `len` 

!!! note "戻り値"
	int



### peek()



```c
int EthernetUDP::peek()
```

!!! note "戻り値"
	int



### flush()



```c
void EthernetUDP::flush()
```



### remoteIP()



```c
virtual IPAddress EthernetUDP::remoteIP()
```

!!! note "戻り値"
	IPAddress



### remotePort()



```c
virtual uint16_t EthernetUDP::remotePort()
```

!!! note "戻り値"
	uint16_t



### localPort()



```c
virtual uint16_t EthernetUDP::localPort()
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



