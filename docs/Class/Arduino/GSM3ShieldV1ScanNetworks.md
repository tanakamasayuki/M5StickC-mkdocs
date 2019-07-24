# GSM3ShieldV1ScanNetworks



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_shield_v1_scan_networks.html)

## メンバー

### GSM3ShieldV1ScanNetworks()



```c
GSM3ShieldV1ScanNetworks::GSM3ShieldV1ScanNetworks(bool trace=false)
```

!!! summary "引数"
	- bool `trace` if true, dumps all AT dialogue to Serial 



### begin()


begin (forces modem hardware restart, so we begin from scratch) 

```c
GSM3_NetworkStatus_t GSM3ShieldV1ScanNetworks::begin()
```

!!! note "戻り値"
	GSM3_NetworkStatus_t Always returns IDLE status 



### getCurrentCarrier()


Read current carrier 

```c
String GSM3ShieldV1ScanNetworks::getCurrentCarrier()
```

!!! note "戻り値"
	String Current carrier 



### getSignalStrength()


Obtain signal strength 

```c
String GSM3ShieldV1ScanNetworks::getSignalStrength()
```

!!! note "戻り値"
	String Signal Strength 



### readNetworks()


Search available carriers 

```c
String GSM3ShieldV1ScanNetworks::readNetworks()
```

!!! note "戻り値"
	String A string with list of networks available 



