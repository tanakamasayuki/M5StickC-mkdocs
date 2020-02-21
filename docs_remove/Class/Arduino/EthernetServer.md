# EthernetServer



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_ethernet_server.html)

## メンバー

###  server_port

```c
uint16_t EthernetServer::server_port
```


### EthernetServer()



```c
EthernetServer::EthernetServer(uint16_t port)
```

!!! summary "引数"
	- uint16_t `port` 



### available()



```c
EthernetClient EthernetServer::available()
```

!!! note "戻り値"
	EthernetClient



### accept()



```c
EthernetClient EthernetServer::accept()
```

!!! note "戻り値"
	EthernetClient



### begin()



```c
void EthernetServer::begin()
```



### write()



```c
size_t EthernetServer::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t EthernetServer::write(const uint8_t *buf, size_t size)
```

!!! summary "引数"
	- constuint8_t * `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### operator bool()



```c
EthernetServer::operator bool()
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



