# GSM3ShieldV1BaseProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_shield_v1_base_provider.html)

## メンバー

### ready()


Get last command status 

```c
int GSM3ShieldV1BaseProvider::ready()
```

!!! note "戻り値"
	int Returns 0 if last command is still executing, 1 success, >1 error 



### prepareAuxLocate()



```c
void GSM3ShieldV1BaseProvider::prepareAuxLocate(PGM_P str, char auxLocate[])
```

!!! summary "引数"
	- PGM_P `str` PROGMEN 
	- char `auxLocate` Buffer where to locate strings 



### manageResponse()



```c
virtual void GSM3ShieldV1BaseProvider::manageResponse(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Initial byte of buffer 
	- byte `to` Final byte of buffer 



### recognizeUnsolicitedEvent()



```c
virtual bool GSM3ShieldV1BaseProvider::recognizeUnsolicitedEvent(byte from)
```

!!! summary "引数"
	- byte `from` 

!!! note "戻り値"
	bool true if successful (default: false) 



