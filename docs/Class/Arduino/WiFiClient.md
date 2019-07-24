# WiFiClient



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_wi_fi_client.html)

## メンバー



### WiFiClient()



```c
WiFiClient::WiFiClient()
```



### WiFiClient()



```c
WiFiClient::WiFiClient(uint8_t sock)
```

!!! summary "引数"
	- uint8_t `sock` 



### status()



```c
uint8_t WiFiClient::status()
```

!!! note "戻り値"
	uint8_t



### connect()



```c
int WiFiClient::connect(IPAddress ip, uint16_t port)
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### connect()



```c
int WiFiClient::connect(const char *host, uint16_t port)
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### write()



```c
size_t WiFiClient::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t WiFiClient::write(const uint8_t *buf, size_t size)
```

!!! summary "引数"
	- constuint8_t * `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### available()



```c
int WiFiClient::available()
```

!!! note "戻り値"
	int



### read()



```c
int WiFiClient::read()
```

!!! note "戻り値"
	int



### read()



```c
int WiFiClient::read(uint8_t *buf, size_t size)
```

!!! summary "引数"
	- uint8_t * `buf` 
	- size_t `size` 

!!! note "戻り値"
	int



### peek()



```c
int WiFiClient::peek()
```

!!! note "戻り値"
	int



### flush()



```c
void WiFiClient::flush()
```



### stop()



```c
void WiFiClient::stop()
```



### connected()



```c
uint8_t WiFiClient::connected()
```

!!! note "戻り値"
	uint8_t



### operator bool()



```c
WiFiClient::operator bool()
```



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



