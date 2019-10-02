# GSM3ShieldV1ModemCore



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_shield_v1_modem_core.html)

## メンバー

###  gss

```c
GSM3SoftSerial GSM3ShieldV1ModemCore::gss
```


### GSM3ShieldV1ModemCore()


Constructor 
```c
GSM3ShieldV1ModemCore::GSM3ShieldV1ModemCore()
```



### getPhoneNumber()


Get phone number 

```c
char* GSM3ShieldV1ModemCore::getPhoneNumber()
```

!!! note "戻り値"
	char * phone number 



### setPhoneNumber()



```c
void GSM3ShieldV1ModemCore::setPhoneNumber(char *n)
```

!!! summary "引数"
	- char * `n` Phone number 



### getPort()


Get port used 

```c
int GSM3ShieldV1ModemCore::getPort()
```

!!! note "戻り値"
	int port 



### setPort()



```c
void GSM3ShieldV1ModemCore::setPort(int p)
```

!!! summary "引数"
	- int `p` Port 



### getCommandError()


Get command error 

```c
uint8_t GSM3ShieldV1ModemCore::getCommandError()
```

!!! note "戻り値"
	uint8_t command error 



### setCommandError()



```c
void GSM3ShieldV1ModemCore::setCommandError(uint8_t n)
```

!!! summary "引数"
	- uint8_t `n` Command error 



### getCommandCounter()


Get command counter 

```c
uint8_t GSM3ShieldV1ModemCore::getCommandCounter()
```

!!! note "戻り値"
	uint8_t command counter 



### setCommandCounter()



```c
void GSM3ShieldV1ModemCore::setCommandCounter(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` Initial value 



### getOngoingCommand()


Get ongoing command 

```c
GSM3_commandType_e GSM3ShieldV1ModemCore::getOngoingCommand()
```

!!! note "戻り値"
	GSM3_commandType_e command 



### setOngoingCommand()



```c
void GSM3ShieldV1ModemCore::setOngoingCommand(GSM3_commandType_e c)
```

!!! summary "引数"
	- GSM3_commandType_e `c` New ongoing command 



### openCommand()



```c
void GSM3ShieldV1ModemCore::openCommand(GSM3ShieldV1BaseProvider *activeProvider, GSM3_commandType_e c)
```

!!! summary "引数"
	- GSM3ShieldV1BaseProvider* `activeProvider` Active provider 
	- GSM3_commandType_e `c` Command for open 



### closeCommand()



```c
void GSM3ShieldV1ModemCore::closeCommand(int code)
```

!!! summary "引数"
	- int `code` Close code 



### write()



```c
size_t GSM3ShieldV1ModemCore::write(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` Character 

!!! note "戻り値"
	size_t size 



### writePGM()



```c
size_t GSM3ShieldV1ModemCore::writePGM(PGM_P str, bool CR=true)
```

!!! summary "引数"
	- PGM_P `str` Buffer for write 
	- bool `CR` Carriadge return adding automatically 

!!! note "戻り値"
	size_t size 



### setDebug()



```c
void GSM3ShieldV1ModemCore::setDebug(bool db)
```

!!! summary "引数"
	- bool `db` Boolean that indicates debug on or off 



### genericParse_rsp()



```c
bool GSM3ShieldV1ModemCore::genericParse_rsp(bool &rsp, const char *string=0, const char *string2=0)
```

!!! summary "引数"
	- bool& `rsp` Returns true if expected response exists 
	- constchar * `string` Substring expected in response 
	- constchar * `string2` Second substring expected in response 

!!! note "戻り値"
	bool true if parsed correctly 



### genericCommand_rq()



```c
void GSM3ShieldV1ModemCore::genericCommand_rq(PGM_P str, bool addCR=true)
```

!!! summary "引数"
	- PGM_P `str` Buffer with AT command 
	- bool `addCR` Carriadge return adding automatically 



### genericCommand_rqc()



```c
void GSM3ShieldV1ModemCore::genericCommand_rqc(const char *str, bool addCR=true)
```

!!! summary "引数"
	- constchar * `str` Buffer with AT command 
	- bool `addCR` Carriadge return adding automatically 



### theBuffer()


Returns the circular buffer 

```c
GSM3CircularBuffer& GSM3ShieldV1ModemCore::theBuffer()
```

!!! note "戻り値"
	GSM3CircularBuffer& circular buffer 



### setStatus()



```c
void GSM3ShieldV1ModemCore::setStatus(GSM3_NetworkStatus_t status)
```

!!! summary "引数"
	- GSM3_NetworkStatus_t `status` Network status 



### getStatus()


Returns actual network status 

```c
GSM3_NetworkStatus_t GSM3ShieldV1ModemCore::getStatus()
```

!!! note "戻り値"
	GSM3_NetworkStatus_t network status 



### registerUMProvider()



```c
void GSM3ShieldV1ModemCore::registerUMProvider(GSM3ShieldV1BaseProvider *provider)
```

!!! summary "引数"
	- GSM3ShieldV1BaseProvider* `provider` Pointer to provider able to receive unsolicited messages 



### unRegisterUMProvider()



```c
void GSM3ShieldV1ModemCore::unRegisterUMProvider(GSM3ShieldV1BaseProvider *provider)
```

!!! summary "引数"
	- GSM3ShieldV1BaseProvider* `provider` Pointer to provider able to receive unsolicited messages 



### registerActiveProvider()



```c
void GSM3ShieldV1ModemCore::registerActiveProvider(GSM3ShieldV1BaseProvider *provider)
```

!!! summary "引数"
	- GSM3ShieldV1BaseProvider* `provider` Pointer to provider receiving responses 



### manageMsg()



```c
void GSM3ShieldV1ModemCore::manageMsg(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Starting byte to read 
	- byte `to` Last byte to read 



### manageReceivedData()


If _debugging, this call is assumed to be made out of interrupts Prints incoming info and calls manageMsgNow 
```c
void GSM3ShieldV1ModemCore::manageReceivedData()
```



### takeMilliseconds()


Chronometer. Measure milliseconds from last call 

```c
unsigned long GSM3ShieldV1ModemCore::takeMilliseconds()
```

!!! note "戻り値"
	unsigned long milliseconds from las time function was called 



### delayInsideInterrupt()



```c
void GSM3ShieldV1ModemCore::delayInsideInterrupt(unsigned long milliseconds)
```

!!! summary "引数"
	- unsigned long `milliseconds` Delay time in milliseconds 



