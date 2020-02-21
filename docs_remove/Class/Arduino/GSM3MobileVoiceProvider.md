# GSM3MobileVoiceProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_mobile_voice_provider.html)

## メンバー

### initialize()



```c
virtual void GSM3MobileVoiceProvider::initialize()
```



### voiceCall()



```c
virtual int GSM3MobileVoiceProvider::voiceCall(const char *number)=0
```

!!! summary "引数"
	- constchar * `number` Phone number to be called 

!!! note "戻り値"
	int If asynchronous, returns 0. If synchronous, 1 if success, other if error 



### answerCall()


Answer a voice call 

```c
virtual int GSM3MobileVoiceProvider::answerCall()=0
```

!!! note "戻り値"
	int If asynchronous, returns 0. If synchronous, 1 if success, other if error 



### hangCall()


Hang a voice call 

```c
virtual int GSM3MobileVoiceProvider::hangCall()=0
```

!!! note "戻り値"
	int If asynchronous, returns 0. If synchronous, 1 if success, other if error 



### retrieveCallingNumber()



```c
virtual int GSM3MobileVoiceProvider::retrieveCallingNumber(char *buffer, int bufsize)=0
```

!!! summary "引数"
	- char * `buffer` Buffer for copy phone number 
	- int `bufsize` Buffer size 

!!! note "戻り値"
	int If asynchronous, returns 0. If synchronous, 1 if success, other if error 



### getvoiceCallStatus()


Returns voice call status 

```c
virtual GSM3_voiceCall_st GSM3MobileVoiceProvider::getvoiceCallStatus()=0
```

!!! note "戻り値"
	GSM3_voiceCall_st voice call status 



### setvoiceCallStatus()



```c
virtual void GSM3MobileVoiceProvider::setvoiceCallStatus(GSM3_voiceCall_st status)=0
```

!!! summary "引数"
	- GSM3_voiceCall_st `status` New status for voice call 



### ready()


Get last command status 

```c
virtual int GSM3MobileVoiceProvider::ready()=0
```

!!! note "戻り値"
	int Returns 0 if last command is still executing, 1 success, >1 error 



