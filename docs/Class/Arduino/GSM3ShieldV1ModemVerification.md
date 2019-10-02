# GSM3ShieldV1ModemVerification



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_shield_v1_modem_verification.html)

## メンバー

### GSM3ShieldV1ModemVerification()


Constructor 
```c
GSM3ShieldV1ModemVerification::GSM3ShieldV1ModemVerification()
```



### begin()


Check modem response and restart it 
```c
int GSM3ShieldV1ModemVerification::begin()
```

!!! note "戻り値"
	int



### getIMEI()


Obtain modem IMEI (command AT) 

```c
String GSM3ShieldV1ModemVerification::getIMEI()
```

!!! note "戻り値"
	String modem IMEI number 



