# GSM3ShieldV1DirectModemProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_shield_v1_direct_modem_provider.html)

## メンバー

### GSM3ShieldV1DirectModemProvider()



```c
GSM3ShieldV1DirectModemProvider::GSM3ShieldV1DirectModemProvider(bool trace=false)
```

!!! summary "引数"
	- bool `trace` if true, dumps all AT dialogue to Serial 



### begin()



```c
void GSM3ShieldV1DirectModemProvider::begin()
```



### restartModem()



```c
void GSM3ShieldV1DirectModemProvider::restartModem()
```



### connect()


Enable the debug process. 
```c
void GSM3ShieldV1DirectModemProvider::connect()
```



### disconnect()


Disable the debug process. 
```c
void GSM3ShieldV1DirectModemProvider::disconnect()
```



### write()



```c
size_t GSM3ShieldV1DirectModemProvider::write(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` Character 

!!! note "戻り値"
	size_t size 



### available()


Check for incoming bytes in buffer 

```c
int GSM3ShieldV1DirectModemProvider::available()
```

!!! note "戻り値"
	int 



### read()


Read from circular buffer 

```c
int GSM3ShieldV1DirectModemProvider::read()
```

!!! note "戻り値"
	int character 



### peek()


Read from circular buffer, but do not delete it 

```c
int GSM3ShieldV1DirectModemProvider::peek()
```

!!! note "戻り値"
	int character 



### flush()


Empty circular buffer 
```c
void GSM3ShieldV1DirectModemProvider::flush()
```



### manageResponse()



```c
void GSM3ShieldV1DirectModemProvider::manageResponse(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Initial byte of buffer 
	- byte `to` Final byte of buffer 



### recognizeUnsolicitedEvent()



```c
bool GSM3ShieldV1DirectModemProvider::recognizeUnsolicitedEvent(byte from)
```

!!! summary "引数"
	- byte `from` 

!!! note "戻り値"
	bool true if successful 



### writeModemCommand()



```c
String GSM3ShieldV1DirectModemProvider::writeModemCommand(String command, int delay)
```

!!! summary "引数"
	- String `command` AT command 
	- int `delay` Time to wait for response 

!!! note "戻り値"
	String response from modem 



