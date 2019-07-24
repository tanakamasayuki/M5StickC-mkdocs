# Client



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_client.html)

## メンバー

### connect()



```c
virtual int Client::connect(IPAddress ip, uint16_t port)=0
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### connect()



```c
virtual int Client::connect(const char *host, uint16_t port)=0
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 

!!! note "戻り値"
	int



### connect()



```c
virtual int Client::connect(IPAddress ip, uint16_t port, int timeout)=0
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 
	- int `timeout` 

!!! note "戻り値"
	int



### connect()



```c
virtual int Client::connect(const char *host, uint16_t port, int timeout)=0
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 
	- int `timeout` 

!!! note "戻り値"
	int



### write()



```c
virtual size_t Client::write(uint8_t)=0
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
virtual size_t Client::write(const uint8_t *buf, size_t size)=0
```

!!! summary "引数"
	- const* `buf` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### available()



```c
virtual int Client::available()=0
```

!!! note "戻り値"
	int



### read()



```c
virtual int Client::read()=0
```

!!! note "戻り値"
	int



### read()



```c
virtual int Client::read(uint8_t *buf, size_t size)=0
```

!!! summary "引数"
	- uint8_t* `buf` 
	- size_t `size` 

!!! note "戻り値"
	int



### peek()



```c
virtual int Client::peek()=0
```

!!! note "戻り値"
	int



### flush()



```c
virtual void Client::flush()=0
```



### stop()



```c
virtual void Client::stop()=0
```



### connected()



```c
virtual uint8_t Client::connected()=0
```

!!! note "戻り値"
	uint8_t



### operator bool()



```c
virtual Client::operator bool()=0
```



