# WiFiUDP



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_wi_fi_u_d_p.html)

## メンバー

### WiFiUDP()



```c
WiFiUDP::WiFiUDP()
```



### ~WiFiUDP()



```c
WiFiUDP::~WiFiUDP()
```



### begin()



```c
uint8_t WiFiUDP::begin(IPAddress a, uint16_t p)
```

!!! summary "引数"
	- IPAddress `a` 
	- uint16_t `p` 

!!! note "戻り値"
	uint8_t



### begin()



```c
uint8_t WiFiUDP::begin(uint16_t p)
```

!!! summary "引数"
	- uint16_t `p` 

!!! note "戻り値"
	uint8_t



### beginMulticast()



```c
uint8_t WiFiUDP::beginMulticast(IPAddress a, uint16_t p)
```

!!! summary "引数"
	- IPAddress `a` 
	- uint16_t `p` 

!!! note "戻り値"
	uint8_t



### stop()



```c
void WiFiUDP::stop()
```



### beginMulticastPacket()



```c
int WiFiUDP::beginMulticastPacket()
```

!!! note "戻り値"
	int



### beginPacket()



```c
int WiFiUDP::beginPacket()
```

!!! note "戻り値"
	int



### beginPacket()



```c
int WiFiUDP::beginPacket(IPAddress ip, uint16_t port)
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### beginPacket()



```c
int WiFiUDP::beginPacket(const char *host, uint16_t port)
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### endPacket()



```c
int WiFiUDP::endPacket()
```

!!! note "戻り値"
	int



### write()



```c
size_t WiFiUDP::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t WiFiUDP::write(const uint8_t *buffer, size_t size)
```

!!! summary "引数"
	- const* `buffer` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### parsePacket()



```c
int WiFiUDP::parsePacket()
```

!!! note "戻り値"
	int



### available()



```c
int WiFiUDP::available()
```

!!! note "戻り値"
	int



### read()



```c
int WiFiUDP::read()
```

!!! note "戻り値"
	int



### read()



```c
int WiFiUDP::read(unsigned char *buffer, size_t len)
```

!!! summary "引数"
	- unsigned char * `buffer` 
	- size_t `len` 

!!! note "戻り値"
	int



### read()



```c
int WiFiUDP::read(char *buffer, size_t len)
```

!!! summary "引数"
	- char * `buffer` 
	- size_t `len` 

!!! note "戻り値"
	int



### peek()



```c
int WiFiUDP::peek()
```

!!! note "戻り値"
	int



### flush()



```c
void WiFiUDP::flush()
```



### remoteIP()



```c
IPAddress WiFiUDP::remoteIP()
```

!!! note "戻り値"
	IPAddress



### remotePort()



```c
uint16_t WiFiUDP::remotePort()
```

!!! note "戻り値"
	uint16_t



