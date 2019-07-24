# WiFiClient



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_wi_fi_client.html)

## メンバー

###  next

```c
WiFiClient* WiFiClient::next
```


### WiFiClient()



```c
WiFiClient::WiFiClient()
```



### WiFiClient()



```c
WiFiClient::WiFiClient(int fd)
```

!!! summary "引数"
	- int `fd` 



### ~WiFiClient()



```c
WiFiClient::~WiFiClient()
```



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
int WiFiClient::connect(IPAddress ip, uint16_t port, int32_t timeout)
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 
	- int32_t `timeout` 

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



### connect()



```c
int WiFiClient::connect(const char *host, uint16_t port, int32_t timeout)
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 
	- int32_t `timeout` 

!!! note "戻り値"
	int



### write()



```c
size_t WiFiClient::write(uint8_t data)
```

!!! summary "引数"
	- uint8_t `data` 

!!! note "戻り値"
	size_t



### write()



```c
size_t WiFiClient::write(const uint8_t *buf, size_t size)
```

!!! summary "引数"
	- const* `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### write_P()



```c
size_t WiFiClient::write_P(PGM_P buf, size_t size)
```

!!! summary "引数"
	- PGM_P `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### write()



```c
size_t WiFiClient::write(Stream &stream)
```

!!! summary "引数"
	- Stream& `stream` 

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
	- uint8_t* `buf` 
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



### operator=()



```c
WiFiClient & WiFiClient::operator=(const WiFiClient &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	WiFiClient&



### operator==()



```c
bool WiFiClient::operator==(const bool value)
```

!!! summary "引数"
	- const `value` 

!!! note "戻り値"
	bool



### operator!=()



```c
bool WiFiClient::operator!=(const bool value)
```

!!! summary "引数"
	- const `value` 

!!! note "戻り値"
	bool



### operator==()



```c
bool WiFiClient::operator==(const WiFiClient &)
```

!!! summary "引数"
	- const& `` 

!!! note "戻り値"
	bool



### operator!=()



```c
bool WiFiClient::operator!=(const WiFiClient &rhs)
```

!!! summary "引数"
	- const& `rhs` 

!!! note "戻り値"
	bool



### fd()



```c
int WiFiClient::fd() const
```

!!! note "戻り値"
	int



### setSocketOption()



```c
int WiFiClient::setSocketOption(int option, char *value, size_t len)
```

!!! summary "引数"
	- int `option` 
	- char * `value` 
	- size_t `len` 

!!! note "戻り値"
	int



### setOption()



```c
int WiFiClient::setOption(int option, int *value)
```

!!! summary "引数"
	- int `option` 
	- int * `value` 

!!! note "戻り値"
	int



### getOption()



```c
int WiFiClient::getOption(int option, int *value)
```

!!! summary "引数"
	- int `option` 
	- int * `value` 

!!! note "戻り値"
	int



### setTimeout()



```c
int WiFiClient::setTimeout(uint32_t seconds)
```

!!! summary "引数"
	- uint32_t `seconds` 

!!! note "戻り値"
	int



### setNoDelay()



```c
int WiFiClient::setNoDelay(bool nodelay)
```

!!! summary "引数"
	- bool `nodelay` 

!!! note "戻り値"
	int



### getNoDelay()



```c
bool WiFiClient::getNoDelay()
```

!!! note "戻り値"
	bool



### remoteIP()



```c
IPAddress WiFiClient::remoteIP() const
```

!!! note "戻り値"
	IPAddress



### remoteIP()



```c
IPAddress WiFiClient::remoteIP(int fd) const
```

!!! summary "引数"
	- int `fd` 

!!! note "戻り値"
	IPAddress



### remotePort()



```c
uint16_t WiFiClient::remotePort() const
```

!!! note "戻り値"
	uint16_t



### remotePort()



```c
uint16_t WiFiClient::remotePort(int fd) const
```

!!! summary "引数"
	- int `fd` 

!!! note "戻り値"
	uint16_t



### localIP()



```c
IPAddress WiFiClient::localIP() const
```

!!! note "戻り値"
	IPAddress



### localIP()



```c
IPAddress WiFiClient::localIP(int fd) const
```

!!! summary "引数"
	- int `fd` 

!!! note "戻り値"
	IPAddress



### localPort()



```c
uint16_t WiFiClient::localPort() const
```

!!! note "戻り値"
	uint16_t



### localPort()



```c
uint16_t WiFiClient::localPort(int fd) const
```

!!! summary "引数"
	- int `fd` 

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



