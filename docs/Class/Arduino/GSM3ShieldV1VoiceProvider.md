# GSM3ShieldV1VoiceProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_shield_v1_voice_provider.html)

## メンバー

### GSM3ShieldV1VoiceProvider()


Constructor 
```c
GSM3ShieldV1VoiceProvider::GSM3ShieldV1VoiceProvider()
```



### initialize()


initilizer, links with modem provider 
```c
void GSM3ShieldV1VoiceProvider::initialize()
```



### manageResponse()



```c
void GSM3ShieldV1VoiceProvider::manageResponse(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Initial byte of buffer 
	- byte `to` Final byte of buffer 



### voiceCall()



```c
int GSM3ShieldV1VoiceProvider::voiceCall(const char *number)
```

!!! summary "引数"
	- constchar * `number` Phone number to be called 

!!! note "戻り値"
	int If asynchronous, returns 0. If synchronous, 1 if success, other if error 



### answerCall()


Answer a voice call 

```c
int GSM3ShieldV1VoiceProvider::answerCall()
```

!!! note "戻り値"
	int If asynchronous, returns 0. If synchronous, 1 if success, other if error 



### hangCall()


Hang a voice call 

```c
int GSM3ShieldV1VoiceProvider::hangCall()
```

!!! note "戻り値"
	int If asynchronous, returns 0. If synchronous, 1 if success, other if error 



### retrieveCallingNumber()



```c
int GSM3ShieldV1VoiceProvider::retrieveCallingNumber(char *buffer, int bufsize)
```

!!! summary "引数"
	- char * `buffer` Buffer for copy phone number 
	- int `bufsize` Buffer size 

!!! note "戻り値"
	int If asynchronous, returns 0. If synchronous, 1 if success, other if error 



### ready()


Get last command status 

```c
int GSM3ShieldV1VoiceProvider::ready()
```

!!! note "戻り値"
	int Returns 0 if last command is still executing, 1 success, >1 error 



### recognizeUnsolicitedEvent()



```c
bool GSM3ShieldV1VoiceProvider::recognizeUnsolicitedEvent(byte oldTail)
```

!!! summary "引数"
	- byte `oldTail` 

!!! note "戻り値"
	bool true if successful 



### getvoiceCallStatus()


Returns voice call status 

```c
GSM3_voiceCall_st GSM3ShieldV1VoiceProvider::getvoiceCallStatus()
```

!!! note "戻り値"
	GSM3_voiceCall_st voice call status 



### setvoiceCallStatus()



```c
void GSM3ShieldV1VoiceProvider::setvoiceCallStatus(GSM3_voiceCall_st status)
```

!!! summary "引数"
	- GSM3_voiceCall_st `status` New status for voice call 



