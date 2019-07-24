# WiFiServer



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_wi_fi_server.html)

## メンバー

### listenOnLocalhost()



```c
void WiFiServer::listenOnLocalhost()
```



### WiFiServer()



```c
WiFiServer::WiFiServer(uint16_t port=80, uint8_t max_clients=4)
```

!!! summary "引数"
	- uint16_t `port` 
	- uint8_t `max_clients` 



### ~WiFiServer()



```c
WiFiServer::~WiFiServer()
```



### available()



```c
WiFiClient WiFiServer::available()
```

!!! note "戻り値"
	WiFiClient



### accept()



```c
WiFiClient WiFiServer::accept()
```

!!! note "戻り値"
	WiFiClient



### begin()



```c
void WiFiServer::begin(uint16_t port=0)
```

!!! summary "引数"
	- uint16_t `port` 



### setNoDelay()



```c
void WiFiServer::setNoDelay(bool nodelay)
```

!!! summary "引数"
	- bool `nodelay` 



### getNoDelay()



```c
bool WiFiServer::getNoDelay()
```

!!! note "戻り値"
	bool



### hasClient()



```c
bool WiFiServer::hasClient()
```

!!! note "戻り値"
	bool



### write()



```c
size_t WiFiServer::write(const uint8_t *data, size_t len)
```

!!! summary "引数"
	- const* `data` 
	- size_t `len` 

!!! note "戻り値"
	size_t



### write()



```c
size_t WiFiServer::write(uint8_t data)
```

!!! summary "引数"
	- uint8_t `data` 

!!! note "戻り値"
	size_t



### end()



```c
void WiFiServer::end()
```



### close()



```c
void WiFiServer::close()
```



### stop()



```c
void WiFiServer::stop()
```



### operator bool()



```c
WiFiServer::operator bool()
```



### setTimeout()



```c
int WiFiServer::setTimeout(uint32_t seconds)
```

!!! summary "引数"
	- uint32_t `seconds` 

!!! note "戻り値"
	int



### stopAll()



```c
void WiFiServer::stopAll()
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



