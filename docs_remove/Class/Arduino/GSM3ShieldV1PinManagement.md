# GSM3ShieldV1PinManagement



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_shield_v1_pin_management.html)

## メンバー

### GSM3ShieldV1PinManagement()


Constructor 
```c
GSM3ShieldV1PinManagement::GSM3ShieldV1PinManagement()
```



### begin()


Check modem response and restart it 
```c
void GSM3ShieldV1PinManagement::begin()
```



### isPIN()


Check if PIN lock or PUK lock is activated 

```c
int GSM3ShieldV1PinManagement::isPIN()
```

!!! note "戻り値"
	int 0 if PIN lock is off, 1 if PIN lock is on, -1 if PUK lock is on, -2 if error exists 



### checkPIN()



```c
int GSM3ShieldV1PinManagement::checkPIN(String pin)
```

!!! summary "引数"
	- String `pin` PIN code 

!!! note "戻り値"
	int 0 if is correct, -1 if is incorrect 



### checkPUK()



```c
int GSM3ShieldV1PinManagement::checkPUK(String puk, String pin)
```

!!! summary "引数"
	- String `puk` PUK code 
	- String `pin` New PIN code 

!!! note "戻り値"
	int 0 if successful, otherwise return -1 



### changePIN()



```c
void GSM3ShieldV1PinManagement::changePIN(String old, String pin)
```

!!! summary "引数"
	- String `old` Old PIN code 
	- String `pin` New PIN code 



### switchPIN()



```c
void GSM3ShieldV1PinManagement::switchPIN(String pin)
```

!!! summary "引数"
	- String `pin` PIN code 



### checkReg()


Check if modem was registered in GSM/GPRS network 

```c
int GSM3ShieldV1PinManagement::checkReg()
```

!!! note "戻り値"
	int 0 if modem was registered, 1 if modem was registered in roaming, -1 if error exists 



### getPINUsed()


Return if PIN lock is used 

```c
bool GSM3ShieldV1PinManagement::getPINUsed()
```

!!! note "戻り値"
	bool true if PIN lock is used, otherwise, return false 



### setPINUsed()



```c
void GSM3ShieldV1PinManagement::setPINUsed(bool used)
```

!!! summary "引数"
	- bool `used` New PIN lock status 



