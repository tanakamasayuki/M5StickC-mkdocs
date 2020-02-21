# GSM3VoiceCallService



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_voice_call_service.html)

## メンバー

### GSM3VoiceCallService()



```c
GSM3VoiceCallService::GSM3VoiceCallService(bool synch=true)
```

!!! summary "引数"
	- bool `synch` If true, the service calls are synchronois 



### getvoiceCallStatus()


Voice call status 

```c
GSM3_voiceCall_st GSM3VoiceCallService::getvoiceCallStatus()
```

!!! note "戻り値"
	GSM3_voiceCall_st Status of the voice call, as described in  { IDLE_CALL, CALLING, RECEIVINGCALL, TALKING}; 



### ready()


Get last command status 

```c
int GSM3VoiceCallService::ready()
```

!!! note "戻り値"
	int Returns 0 if last command is still executing, 1 success, >1 error 



### voiceCall()



```c
int GSM3VoiceCallService::voiceCall(const char *to, unsigned long timeout=30000)
```

!!! summary "引数"
	- constchar * `to` Receiver number. Country extension can be used or not. Char buffer should not be released or used until command is over 
	- unsigned long `timeout` In millisecods. Time ringing before closing the call. Only used in synchronous mode. If zero, ring undefinitely 

!!! note "戻り値"
	int In asynchronous mode returns 0 if last command is still executing, 1 success, >1 error In synchronous mode returns 1 if the call is placed, 0 if not. 



### answerCall()


Accept an incoming voice call 

```c
int GSM3VoiceCallService::answerCall()
```

!!! note "戻り値"
	int In asynchronous mode returns 0 if last command is still executing, 1 success, >1 error In synchronous mode returns 1 if the call is answered, 0 if not. 



### hangCall()


Hang a stablished call or an incoming ring 

```c
int GSM3VoiceCallService::hangCall()
```

!!! note "戻り値"
	int In asynchronous mode returns 0 if last command is still executing, 1 success, >1 error In synchronous mode returns 1 if the call is answered, 0 if not. 



### retrieveCallingNumber()



```c
int GSM3VoiceCallService::retrieveCallingNumber(char *buffer, int bufsize)
```

!!! summary "引数"
	- char * `buffer` pointer to the buffer memory 
	- int `bufsize` size of available memory area, at least should be 10 characters 

!!! note "戻り値"
	int In asynchronous mode returns 0 if last command is still executing, 1 success, >1 error In synchronous mode returns 1 if the number is correcty taken 0 if not 



