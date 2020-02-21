# GSM3ShieldV1MultiClientProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_shield_v1_multi_client_provider.html)

## メンバー

### GSM3ShieldV1MultiClientProvider()


Constructor 
```c
GSM3ShieldV1MultiClientProvider::GSM3ShieldV1MultiClientProvider()
```



### minSocket()


Minimum socket 

```c
int GSM3ShieldV1MultiClientProvider::minSocket()
```

!!! note "戻り値"
	int 0 



### maxSocket()


Maximum socket 

```c
int GSM3ShieldV1MultiClientProvider::maxSocket()
```

!!! note "戻り値"
	int 5 



### connectTCPClient()



```c
int GSM3ShieldV1MultiClientProvider::connectTCPClient(const char *server, int port, int id_socket)
```

!!! summary "引数"
	- constchar * `server` String with IP or server name 
	- int `port` Remote port number 
	- int `id_socket` Local socket number 

!!! note "戻り値"
	int 0 if command running, 1 if success, otherwise error 



### connectTCPClient()



```c
int GSM3ShieldV1MultiClientProvider::connectTCPClient(IPAddress add, int port, int id_socket)
```

!!! summary "引数"
	- IPAddress `add` Remote IP address 
	- int `port` Remote port number 
	- int `id_socket` Local socket number 

!!! note "戻り値"
	int 0 if command running, 1 if success, otherwise error 



### beginWriteSocket()



```c
void GSM3ShieldV1MultiClientProvider::beginWriteSocket(bool client1Server0, int id_socket)
```

!!! summary "引数"
	- bool `client1Server0` 1 if modem acts as client, 0 if acts as server 
	- int `id_socket` Local socket number 



### writeSocket()



```c
void GSM3ShieldV1MultiClientProvider::writeSocket(const char *buf)
```

!!! summary "引数"
	- constchar * `buf` characters to be written (final 0 will not be written) 



### writeSocket()



```c
void GSM3ShieldV1MultiClientProvider::writeSocket(char c)
```

!!! summary "引数"
	- char `c` character to be written 



### endWriteSocket()


Finish current writing 
```c
void GSM3ShieldV1MultiClientProvider::endWriteSocket()
```



### availableSocket()



```c
int GSM3ShieldV1MultiClientProvider::availableSocket(bool client, int id_socket)
```

!!! summary "引数"
	- bool `client` 
	- int `id_socket` Local socket number 

!!! note "戻り値"
	int 0 if command running, 1 if there are data available, 4 if no data, otherwise error 



### readSocket()


Read a character from socket 

```c
int GSM3ShieldV1MultiClientProvider::readSocket()
```

!!! note "戻り値"
	int socket 



### flushSocket()


Flush socket 
```c
void GSM3ShieldV1MultiClientProvider::flushSocket()
```



### peekSocket()


Get a character but will not advance the buffer head 

```c
int GSM3ShieldV1MultiClientProvider::peekSocket()
```

!!! note "戻り値"
	int character 



### disconnectTCP()



```c
int GSM3ShieldV1MultiClientProvider::disconnectTCP(bool client1Server0, int id_socket)
```

!!! summary "引数"
	- bool `client1Server0` 1 if modem acts as client, 0 if acts as server 
	- int `id_socket` Local socket number 

!!! note "戻り値"
	int 0 if command running, 1 if success, otherwise error 



### recognizeUnsolicitedEvent()



```c
bool GSM3ShieldV1MultiClientProvider::recognizeUnsolicitedEvent(byte from)
```

!!! summary "引数"
	- byte `from` 

!!! note "戻り値"
	bool true if successful 



### manageResponse()



```c
void GSM3ShieldV1MultiClientProvider::manageResponse(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Initial byte of buffer 
	- byte `to` Final byte of buffer 



### ready()


Get last command status 

```c
int GSM3ShieldV1MultiClientProvider::ready()
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



### getSocket()



```c
int GSM3ShieldV1MultiClientProvider::getSocket(int socket=-1)
```

!!! summary "引数"
	- int `socket` 

!!! note "戻り値"
	int socket 



### releaseSocket()



```c
void GSM3ShieldV1MultiClientProvider::releaseSocket(int socket)
```

!!! summary "引数"
	- int `socket` Socket for release 



### getStatusSocketClient()



```c
bool GSM3ShieldV1MultiClientProvider::getStatusSocketClient(uint8_t socket)
```

!!! summary "引数"
	- uint8_t `socket` Socket 

!!! note "戻り値"
	bool socket client status 



