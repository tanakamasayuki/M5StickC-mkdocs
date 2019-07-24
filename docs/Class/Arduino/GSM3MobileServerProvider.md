# GSM3MobileServerProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_mobile_server_provider.html)

## メンバー

### minSocketAsServer()


minSocketAsServer 

```c
virtual int GSM3MobileServerProvider::minSocketAsServer()=0
```

!!! note "戻り値"
	int socket 



### maxSocketAsServer()


maxSocketAsServer 

```c
virtual int GSM3MobileServerProvider::maxSocketAsServer()=0
```

!!! note "戻り値"
	int socket 



### ready()


Get last command status 

```c
virtual int GSM3MobileServerProvider::ready()=0
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



### GSM3MobileServerProvider()


Constructor 
```c
GSM3MobileServerProvider::GSM3MobileServerProvider()
```



### connectTCPServer()



```c
virtual int GSM3MobileServerProvider::connectTCPServer(int port)=0
```

!!! summary "引数"
	- int `port` TCP port 

!!! note "戻り値"
	int command error if exists 



### getNewOccupiedSocketAsServer()


Get new occupied socket as server 

```c
virtual int GSM3MobileServerProvider::getNewOccupiedSocketAsServer()=0
```

!!! note "戻り値"
	int return -1 if no new socket has been occupied 



### getStatusSocketAsServer()



```c
virtual bool GSM3MobileServerProvider::getStatusSocketAsServer(uint8_t socket)=0
```

!!! summary "引数"
	- uint8_t `socket` Socket 

!!! note "戻り値"
	bool socket status (true if connected) 



