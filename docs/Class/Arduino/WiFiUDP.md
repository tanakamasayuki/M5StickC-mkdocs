# WiFiUDP



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_wi_fi_u_d_p.html)

## メンバー



### WiFiUDP()



```c
WiFiUDP::WiFiUDP()
```



### begin()



```c
uint8_t WiFiUDP::begin(uint16_t)
```

!!! summary "引数"
	- uint16_t `` 

!!! note "戻り値"
	uint8_t



### stop()



```c
void WiFiUDP::stop()
```



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
	- constuint8_t * `buffer` 
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
virtual int WiFiUDP::read(char *buffer, size_t len)
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



