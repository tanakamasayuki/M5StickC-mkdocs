# GSM3ShieldV1DataNetworkProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_shield_v1_data_network_provider.html)

## メンバー

### networkAttach()



```c
GSM3_NetworkStatus_t GSM3ShieldV1DataNetworkProvider::networkAttach(char *networkId, char *user, char *pass)
```

!!! summary "引数"
	- char * `networkId` APN GPRS 
	- char * `user` Username 
	- char * `pass` Password 

!!! note "戻り値"
	GSM3_NetworkStatus_t connection status 



### networkDetach()


Detach GPRS/GSM network 

```c
GSM3_NetworkStatus_t GSM3ShieldV1DataNetworkProvider::networkDetach()
```

!!! note "戻り値"
	GSM3_NetworkStatus_t connection status 



### attachGPRS()



```c
GSM3_NetworkStatus_t GSM3ShieldV1DataNetworkProvider::attachGPRS(char *apn, char *user_name, char *password, bool synchronous=true)
```

!!! summary "引数"
	- char * `apn` APN GPRS 
	- char * `user_name` Username 
	- char * `password` Password 
	- bool `synchronous` Sync mode 

!!! note "戻り値"
	GSM3_NetworkStatus_t connection status 



### detachGPRS()



```c
GSM3_NetworkStatus_t GSM3ShieldV1DataNetworkProvider::detachGPRS(bool synchronous=true)
```

!!! summary "引数"
	- bool `synchronous` Sync mode 

!!! note "戻り値"
	GSM3_NetworkStatus_t connection status 



### ready()


Returns 0 if last command is still executing 

```c
int GSM3ShieldV1DataNetworkProvider::ready()
```

!!! note "戻り値"
	int 1 if success, >1 if error 



### getStatus()


Get network status (connection) 

```c
GSM3_NetworkStatus_t GSM3ShieldV1DataNetworkProvider::getStatus()
```

!!! note "戻り値"
	GSM3_NetworkStatus_t status 



### getIP()



```c
int GSM3ShieldV1DataNetworkProvider::getIP(char *LocalIP, int LocalIPlength)
```

!!! summary "引数"
	- char * `LocalIP` Buffer for copy IP address 
	- int `LocalIPlength` Buffer length 

!!! note "戻り値"
	int command error if exists 



### getIPAddress()


Get actual assigned IP address in  format 

```c
IPAddress GSM3ShieldV1DataNetworkProvider::getIPAddress()
```

!!! note "戻り値"
	IPAddress IP address in  format 



### manageResponse()



```c
void GSM3ShieldV1DataNetworkProvider::manageResponse(byte from, byte to)
```

!!! summary "引数"
	- byte `from` Initial byte of buffer 
	- byte `to` Final byte of buffer 



