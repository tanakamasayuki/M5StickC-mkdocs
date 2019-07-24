# GSM3SMSService



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_s_m_s_service.html)

## メンバー

### GSM3SMSService()



```c
GSM3SMSService::GSM3SMSService(bool synch=true)
```

!!! summary "引数"
	- bool `synch` Determines sync mode 



### write()



```c
size_t GSM3SMSService::write(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` Character 

!!! note "戻り値"
	size_t size 



### beginSMS()



```c
int GSM3SMSService::beginSMS(const char *to)
```

!!! summary "引数"
	- constchar * `to` Destination 

!!! note "戻り値"
	int error command if it exists 



### ready()


Get last command status 

```c
int GSM3SMSService::ready()
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



### endSMS()


End SMS 

```c
int GSM3SMSService::endSMS()
```

!!! note "戻り値"
	int error command if it exists 



### available()


Check if SMS available and prepare it to be read 

```c
int GSM3SMSService::available()
```

!!! note "戻り値"
	int number of bytes in a received SMS 



### remoteNumber()



```c
int GSM3SMSService::remoteNumber(char *number, int nlength)
```

!!! summary "引数"
	- char * `number` Buffer for save number phone 
	- int `nlength` Buffer length 

!!! note "戻り値"
	int 1 success, >1 error 



### read()


Read one char for SMS buffer (advance circular buffer) 

```c
int GSM3SMSService::read()
```

!!! note "戻り値"
	int byte 



### peek()


Read a byte but do not advance the buffer header (circular buffer) 

```c
int GSM3SMSService::peek()
```

!!! note "戻り値"
	int byte 



### flush()


Delete the SMS from Modem memory and proccess answer 
```c
void GSM3SMSService::flush()
```



