# GSM3MobileClientProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_mobile_client_provider.html)

## メンバー

### GSM3MobileClientProvider()


Constructor 
```c
GSM3MobileClientProvider::GSM3MobileClientProvider()
```



### minSocket()


Minimum socket 

```c
virtual int GSM3MobileClientProvider::minSocket()=0
```

!!! note "戻り値"
	int socket 



### maxSocket()


Maximum socket 

```c
virtual int GSM3MobileClientProvider::maxSocket()=0
```

!!! note "戻り値"
	int socket 



### ready()


Get last command status 

```c
virtual int GSM3MobileClientProvider::ready()=0
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



### getStatusSocketClient()



```c
virtual bool GSM3MobileClientProvider::getStatusSocketClient(uint8_t socket)=0
```

!!! summary "引数"
	- uint8_t `socket` Socket 

!!! note "戻り値"
	bool 1 if connected 



### getSocket()



```c
virtual int GSM3MobileClientProvider::getSocket(int socket=-1)=0
```

!!! summary "引数"
	- int `socket` Socket 

!!! note "戻り値"
	int socket 



### releaseSocket()



```c
virtual void GSM3MobileClientProvider::releaseSocket(int socket)=0
```

!!! summary "引数"
	- int `socket` Socket 



### connectTCPClient()



```c
virtual int GSM3MobileClientProvider::connectTCPClient(const char *server, int port, int id_socket)=0
```

!!! summary "引数"
	- constchar * `server`  name or IP address in a String 
	- int `port` Port 
	- int `id_socket` Socket 

!!! note "戻り値"
	int 0 if command running, 1 if success, otherwise error 



### connectTCPClient()



```c
virtual int GSM3MobileClientProvider::connectTCPClient(IPAddress add, int port, int id_socket)=0
```

!!! summary "引数"
	- IPAddress `add` IP address in  format 
	- int `port` Port 
	- int `id_socket` Socket 

!!! note "戻り値"
	int 0 if command running, 1 if success, otherwise error 



### beginWriteSocket()



```c
virtual void GSM3MobileClientProvider::beginWriteSocket(bool client1Server0, int id_socket)=0
```

!!! summary "引数"
	- bool `client1Server0` 1 if modem acts as client, 0 if acts as server 
	- int `id_socket` Local socket number 



### writeSocket()



```c
virtual void GSM3MobileClientProvider::writeSocket(uint8_t c)=0
```

!!! summary "引数"
	- uint8_t `c` character to be written 



### writeSocket()



```c
virtual void GSM3MobileClientProvider::writeSocket(const char *buf)=0
```

!!! summary "引数"
	- constchar * `buf` characters to be written (final 0 will not be written) 



### endWriteSocket()


Finish current writing 
```c
virtual void GSM3MobileClientProvider::endWriteSocket()=0
```



### availableSocket()



```c
virtual int GSM3MobileClientProvider::availableSocket(bool client, int id_socket)=0
```

!!! summary "引数"
	- bool `client` 
	- int `id_socket` Local socket number 

!!! note "戻り値"
	int 0 if command running, 1 if there are data available, 4 if no data, otherwise error 



### readSocket()


Read data (get a character) available in socket 

```c
virtual int GSM3MobileClientProvider::readSocket()=0
```

!!! note "戻り値"
	int character 



### flushSocket()


Flush socket 
```c
virtual void GSM3MobileClientProvider::flushSocket()=0
```



### peekSocket()


Get a character but will not advance the buffer head 

```c
virtual int GSM3MobileClientProvider::peekSocket()=0
```

!!! note "戻り値"
	int character 



### disconnectTCP()



```c
virtual int GSM3MobileClientProvider::disconnectTCP(bool client1Server0, int idsocket)=0
```

!!! summary "引数"
	- bool `client1Server0` 1 if modem acts as client, 0 if acts as server 
	- int `idsocket` 

!!! note "戻り値"
	int 0 if command running, 1 if success, otherwise error 



