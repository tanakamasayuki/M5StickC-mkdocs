# GSM3ShieldV1SMSProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_shield_v1_s_m_s_provider.html)

## メンバー

### GSM3ShieldV1SMSProvider()



```c
GSM3ShieldV1SMSProvider::GSM3ShieldV1SMSProvider()
```



### manageResponse()



```c
void GSM3ShieldV1SMSProvider::manageResponse(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Initial byte of buffer 
	- byte `to` Final byte of buffer 



### beginSMS()



```c
int GSM3ShieldV1SMSProvider::beginSMS(const char *to)
```

!!! summary "引数"
	- constchar * `to` Destination 

!!! note "戻り値"
	int error command if it exists 



### writeSMS()



```c
void GSM3ShieldV1SMSProvider::writeSMS(char c)
```

!!! summary "引数"
	- char `c` Character 



### endSMS()


End SMS 

```c
int GSM3ShieldV1SMSProvider::endSMS()
```

!!! note "戻り値"
	int error command if it exists 



### availableSMS()


Check if SMS available and prepare it to be read 

```c
int GSM3ShieldV1SMSProvider::availableSMS()
```

!!! note "戻り値"
	int number of bytes in a received SMS 



### peekSMS()


Read a byte but do not advance the buffer header (circular buffer) 

```c
int GSM3ShieldV1SMSProvider::peekSMS()
```

!!! note "戻り値"
	int character 



### flushSMS()


Delete the SMS from Modem memory and proccess answer 
```c
void GSM3ShieldV1SMSProvider::flushSMS()
```



### remoteSMSNumber()



```c
int GSM3ShieldV1SMSProvider::remoteSMSNumber(char *number, int nlength)
```

!!! summary "引数"
	- char * `number` Buffer for save number phone 
	- int `nlength` Buffer length 

!!! note "戻り値"
	int 1 success, >1 error 



### readSMS()


Read one char for SMS buffer (advance circular buffer) 

```c
int GSM3ShieldV1SMSProvider::readSMS()
```

!!! note "戻り値"
	int character 



### ready()


Get last command status 

```c
int GSM3ShieldV1SMSProvider::ready()
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



