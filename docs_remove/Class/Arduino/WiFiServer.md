# WiFiServer



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_wi_fi_server.html)

## メンバー

### WiFiServer()



```c
WiFiServer::WiFiServer(uint16_t)
```

!!! summary "引数"
	- uint16_t `` 



### available()



```c
WiFiClient WiFiServer::available(uint8_t *status=NULL)
```

!!! summary "引数"
	- uint8_t * `status` 

!!! note "戻り値"
	WiFiClient



### begin()



```c
void WiFiServer::begin()
```



### write()



```c
size_t WiFiServer::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t WiFiServer::write(const uint8_t *buf, size_t size)
```

!!! summary "引数"
	- constuint8_t * `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### status()



```c
uint8_t WiFiServer::status()
```

!!! note "戻り値"
	uint8_t



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



