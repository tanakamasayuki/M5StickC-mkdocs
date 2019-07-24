# GSM3MobileServerService



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_mobile_server_service.html)

## メンバー

### GSM3MobileServerService()



```c
GSM3MobileServerService::GSM3MobileServerService(uint8_t port, bool synch=true)
```

!!! summary "引数"
	- uint8_t `port` Port 
	- bool `synch` True if the server acts synchronously 



### ready()


Get last command status 

```c
int GSM3MobileServerService::ready()
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



### begin()


Initialize server 
```c
void GSM3MobileServerService::begin()
```



### available()



```c
GSM3MobileClientService GSM3MobileServerService::available(bool synch=true)
```

!!! summary "引数"
	- bool `synch` If true, the returned client is synchronous or blocking. 

!!! note "戻り値"
	GSM3MobileClientService  if successful, else error 



### beginWrite()


Begin write in socket 
```c
void GSM3MobileServerService::beginWrite()
```



### write()



```c
size_t GSM3MobileServerService::write(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` Character 

!!! note "戻り値"
	size_t size 



### write()



```c
size_t GSM3MobileServerService::write(const uint8_t *buf)
```

!!! summary "引数"
	- constuint8_t * `buf` Buffer 

!!! note "戻り値"
	size_t size 



### write()



```c
size_t GSM3MobileServerService::write(const uint8_t *buf, size_t sz)
```

!!! summary "引数"
	- constuint8_t * `buf` Buffer
	- size_t `sz` Buffer size 

!!! note "戻り値"
	size_t size 



### endWrite()


End write in socket 
```c
void GSM3MobileServerService::endWrite()
```



### stop()


Stop server 
```c
void GSM3MobileServerService::stop()
```



