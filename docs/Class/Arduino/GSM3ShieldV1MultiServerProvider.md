# GSM3ShieldV1MultiServerProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_shield_v1_multi_server_provider.html)

## メンバー

### GSM3ShieldV1MultiServerProvider()


Constructor 
```c
GSM3ShieldV1MultiServerProvider::GSM3ShieldV1MultiServerProvider()
```



### minSocketAsServer()


minSocketAsServer 

```c
int GSM3ShieldV1MultiServerProvider::minSocketAsServer()
```

!!! note "戻り値"
	int 0 



### maxSocketAsServer()


maxSocketAsServer 

```c
int GSM3ShieldV1MultiServerProvider::maxSocketAsServer()
```

!!! note "戻り値"
	int 0 



### getSocketAsServerModemStatus()



```c
bool GSM3ShieldV1MultiServerProvider::getSocketAsServerModemStatus(int s)
```

!!! summary "引数"
	- int `s` 

!!! note "戻り値"
	bool modem status (true if connected) 



### getNewOccupiedSocketAsServer()


Get new occupied socket as server 

```c
int GSM3ShieldV1MultiServerProvider::getNewOccupiedSocketAsServer()
```

!!! note "戻り値"
	int command error if exists 



### connectTCPServer()



```c
int GSM3ShieldV1MultiServerProvider::connectTCPServer(int port)
```

!!! summary "引数"
	- int `port` TCP port 

!!! note "戻り値"
	int command error if exists 



### getIP()



```c
int GSM3ShieldV1MultiServerProvider::getIP(char *LocalIP, int LocalIPlength)
```

!!! summary "引数"
	- char * `LocalIP` Buffer for copy IP address 
	- int `LocalIPlength` Length of buffer 

!!! note "戻り値"
	int command error if exists 



### ready()


Get last command status 

```c
int GSM3ShieldV1MultiServerProvider::ready()
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



### getStatusSocketAsServer()



```c
bool GSM3ShieldV1MultiServerProvider::getStatusSocketAsServer(uint8_t socket)
```

!!! summary "引数"
	- uint8_t `socket` Socket to get status 

!!! note "戻り値"
	bool socket status 



### manageResponse()



```c
void GSM3ShieldV1MultiServerProvider::manageResponse(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Initial byte of buffer 
	- byte `to` Final byte of buffer 



### recognizeUnsolicitedEvent()



```c
bool GSM3ShieldV1MultiServerProvider::recognizeUnsolicitedEvent(byte oldTail)
```

!!! summary "引数"
	- byte `oldTail` 

!!! note "戻り値"
	bool true if successful 



