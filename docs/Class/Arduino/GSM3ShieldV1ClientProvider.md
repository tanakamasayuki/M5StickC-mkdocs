# GSM3ShieldV1ClientProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_shield_v1_client_provider.html)

## メンバー

### GSM3ShieldV1ClientProvider()


Constructor 
```c
GSM3ShieldV1ClientProvider::GSM3ShieldV1ClientProvider()
```



### minSocket()


minSocket 

```c
int GSM3ShieldV1ClientProvider::minSocket()
```

!!! note "戻り値"
	int 0 



### maxSocket()


maxSocket 

```c
int GSM3ShieldV1ClientProvider::maxSocket()
```

!!! note "戻り値"
	int 0 



### connectTCPClient()



```c
int GSM3ShieldV1ClientProvider::connectTCPClient(const char *server, int port, int id_socket)
```

!!! summary "引数"
	- constchar * `server` String with IP or server name 
	- int `port` Remote port number 
	- int `id_socket` Local socket number 

!!! note "戻り値"
	int 0 if command running, 1 if success, otherwise error 



### connectTCPClient()



```c
int GSM3ShieldV1ClientProvider::connectTCPClient(IPAddress add, int port, int id_socket)
```

!!! summary "引数"
	- IPAddress `add` Remote IP address 
	- int `port` Remote port number 
	- int `id_socket` Local socket number 

!!! note "戻り値"
	int 0 if command running, 1 if success, otherwise error 



### beginWriteSocket()



```c
void GSM3ShieldV1ClientProvider::beginWriteSocket(bool client1Server0, int id_socket)
```

!!! summary "引数"
	- bool `client1Server0` 1 if modem acts as client, 0 if acts as server 
	- int `id_socket` Local socket number 



### writeSocket()



```c
void GSM3ShieldV1ClientProvider::writeSocket(const char *buf)
```

!!! summary "引数"
	- constchar * `buf` characters to be written (final 0 will not be written) 



### writeSocket()



```c
void GSM3ShieldV1ClientProvider::writeSocket(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` character to be written 



### endWriteSocket()


Finish current writing 
```c
void GSM3ShieldV1ClientProvider::endWriteSocket()
```



### availableSocket()



```c
int GSM3ShieldV1ClientProvider::availableSocket(bool client, int id_socket)
```

!!! summary "引数"
	- bool `client` 
	- int `id_socket` Local socket number 

!!! note "戻り値"
	int 0 if command running, 1 if there are data available, 4 if no data, otherwise error 



### readSocket()


Read data (get a character) available in socket 

```c
int GSM3ShieldV1ClientProvider::readSocket()
```

!!! note "戻り値"
	int character 



### flushSocket()


Flush socket 
```c
void GSM3ShieldV1ClientProvider::flushSocket()
```



### peekSocket()


Get a character but will not advance the buffer head 

```c
int GSM3ShieldV1ClientProvider::peekSocket()
```

!!! note "戻り値"
	int character 



### disconnectTCP()



```c
int GSM3ShieldV1ClientProvider::disconnectTCP(bool client1Server0, int id_socket)
```

!!! summary "引数"
	- bool `client1Server0` 1 if modem acts as client, 0 if acts as server 
	- int `id_socket` Socket 

!!! note "戻り値"
	int 0 if command running, 1 if success, otherwise error 



### recognizeUnsolicitedEvent()



```c
bool GSM3ShieldV1ClientProvider::recognizeUnsolicitedEvent(byte from)
```

!!! summary "引数"
	- byte `from` 

!!! note "戻り値"
	bool true if successful 



### manageResponse()



```c
void GSM3ShieldV1ClientProvider::manageResponse(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Initial byte position 
	- byte `to` Final byte position 



### ready()


Get last command status 

```c
int GSM3ShieldV1ClientProvider::ready()
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



### getSocket()



```c
int GSM3ShieldV1ClientProvider::getSocket(int socket=-1)
```

!!! summary "引数"
	- int `socket` Socket

!!! note "戻り値"
	int socket 



### releaseSocket()



```c
void GSM3ShieldV1ClientProvider::releaseSocket(int socket)
```

!!! summary "引数"
	- int `socket` Socket 



### getStatusSocketClient()



```c
bool GSM3ShieldV1ClientProvider::getStatusSocketClient(uint8_t socket)
```

!!! summary "引数"
	- uint8_t `socket` Socket 

!!! note "戻り値"
	bool 1 if connected, 0 otherwise 



