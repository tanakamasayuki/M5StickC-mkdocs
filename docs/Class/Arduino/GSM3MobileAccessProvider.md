# GSM3MobileAccessProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_mobile_access_provider.html)

## メンバー

### begin()



```c
virtual GSM3_NetworkStatus_t GSM3MobileAccessProvider::begin(char *pin=0, bool restart=true, bool synchronous=true)=0
```

!!! summary "引数"
	- char * `pin` PIN code 
	- bool `restart` Determines if hardware restart 
	- bool `synchronous` Determines sync mode 

!!! note "戻り値"
	GSM3_NetworkStatus_t If synchronous, GSM3_NetworkStatus_t. If asynchronous, returns 0. 



### isAccessAlive()


Check network access status 

```c
virtual int GSM3MobileAccessProvider::isAccessAlive()=0
```

!!! note "戻り値"
	int 1 if Alive, 0 if down 



### shutdown()


Shutdown the modem (power off really) 

```c
virtual bool GSM3MobileAccessProvider::shutdown()=0
```

!!! note "戻り値"
	bool true if successful 



### secureShutdown()


Secure shutdown the modem (power off really) 

```c
virtual bool GSM3MobileAccessProvider::secureShutdown()=0
```

!!! note "戻り値"
	bool always true 



### ready()


Get last command status 

```c
virtual int GSM3MobileAccessProvider::ready()=0
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



