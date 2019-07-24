# GSM3MobileNetworkProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_mobile_network_provider.html)

## メンバー

### minSocketAsServer()


minSocketAsServer 

```c
virtual int GSM3MobileNetworkProvider::minSocketAsServer()
```

!!! note "戻り値"
	int 0 



### maxSocketAsServer()


maxSocketAsServer 

```c
virtual int GSM3MobileNetworkProvider::maxSocketAsServer()
```

!!! note "戻り値"
	int 0 



### ready()


Get last command status 

```c
virtual int GSM3MobileNetworkProvider::ready()=0
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



### GSM3MobileNetworkProvider()


Constructor 
```c
GSM3MobileNetworkProvider::GSM3MobileNetworkProvider()
```



### getStatus()


Get network status 

```c
virtual GSM3_NetworkStatus_t GSM3MobileNetworkProvider::getStatus()
```

!!! note "戻り値"
	GSM3_NetworkStatus_t network status 



### getStatusSocketClient()



```c
bool GSM3MobileNetworkProvider::getStatusSocketClient(uint8_t socket)
```

!!! summary "引数"
	- uint8_t `socket` Socket 

!!! note "戻り値"
	bool 1 if connected, 0 otherwise 



### closeCommand()



```c
virtual void GSM3MobileNetworkProvider::closeCommand(int code)
```

!!! summary "引数"
	- int `code` Close code 



### connectTCPServer()



```c
virtual int GSM3MobileNetworkProvider::connectTCPServer(int port, char *localIP, int localIPlength)
```

!!! summary "引数"
	- int `port` Port 
	- char * `localIP` IP address 
	- int `localIPlength` IP address size in characters 

!!! note "戻り値"
	int command error if exists 



### getIP()



```c
virtual int GSM3MobileNetworkProvider::getIP(char *LocalIP, int LocalIPlength)
```

!!! summary "引数"
	- char * `LocalIP` Buffer for save IP address 
	- int `LocalIPlength` Buffer size 

!!! note "戻り値"
	int



### getNewOccupiedSocketAsServer()


Get new occupied socket 

```c
int GSM3MobileNetworkProvider::getNewOccupiedSocketAsServer()
```

!!! note "戻り値"
	int -1 if no new socket has been occupied 



### getStatusSocketAsServer()



```c
bool GSM3MobileNetworkProvider::getStatusSocketAsServer(uint8_t socket)
```

!!! summary "引数"
	- uint8_t `socket` Socket to get status 

!!! note "戻り値"
	bool socket status 



### disconnectTCP()



```c
int GSM3MobileNetworkProvider::disconnectTCP(bool client1Server0, int idsocket)
```

!!! summary "引数"
	- bool `client1Server0` 1 if modem acts as client, 0 if acts as server 
	- int `idsocket` 

!!! note "戻り値"
	int 0 if command running, 1 if success, otherwise error 



### releaseSocket()



```c
void GSM3MobileNetworkProvider::releaseSocket(int socket)
```

!!! summary "引数"
	- int `socket` Socket 



