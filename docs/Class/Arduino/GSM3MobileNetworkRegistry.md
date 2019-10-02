# GSM3MobileNetworkRegistry



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_mobile_network_registry.html)

## メンバー

### GSM3MobileNetworkRegistry()


Constructor 
```c
GSM3MobileNetworkRegistry::GSM3MobileNetworkRegistry()
```



### registerMobileNetworkProvider()



```c
void GSM3MobileNetworkRegistry::registerMobileNetworkProvider(GSM3MobileNetworkProvider *provider)
```

!!! summary "引数"
	- GSM3MobileNetworkProvider* `provider` Provider 



### getMobileNetworkProvider()


Returns network provider object pointer 

```c
GSM3MobileNetworkProvider * GSM3MobileNetworkRegistry::getMobileNetworkProvider()
```

!!! note "戻り値"
	GSM3MobileNetworkProvider* mobile network provider 



