# GSM3ShieldV1CellManagement



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_shield_v1_cell_management.html)

## メンバー

### GSM3ShieldV1CellManagement()


Constructor 
```c
GSM3ShieldV1CellManagement::GSM3ShieldV1CellManagement()
```



### manageResponse()



```c
void GSM3ShieldV1CellManagement::manageResponse(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Initial byte of buffer 
	- byte `to` Final byte of buffer 



### getLocation()


getLocation 

```c
int GSM3ShieldV1CellManagement::getLocation(char *country, char *network, char *area, char *cell)
```

!!! summary "引数"
	- char * `country` 
	- char * `network` 
	- char * `area` 
	- char * `cell` 

!!! note "戻り値"
	int current cell location 



### getICCID()


getICCID 
```c
int GSM3ShieldV1CellManagement::getICCID(char *iccid)
```

!!! summary "引数"
	- char * `iccid` 

!!! note "戻り値"
	int



### ready()


Get last command status 

```c
int GSM3ShieldV1CellManagement::ready()
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



