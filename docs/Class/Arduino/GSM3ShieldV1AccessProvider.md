# GSM3ShieldV1AccessProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_shield_v1_access_provider.html)

## メンバー

### GSM3ShieldV1AccessProvider()



```c
GSM3ShieldV1AccessProvider::GSM3ShieldV1AccessProvider(bool debug=false)
```

!!! summary "引数"
	- bool `debug` Determines debug mode 



### begin()



```c
GSM3_NetworkStatus_t GSM3ShieldV1AccessProvider::begin(char *pin=0, bool restart=true, bool synchronous=true)
```

!!! summary "引数"
	- char * `pin` SIM PIN number (4 digits in a string, example: "1234"). If NULL the SIM has no configured PIN. 
	- bool `restart` Restart the modem. Default is TRUE. The modem receives a signal through the Ctrl/D7 pin. If it is shut down, it will start-up. If it is running, it will restart. Takes up to 10 seconds 
	- bool `synchronous` If TRUE the call only returns after the Start is complete or fails. If FALSE the call will return inmediately. You have to call repeatedly  until you get a result. Default is TRUE. 

!!! note "戻り値"
	GSM3_NetworkStatus_t If synchronous, GSM3_NetworkStatus_t. If asynchronous, returns 0. 



### isAccessAlive()


Check network access status 

```c
int GSM3ShieldV1AccessProvider::isAccessAlive()
```

!!! note "戻り値"
	int 1 if Alive, 0 if down 



### shutdown()


Shutdown the modem (power off really) 

```c
bool GSM3ShieldV1AccessProvider::shutdown()
```

!!! note "戻り値"
	bool true if successful 



### secureShutdown()


Secure shutdown the modem (power off really) 

```c
bool GSM3ShieldV1AccessProvider::secureShutdown()
```

!!! note "戻り値"
	bool true if successful 



### ready()


Returns 0 if last command is still executing 

```c
int GSM3ShieldV1AccessProvider::ready()
```

!!! note "戻り値"
	int 1 if success, >1 if error 



### getStatus()


Returns modem status 

```c
GSM3_NetworkStatus_t GSM3ShieldV1AccessProvider::getStatus()
```

!!! note "戻り値"
	GSM3_NetworkStatus_t modem network status 



### manageResponse()



```c
void GSM3ShieldV1AccessProvider::manageResponse(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Initial byte of buffer 
	- byte `to` Final byte of buffer 



### HWrestart()


Restart the modem (will shut down if running) 

```c
int GSM3ShieldV1AccessProvider::HWrestart()
```

!!! note "戻り値"
	int 1 if success, >1 if error 



### HWstart()


Start the modem (will not shut down if running) 

```c
int GSM3ShieldV1AccessProvider::HWstart()
```

!!! note "戻り値"
	int 1 if success, >1 if error 



