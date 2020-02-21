# GSM3MobileMockupProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_mobile_mockup_provider.html)

## メンバー

### minSocket()


Minimum socket 

```c
int GSM3MobileMockupProvider::minSocket()
```

!!! note "戻り値"
	int 1 



### maxSocket()


Maximum socket 

```c
int GSM3MobileMockupProvider::maxSocket()
```

!!! note "戻り値"
	int 8 



### GSM3MobileMockupProvider()


Constructor 
```c
GSM3MobileMockupProvider::GSM3MobileMockupProvider()
```



### getStatus()


Get network status 

```c
GSM3_NetworkStatus_t GSM3MobileMockupProvider::getStatus()
```

!!! note "戻り値"
	GSM3_NetworkStatus_t network status 



### getvoiceCallStatus()


Get voice call status 

```c
GSM3_voiceCall_st GSM3MobileMockupProvider::getvoiceCallStatus()
```

!!! note "戻り値"
	GSM3_voiceCall_st call status 



### ready()


Get last command status 

```c
int GSM3MobileMockupProvider::ready()
```

!!! note "戻り値"
	int Returns 0 if last command is still executing, 1 success, >1 error 



### closeCommand()



```c
void GSM3MobileMockupProvider::closeCommand(int code)
```

!!! summary "引数"
	- int `code` Close code 



### begin()



```c
int GSM3MobileMockupProvider::begin(char *pin=0)
```

!!! summary "引数"
	- char * `pin` PIN code 

!!! note "戻り値"
	int 



### isModemAlive()


Check if is modem alive 

```c
int GSM3MobileMockupProvider::isModemAlive()
```

!!! note "戻り値"
	int 0 



### shutdown()


Shutdown the modem (power off really) 

```c
bool GSM3MobileMockupProvider::shutdown()
```

!!! note "戻り値"
	bool true if successful 



### voiceCall()



```c
int GSM3MobileMockupProvider::voiceCall(const char *number)
```

!!! summary "引数"
	- constchar * `number` Phone number to be called 

!!! note "戻り値"
	int If asynchronous, returns 0. If synchronous, 1 if success, other if error 



### answerCall()


Answer a voice call 

```c
int GSM3MobileMockupProvider::answerCall()
```

!!! note "戻り値"
	int If asynchronous, returns 0. If synchronous, 1 if success, other if error 



### hangCall()


Hang a voice call 

```c
int GSM3MobileMockupProvider::hangCall()
```

!!! note "戻り値"
	int If asynchronous, returns 0. If synchronous, 1 if success, other if error 



### retrieveCallingNumber()



```c
int GSM3MobileMockupProvider::retrieveCallingNumber(char *buffer, int *&bufsize)
```

!!! summary "引数"
	- char * `buffer` Buffer for copy phone number 
	- int *& `bufsize` Buffer size 

!!! note "戻り値"
	int If asynchronous, returns 0. If synchronous, 1 if success, other if error 



### beginSMS()



```c
int GSM3MobileMockupProvider::beginSMS(const char *number)
```

!!! summary "引数"
	- constchar * `number` Destination 

!!! note "戻り値"
	int error command if it exists 



### endSMS()


End SMS 

```c
int GSM3MobileMockupProvider::endSMS()
```

!!! note "戻り値"
	int error command if it exists 



### availableSMS()


Check if SMS available and prepare it to be read 

```c
int GSM3MobileMockupProvider::availableSMS()
```

!!! note "戻り値"
	int error command if it exists 



### peek()


Read a byte but do not advance the buffer header (circular buffer) 

```c
int GSM3MobileMockupProvider::peek()
```

!!! note "戻り値"
	int character 



### flushSMS()


Delete the SMS from Modem memory and proccess answer 
```c
void GSM3MobileMockupProvider::flushSMS()
```



### remoteSMSNumber()



```c
int GSM3MobileMockupProvider::remoteSMSNumber(char *number, int nlength)
```

!!! summary "引数"
	- char * `number` Buffer for save number phone 
	- int `nlength` Buffer length 

!!! note "戻り値"
	int 1 success, >1 error 



### readSMS()


Read one char for SMS buffer (advance circular buffer) 

```c
int GSM3MobileMockupProvider::readSMS()
```

!!! note "戻り値"
	int character 



### writeSMS()



```c
void GSM3MobileMockupProvider::writeSMS(char c)
```

!!! summary "引数"
	- char `c` Character 



### connectTCPClient()



```c
int GSM3MobileMockupProvider::connectTCPClient(const char *server, int port, int id_socket)
```

!!! summary "引数"
	- constchar * `server` String with IP or server name 
	- int `port` Remote port number 
	- int `id_socket` Local socket number 

!!! note "戻り値"
	int 0 if command running, 1 if success, otherwise error 



### writeSocket()



```c
void GSM3MobileMockupProvider::writeSocket(const uint8_t *buf, size_t size, int idsocket)
```

!!! summary "引数"
	- constuint8_t * `buf` Buffer 
	- size_t `size` Buffer size 
	- int `idsocket` Socket 



### readSocket()



```c
int GSM3MobileMockupProvider::readSocket(uint8_t *buf, size_t size, int idsocket)
```

!!! summary "引数"
	- uint8_t * `buf` Buffer 
	- size_t `size` Buffer size 
	- int `idsocket` Socket 

!!! note "戻り値"
	int 



### availableSocket()



```c
int GSM3MobileMockupProvider::availableSocket(int idsocket)
```

!!! summary "引数"
	- int `idsocket` Local socket number 

!!! note "戻り値"
	int 0 if command running, 1 if there are data available, 4 if no data, otherwise error 



### readSocket()



```c
int GSM3MobileMockupProvider::readSocket(int idsocket, bool advance=true)
```

!!! summary "引数"
	- int `idsocket` Socket 
	- bool `advance` Determines if advance the buffer head 

!!! note "戻り値"
	int character 



### flushSocket()



```c
void GSM3MobileMockupProvider::flushSocket(int idsocket)
```

!!! summary "引数"
	- int `idsocket` Socket 



### disconnectTCP()



```c
int GSM3MobileMockupProvider::disconnectTCP(int idsocket)
```

!!! summary "引数"
	- int `idsocket` Socket 

!!! note "戻り値"
	int 0 if command running, 1 if success, otherwise error 



### connectTCPServer()



```c
int GSM3MobileMockupProvider::connectTCPServer(int port, char *localIP, int *localIPlength)
```

!!! summary "引数"
	- int `port` Port 
	- char * `localIP` IP address 
	- int * `localIPlength` IP address size in characters 

!!! note "戻り値"
	int command error if exists 



### getSocketModemStatus()



```c
bool GSM3MobileMockupProvider::getSocketModemStatus(uint8_t s)
```

!!! summary "引数"
	- uint8_t `s` Socket 

!!! note "戻り値"
	bool modem status (true if connected) 



