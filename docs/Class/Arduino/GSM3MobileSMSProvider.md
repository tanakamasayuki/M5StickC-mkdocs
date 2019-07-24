# GSM3MobileSMSProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_mobile_s_m_s_provider.html)

## メンバー

### beginSMS()



```c
virtual int GSM3MobileSMSProvider::beginSMS(const char *to)
```

!!! summary "引数"
	- constchar * `to` Destination 

!!! note "戻り値"
	int error command if it exists 



### writeSMS()



```c
virtual void GSM3MobileSMSProvider::writeSMS(const char c)
```

!!! summary "引数"
	- constchar `c` Character 



### endSMS()


End SMS 

```c
virtual int GSM3MobileSMSProvider::endSMS()
```

!!! note "戻り値"
	int error command if it exists 



### availableSMS()


Check if SMS available and prepare it to be read 

```c
virtual int GSM3MobileSMSProvider::availableSMS()
```

!!! note "戻り値"
	int number of bytes in a received SMS 



### peekSMS()


Read a byte but do not advance the buffer header (circular buffer) 

```c
virtual int GSM3MobileSMSProvider::peekSMS()
```

!!! note "戻り値"
	int character 



### flushSMS()


Delete the SMS from Modem memory and proccess answer 
```c
virtual void GSM3MobileSMSProvider::flushSMS()
```



### remoteSMSNumber()



```c
virtual int GSM3MobileSMSProvider::remoteSMSNumber(char *number, int nlength)
```

!!! summary "引数"
	- char * `number` Buffer for save number phone 
	- int `nlength` Buffer length 

!!! note "戻り値"
	int 1 success, >1 error 



### readSMS()


Read one char for SMS buffer (advance circular buffer) 

```c
virtual int GSM3MobileSMSProvider::readSMS()
```

!!! note "戻り値"
	int character 



### ready()


Get last command status 

```c
virtual int GSM3MobileSMSProvider::ready()=0
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



