# WiFiClientSecure



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_wi_fi_client_secure.html)

## メンバー

###  next

```c
WiFiClientSecure* WiFiClientSecure::next
```


### WiFiClientSecure()



```c
WiFiClientSecure::WiFiClientSecure()
```



### WiFiClientSecure()



```c
WiFiClientSecure::WiFiClientSecure(int socket)
```

!!! summary "引数"
	- int `socket` 



### ~WiFiClientSecure()



```c
WiFiClientSecure::~WiFiClientSecure()
```



### connect()



```c
int WiFiClientSecure::connect(IPAddress ip, uint16_t port)
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### connect()



```c
int WiFiClientSecure::connect(IPAddress ip, uint16_t port, int32_t timeout)
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 
	- int32_t `timeout` 

!!! note "戻り値"
	int



### connect()



```c
int WiFiClientSecure::connect(const char *host, uint16_t port)
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### connect()



```c
int WiFiClientSecure::connect(const char *host, uint16_t port, int32_t timeout)
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 
	- int32_t `timeout` 

!!! note "戻り値"
	int



### connect()



```c
int WiFiClientSecure::connect(IPAddress ip, uint16_t port, const char *rootCABuff, const char *cli_cert, const char *cli_key)
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 
	- constchar * `rootCABuff` 
	- constchar * `cli_cert` 
	- constchar * `cli_key` 

!!! note "戻り値"
	int



### connect()



```c
int WiFiClientSecure::connect(const char *host, uint16_t port, const char *rootCABuff, const char *cli_cert, const char *cli_key)
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 
	- constchar * `rootCABuff` 
	- constchar * `cli_cert` 
	- constchar * `cli_key` 

!!! note "戻り値"
	int



### connect()



```c
int WiFiClientSecure::connect(IPAddress ip, uint16_t port, const char *pskIdent, const char *psKey)
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 
	- constchar * `pskIdent` 
	- constchar * `psKey` 

!!! note "戻り値"
	int



### connect()



```c
int WiFiClientSecure::connect(const char *host, uint16_t port, const char *pskIdent, const char *psKey)
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 
	- constchar * `pskIdent` 
	- constchar * `psKey` 

!!! note "戻り値"
	int



### peek()



```c
int WiFiClientSecure::peek()
```

!!! note "戻り値"
	int



### write()



```c
size_t WiFiClientSecure::write(uint8_t data)
```

!!! summary "引数"
	- uint8_t `data` 

!!! note "戻り値"
	size_t



### write()



```c
size_t WiFiClientSecure::write(const uint8_t *buf, size_t size)
```

!!! summary "引数"
	- const* `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### available()



```c
int WiFiClientSecure::available()
```

!!! note "戻り値"
	int



### read()



```c
int WiFiClientSecure::read()
```

!!! note "戻り値"
	int



### read()



```c
int WiFiClientSecure::read(uint8_t *buf, size_t size)
```

!!! summary "引数"
	- uint8_t* `buf` 
	- size_t `size` 

!!! note "戻り値"
	int



### flush()



```c
void WiFiClientSecure::flush()
```



### stop()



```c
void WiFiClientSecure::stop()
```



### connected()



```c
uint8_t WiFiClientSecure::connected()
```

!!! note "戻り値"
	uint8_t



### lastError()



```c
int WiFiClientSecure::lastError(char *buf, const size_t size)
```

!!! summary "引数"
	- char * `buf` 
	- constsize_t `size` 

!!! note "戻り値"
	int



### setPreSharedKey()



```c
void WiFiClientSecure::setPreSharedKey(const char *pskIdent, const char *psKey)
```

!!! summary "引数"
	- constchar * `pskIdent` 
	- constchar * `psKey` 



### setCACert()



```c
void WiFiClientSecure::setCACert(const char *rootCA)
```

!!! summary "引数"
	- constchar * `rootCA` 



### setCertificate()



```c
void WiFiClientSecure::setCertificate(const char *client_ca)
```

!!! summary "引数"
	- constchar * `client_ca` 



### setPrivateKey()



```c
void WiFiClientSecure::setPrivateKey(const char *private_key)
```

!!! summary "引数"
	- constchar * `private_key` 



### loadCACert()



```c
bool WiFiClientSecure::loadCACert(Stream &stream, size_t size)
```

!!! summary "引数"
	- Stream& `stream` 
	- size_t `size` 

!!! note "戻り値"
	bool



### loadCertificate()



```c
bool WiFiClientSecure::loadCertificate(Stream &stream, size_t size)
```

!!! summary "引数"
	- Stream& `stream` 
	- size_t `size` 

!!! note "戻り値"
	bool



### loadPrivateKey()



```c
bool WiFiClientSecure::loadPrivateKey(Stream &stream, size_t size)
```

!!! summary "引数"
	- Stream& `stream` 
	- size_t `size` 

!!! note "戻り値"
	bool



### verify()



```c
bool WiFiClientSecure::verify(const char *fingerprint, const char *domain_name)
```

!!! summary "引数"
	- constchar * `fingerprint` 
	- constchar * `domain_name` 

!!! note "戻り値"
	bool



### setHandshakeTimeout()



```c
void WiFiClientSecure::setHandshakeTimeout(unsigned long handshake_timeout)
```

!!! summary "引数"
	- unsigned long `handshake_timeout` 



### setTimeout()



```c
int WiFiClientSecure::setTimeout(uint32_t seconds)
```

!!! summary "引数"
	- uint32_t `seconds` 

!!! note "戻り値"
	int



### operator bool()



```c
WiFiClientSecure::operator bool()
```



### operator=()



```c
WiFiClientSecure & WiFiClientSecure::operator=(const WiFiClientSecure &other)
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	WiFiClientSecure&



### operator==()



```c
bool WiFiClientSecure::operator==(const bool value)
```

!!! summary "引数"
	- const `value` 

!!! note "戻り値"
	bool



### operator!=()



```c
bool WiFiClientSecure::operator!=(const bool value)
```

!!! summary "引数"
	- const `value` 

!!! note "戻り値"
	bool



### operator==()



```c
bool WiFiClientSecure::operator==(const WiFiClientSecure &)
```

!!! summary "引数"
	- const& `` 

!!! note "戻り値"
	bool



### operator!=()



```c
bool WiFiClientSecure::operator!=(const WiFiClientSecure &rhs)
```

!!! summary "引数"
	- const& `rhs` 

!!! note "戻り値"
	bool



### socket()



```c
int WiFiClientSecure::socket()
```

!!! note "戻り値"
	int



