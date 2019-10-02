# GSM3MobileClientService



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_mobile_client_service.html)

## メンバー

### GSM3MobileClientService()



```c
GSM3MobileClientService::GSM3MobileClientService(bool synch=true)
```

!!! summary "引数"
	- bool `synch` Sync mode 



### GSM3MobileClientService()



```c
GSM3MobileClientService::GSM3MobileClientService(int socket, bool synch)
```

!!! summary "引数"
	- int `socket` Socket 
	- bool `synch` Sync mode 



### ready()


Get last command status 

```c
int GSM3MobileClientService::ready()
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



### connect()



```c
int GSM3MobileClientService::connect(IPAddress, uint16_t)
```

!!! summary "引数"
	- uint16_t `` 

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, 2 if there are no resources 



### connect()



```c
int GSM3MobileClientService::connect(const char *host, uint16_t port)
```

!!! summary "引数"
	- constchar * `host` Hostname 
	- uint16_t `port` Port 

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, 2 if there are no resources 



### beginWrite()



```c
void GSM3MobileClientService::beginWrite(bool sync=false)
```

!!! summary "引数"
	- bool `sync` Sync mode 



### write()



```c
size_t GSM3MobileClientService::write(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` Character 

!!! note "戻り値"
	size_t size 



### write()



```c
size_t GSM3MobileClientService::write(const uint8_t *buf)
```

!!! summary "引数"
	- constuint8_t * `buf` Buffer 

!!! note "戻り値"
	size_t buffer size 



### write()



```c
size_t GSM3MobileClientService::write(const uint8_t *, size_t)
```

!!! summary "引数"
	- size_t `` 

!!! note "戻り値"
	size_t buffer size 



### endWrite()



```c
void GSM3MobileClientService::endWrite(bool sync=false)
```

!!! summary "引数"
	- bool `sync` Sync mode 



### connected()


Check if connected to server 

```c
uint8_t GSM3MobileClientService::connected()
```

!!! note "戻り値"
	uint8_t 1 if connected 



### operator bool()



```c
GSM3MobileClientService::operator bool()
```



### read()



```c
int GSM3MobileClientService::read(uint8_t *buf, size_t size)
```

!!! summary "引数"
	- uint8_t * `buf` Buffer
	- size_t `size` Buffer size 

!!! note "戻り値"
	int bytes read 



### read()


Read a character from response buffer 

```c
int GSM3MobileClientService::read()
```

!!! note "戻り値"
	int character 



### available()


Check if exists a response available 

```c
int GSM3MobileClientService::available()
```

!!! note "戻り値"
	int 1 if exists, 0 if not exists 



### peek()


Read a character from response buffer but does not move the pointer. 

```c
int GSM3MobileClientService::peek()
```

!!! note "戻り値"
	int character 



### flush()


Flush response buffer 
```c
void GSM3MobileClientService::flush()
```



### stop()


Stop client 
```c
void GSM3MobileClientService::stop()
```



### getSocket()


Get socket 

```c
int GSM3MobileClientService::getSocket()
```

!!! note "戻り値"
	int socket 



