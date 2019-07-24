# GSM3ShieldV1BandManagement



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_g_s_m3_shield_v1_band_management.html)

## メンバー

### GSM3ShieldV1BandManagement()



```c
GSM3ShieldV1BandManagement::GSM3ShieldV1BandManagement(bool trace=false)
```

!!! summary "引数"
	- bool `trace` If true, dumps all AT dialogue to Serial 



### begin()


Forces modem hardware restart, so we begin from scratch 

```c
GSM3_NetworkStatus_t GSM3ShieldV1BandManagement::begin()
```

!!! note "戻り値"
	GSM3_NetworkStatus_t always returns IDLE status 



### getBand()


Get current modem work band 

```c
String GSM3ShieldV1BandManagement::getBand()
```

!!! note "戻り値"
	String current modem work band 



### setBand()



```c
bool GSM3ShieldV1BandManagement::setBand(String band)
```

!!! summary "引数"
	- String `band` Desired new band 

!!! note "戻り値"
	bool true if success, false otherwise 



