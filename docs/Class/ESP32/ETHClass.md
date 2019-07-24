# ETHClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_e_t_h_class.html)

## メンバー





### ETHClass()



```c
ETHClass::ETHClass()
```



### ~ETHClass()



```c
ETHClass::~ETHClass()
```



### begin()



```c
bool ETHClass::begin(uint8_t phy_addr=ETH_PHY_ADDR, int power=ETH_PHY_POWER, int mdc=ETH_PHY_MDC, int mdio=ETH_PHY_MDIO, eth_phy_type_t type=ETH_PHY_TYPE, eth_clock_mode_t clk_mode=ETH_CLK_MODE)
```

!!! summary "引数"
	- uint8_t `phy_addr` 
	- int `power` 
	- int `mdc` 
	- int `mdio` 
	- eth_phy_type_t `type` 
	- eth_clock_mode_t `clk_mode` 

!!! note "戻り値"
	bool



### config()



```c
bool ETHClass::config(IPAddress local_ip, IPAddress gateway, IPAddress subnet, IPAddress dns1=(uint32_t) 0x00000000, IPAddress dns2=(uint32_t) 0x00000000)
```

!!! summary "引数"
	- IPAddress `local_ip` 
	- IPAddress `gateway` 
	- IPAddress `subnet` 
	- IPAddress `dns1` 
	- IPAddress `dns2` 

!!! note "戻り値"
	bool



### getHostname()



```c
const char * ETHClass::getHostname()
```

!!! note "戻り値"
	constchar *



### setHostname()



```c
bool ETHClass::setHostname(const char *hostname)
```

!!! summary "引数"
	- constchar * `hostname` 

!!! note "戻り値"
	bool



### fullDuplex()



```c
bool ETHClass::fullDuplex()
```

!!! note "戻り値"
	bool



### linkUp()



```c
bool ETHClass::linkUp()
```

!!! note "戻り値"
	bool



### linkSpeed()



```c
uint8_t ETHClass::linkSpeed()
```

!!! note "戻り値"
	uint8_t



### enableIpV6()



```c
bool ETHClass::enableIpV6()
```

!!! note "戻り値"
	bool



### localIPv6()



```c
IPv6Address ETHClass::localIPv6()
```

!!! note "戻り値"
	IPv6Address



### localIP()



```c
IPAddress ETHClass::localIP()
```

!!! note "戻り値"
	IPAddress



### subnetMask()



```c
IPAddress ETHClass::subnetMask()
```

!!! note "戻り値"
	IPAddress



### gatewayIP()



```c
IPAddress ETHClass::gatewayIP()
```

!!! note "戻り値"
	IPAddress



### dnsIP()



```c
IPAddress ETHClass::dnsIP(uint8_t dns_no=0)
```

!!! summary "引数"
	- uint8_t `dns_no` 

!!! note "戻り値"
	IPAddress



### macAddress()



```c
uint8_t* ETHClass::macAddress(uint8_t *mac)
```

!!! summary "引数"
	- uint8_t* `mac` 

!!! note "戻り値"
	uint8_t*



### macAddress()



```c
String ETHClass::macAddress()
```

!!! note "戻り値"
	String



