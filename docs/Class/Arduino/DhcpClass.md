# DhcpClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_dhcp_class.html)

## メンバー

### getLocalIp()



```c
IPAddress DhcpClass::getLocalIp()
```

!!! note "戻り値"
	IPAddress



### getSubnetMask()



```c
IPAddress DhcpClass::getSubnetMask()
```

!!! note "戻り値"
	IPAddress



### getGatewayIp()



```c
IPAddress DhcpClass::getGatewayIp()
```

!!! note "戻り値"
	IPAddress



### getDhcpServerIp()



```c
IPAddress DhcpClass::getDhcpServerIp()
```

!!! note "戻り値"
	IPAddress



### getDnsServerIp()



```c
IPAddress DhcpClass::getDnsServerIp()
```

!!! note "戻り値"
	IPAddress



### beginWithDHCP()



```c
int DhcpClass::beginWithDHCP(uint8_t *, unsigned long timeout=60000, unsigned long responseTimeout=4000)
```

!!! summary "引数"
	- uint8_t * `` 
	- unsigned long `timeout` 
	- unsigned long `responseTimeout` 

!!! note "戻り値"
	int



### checkLease()



```c
int DhcpClass::checkLease()
```

!!! note "戻り値"
	int



