# GSM3ShieldV1



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_shield_v1.html)

## メンバー

### GSM3ShieldV1()


Constructor 
```c
GSM3ShieldV1::GSM3ShieldV1(bool debug=false)
```

!!! summary "引数"
	- bool `debug` 



### manageResponse()



```c
void GSM3ShieldV1::manageResponse(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Initial byte of buffer 
	- byte `to` Final byte of buffer 



### ready()


Get last command status 

```c
int GSM3ShieldV1::ready()
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



### genericParse_rsp2()



```c
bool GSM3ShieldV1::genericParse_rsp2(bool &rsp, char *string1, char *string2)
```

!!! summary "引数"
	- bool& `rsp` Returns true if expected response exists 
	- char * `string1` Substring expected in response 
	- char * `string2` Second substring expected in response 

!!! note "戻り値"
	bool true if parsed successful 



### recognizeUnsolicitedEvent()



```c
bool GSM3ShieldV1::recognizeUnsolicitedEvent(byte oldTail)
```

!!! summary "引数"
	- byte `oldTail` 

!!! note "戻り値"
	bool true if successful 



### answerReceived()


Receive answer 

```c
bool GSM3ShieldV1::answerReceived()
```

!!! note "戻り値"
	bool true if successful 



### socketReceived()



```c
bool GSM3ShieldV1::socketReceived(int id_socket)
```

!!! summary "引数"
	- int `id_socket` Socket ID 

!!! note "戻り値"
	bool true if successful 



### update_activeIDsockets()



```c
void GSM3ShieldV1::update_activeIDsockets(bool active, int ID)
```

!!! summary "引数"
	- bool `active` Active sockets 
	- int `ID` Id for update 



### assignIDsocket()



```c
bool GSM3ShieldV1::assignIDsocket(int &ID)
```

!!! summary "引数"
	- int & `ID` Id to assign to socket 

!!! note "戻り値"
	bool true if successful 



### closedDataSocket()


Close data socket 

```c
bool GSM3ShieldV1::closedDataSocket()
```

!!! note "戻り値"
	bool true if successful 



