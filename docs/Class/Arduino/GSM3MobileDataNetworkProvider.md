# GSM3MobileDataNetworkProvider



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_mobile_data_network_provider.html)

## メンバー

### networkAttach()



```c
virtual GSM3_NetworkStatus_t GSM3MobileDataNetworkProvider::networkAttach(char *networId, char *user, char *pass)=0
```

!!! summary "引数"
	- char * `networId` 
	- char * `user` Username 
	- char * `pass` Password 

!!! note "戻り値"
	GSM3_NetworkStatus_t connection status 



### networkDetach()


Detach GPRS/GSM network 

```c
virtual GSM3_NetworkStatus_t GSM3MobileDataNetworkProvider::networkDetach()=0
```

!!! note "戻り値"
	GSM3_NetworkStatus_t connection status 



