# EthernetClient



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_ethernet_client.html)

## メンバー



### EthernetClient()



```c
EthernetClient::EthernetClient()
```



### EthernetClient()



```c
EthernetClient::EthernetClient(uint8_t s)
```

!!! summary "引数"
	- uint8_t `s` 



### status()



```c
uint8_t EthernetClient::status()
```

!!! note "戻り値"
	uint8_t



### connect()



```c
int EthernetClient::connect(IPAddress ip, uint16_t port)
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### connect()



```c
int EthernetClient::connect(const char *host, uint16_t port)
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### availableForWrite()



```c
int EthernetClient::availableForWrite(void)
```

!!! note "戻り値"
	int



### write()



```c
size_t EthernetClient::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t EthernetClient::write(const uint8_t *buf, size_t size)
```

!!! summary "引数"
	- constuint8_t * `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### available()



```c
int EthernetClient::available()
```

!!! note "戻り値"
	int



### read()



```c
int EthernetClient::read()
```

!!! note "戻り値"
	int



### read()



```c
int EthernetClient::read(uint8_t *buf, size_t size)
```

!!! summary "引数"
	- uint8_t * `buf` 
	- size_t `size` 

!!! note "戻り値"
	int



### peek()



```c
int EthernetClient::peek()
```

!!! note "戻り値"
	int



### flush()



```c
void EthernetClient::flush()
```



### stop()



```c
void EthernetClient::stop()
```



### connected()



```c
uint8_t EthernetClient::connected()
```

!!! note "戻り値"
	uint8_t



### operator bool()



```c
virtual EthernetClient::operator bool()
```



### operator==()



```c
virtual bool EthernetClient::operator==(const bool value)
```

!!! summary "引数"
	- const `value` 

!!! note "戻り値"
	bool



### operator!=()



```c
virtual bool EthernetClient::operator!=(const bool value)
```

!!! summary "引数"
	- const `value` 

!!! note "戻り値"
	bool



### operator==()



```c
bool EthernetClient::operator==(const EthernetClient &)
```

!!! summary "引数"
	- const& `` 

!!! note "戻り値"
	bool



### operator!=()



```c
virtual bool EthernetClient::operator!=(const EthernetClient &rhs)
```

!!! summary "引数"
	- const& `rhs` 

!!! note "戻り値"
	bool



### getSocketNumber()



```c
uint8_t EthernetClient::getSocketNumber() const
```

!!! note "戻り値"
	uint8_t



### localPort()



```c
uint16_t EthernetClient::localPort()
```

!!! note "戻り値"
	uint16_t



### remoteIP()



```c
IPAddress EthernetClient::remoteIP()
```

!!! note "戻り値"
	IPAddress



### remotePort()



```c
uint16_t EthernetClient::remotePort()
```

!!! note "戻り値"
	uint16_t



### setConnectionTimeout()



```c
virtual void EthernetClient::setConnectionTimeout(uint16_t timeout)
```

!!! summary "引数"
	- uint16_t `timeout` 



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



