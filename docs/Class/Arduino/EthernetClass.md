# EthernetClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_ethernet_class.html)

## メンバー







### begin()



```c
int EthernetClass::begin(uint8_t *mac, unsigned long timeout=60000, unsigned long responseTimeout=4000)
```

!!! summary "引数"
	- uint8_t * `mac` 
	- unsigned long `timeout` 
	- unsigned long `responseTimeout` 

!!! note "戻り値"
	int



### maintain()



```c
int EthernetClass::maintain()
```

!!! note "戻り値"
	int



### linkStatus()



```c
EthernetLinkStatus EthernetClass::linkStatus()
```

!!! note "戻り値"
	EthernetLinkStatus



### hardwareStatus()



```c
EthernetHardwareStatus EthernetClass::hardwareStatus()
```

!!! note "戻り値"
	EthernetHardwareStatus



### begin()



```c
void EthernetClass::begin(uint8_t *mac, IPAddress ip)
```

!!! summary "引数"
	- uint8_t * `mac` 
	- IPAddress `ip` 



### begin()



```c
void EthernetClass::begin(uint8_t *mac, IPAddress ip, IPAddress dns)
```

!!! summary "引数"
	- uint8_t * `mac` 
	- IPAddress `ip` 
	- IPAddress `dns` 



### begin()



```c
void EthernetClass::begin(uint8_t *mac, IPAddress ip, IPAddress dns, IPAddress gateway)
```

!!! summary "引数"
	- uint8_t * `mac` 
	- IPAddress `ip` 
	- IPAddress `dns` 
	- IPAddress `gateway` 



### begin()



```c
void EthernetClass::begin(uint8_t *mac, IPAddress ip, IPAddress dns, IPAddress gateway, IPAddress subnet)
```

!!! summary "引数"
	- uint8_t * `mac` 
	- IPAddress `ip` 
	- IPAddress `dns` 
	- IPAddress `gateway` 
	- IPAddress `subnet` 



### init()



```c
void EthernetClass::init(uint8_t sspin=10)
```

!!! summary "引数"
	- uint8_t `sspin` 



### MACAddress()



```c
void EthernetClass::MACAddress(uint8_t *mac_address)
```

!!! summary "引数"
	- uint8_t * `mac_address` 



### localIP()



```c
IPAddress EthernetClass::localIP()
```

!!! note "戻り値"
	IPAddress



### subnetMask()



```c
IPAddress EthernetClass::subnetMask()
```

!!! note "戻り値"
	IPAddress



### gatewayIP()



```c
IPAddress EthernetClass::gatewayIP()
```

!!! note "戻り値"
	IPAddress



### dnsServerIP()



```c
static IPAddress EthernetClass::dnsServerIP()
```

!!! note "戻り値"
	IPAddress



### setMACAddress()



```c
void EthernetClass::setMACAddress(const uint8_t *mac_address)
```

!!! summary "引数"
	- constuint8_t * `mac_address` 



### setLocalIP()



```c
void EthernetClass::setLocalIP(const IPAddress local_ip)
```

!!! summary "引数"
	- const `local_ip` 



### setSubnetMask()



```c
void EthernetClass::setSubnetMask(const IPAddress subnet)
```

!!! summary "引数"
	- const `subnet` 



### setGatewayIP()



```c
void EthernetClass::setGatewayIP(const IPAddress gateway)
```

!!! summary "引数"
	- const `gateway` 



### setDnsServerIP()



```c
void EthernetClass::setDnsServerIP(const IPAddress dns_server)
```

!!! summary "引数"
	- const `dns_server` 



### setRetransmissionTimeout()



```c
void EthernetClass::setRetransmissionTimeout(uint16_t milliseconds)
```

!!! summary "引数"
	- uint16_t `milliseconds` 



### setRetransmissionCount()



```c
void EthernetClass::setRetransmissionCount(uint8_t num)
```

!!! summary "引数"
	- uint8_t `num` 



