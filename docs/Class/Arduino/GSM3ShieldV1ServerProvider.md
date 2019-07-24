# GSM3ShieldV1ServerProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_shield_v1_server_provider.html)

## メンバー

### GSM3ShieldV1ServerProvider()


Constructor 
```c
GSM3ShieldV1ServerProvider::GSM3ShieldV1ServerProvider()
```



### minSocketAsServer()


minSocketAsServer 

```c
int GSM3ShieldV1ServerProvider::minSocketAsServer()
```

!!! note "戻り値"
	int 0 



### maxSocketAsServer()


maxSocketAsServer 

```c
int GSM3ShieldV1ServerProvider::maxSocketAsServer()
```

!!! note "戻り値"
	int 0 



### getSocketAsServerModemStatus()



```c
bool GSM3ShieldV1ServerProvider::getSocketAsServerModemStatus(int s)
```

!!! summary "引数"
	- int `s` Socket 

!!! note "戻り値"
	bool modem status (true if connected) 



### getNewOccupiedSocketAsServer()


Get new occupied socket as server 

```c
int GSM3ShieldV1ServerProvider::getNewOccupiedSocketAsServer()
```

!!! note "戻り値"
	int return -1 if no new socket has been occupied 



### connectTCPServer()



```c
int GSM3ShieldV1ServerProvider::connectTCPServer(int port)
```

!!! summary "引数"
	- int `port` TCP port 

!!! note "戻り値"
	int command error if exists 



### ready()


Get last command status 

```c
int GSM3ShieldV1ServerProvider::ready()
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



### getStatusSocketAsServer()



```c
bool GSM3ShieldV1ServerProvider::getStatusSocketAsServer(uint8_t socket)
```

!!! summary "引数"
	- uint8_t `socket` Socket to get status 

!!! note "戻り値"
	bool socket status 



### manageResponse()



```c
void GSM3ShieldV1ServerProvider::manageResponse(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Initial byte of buffer 
	- byte `to` Final byte of buffer 



### recognizeUnsolicitedEvent()



```c
bool GSM3ShieldV1ServerProvider::recognizeUnsolicitedEvent(byte oldTail)
```

!!! summary "引数"
	- byte `oldTail` 

!!! note "戻り値"
	bool true if successful 



