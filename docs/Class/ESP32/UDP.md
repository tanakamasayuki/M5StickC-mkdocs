# UDP



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_u_d_p.html)

## メンバー

### begin()



```c
virtual uint8_t UDP::begin(uint16_t)=0
```

!!! summary "引数"
	- uint16_t `` 

!!! note "戻り値"
	uint8_t



### stop()



```c
virtual void UDP::stop()=0
```



### beginPacket()



```c
virtual int UDP::beginPacket(IPAddress ip, uint16_t port)=0
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### beginPacket()



```c
virtual int UDP::beginPacket(const char *host, uint16_t port)=0
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### endPacket()



```c
virtual int UDP::endPacket()=0
```

!!! note "戻り値"
	int



### write()



```c
virtual size_t UDP::write(uint8_t)=0
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
virtual size_t UDP::write(const uint8_t *buffer, size_t size)=0
```

!!! summary "引数"
	- const* `buffer` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### parsePacket()



```c
virtual int UDP::parsePacket()=0
```

!!! note "戻り値"
	int



### available()



```c
virtual int UDP::available()=0
```

!!! note "戻り値"
	int



### read()



```c
virtual int UDP::read()=0
```

!!! note "戻り値"
	int



### read()



```c
virtual int UDP::read(unsigned char *buffer, size_t len)=0
```

!!! summary "引数"
	- unsigned char * `buffer` 
	- size_t `len` 

!!! note "戻り値"
	int



### read()



```c
virtual int UDP::read(char *buffer, size_t len)=0
```

!!! summary "引数"
	- char * `buffer` 
	- size_t `len` 

!!! note "戻り値"
	int



### peek()



```c
virtual int UDP::peek()=0
```

!!! note "戻り値"
	int



### flush()



```c
virtual void UDP::flush()=0
```



### remoteIP()



```c
virtual IPAddress UDP::remoteIP()=0
```

!!! note "戻り値"
	IPAddress



### remotePort()



```c
virtual uint16_t UDP::remotePort()=0
```

!!! note "戻り値"
	uint16_t



