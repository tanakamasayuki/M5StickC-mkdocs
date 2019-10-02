# AsyncUDPPacket



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_async_u_d_p_packet.html)

## メンバー

### AsyncUDPPacket()



```c
AsyncUDPPacket::AsyncUDPPacket(AsyncUDP *udp, pbuf *pb, const ip_addr_t *addr, uint16_t port, struct netif *netif)
```

!!! summary "引数"
	- AsyncUDP* `udp` 
	- pbuf* `pb` 
	- const* `addr` 
	- uint16_t `port` 
	- netifstruct  * `netif` 



### ~AsyncUDPPacket()



```c
AsyncUDPPacket::~AsyncUDPPacket()
```



### data()



```c
uint8_t * AsyncUDPPacket::data()
```

!!! note "戻り値"
	uint8_t*



### length()



```c
size_t AsyncUDPPacket::length()
```

!!! note "戻り値"
	size_t



### isBroadcast()



```c
bool AsyncUDPPacket::isBroadcast()
```

!!! note "戻り値"
	bool



### isMulticast()



```c
bool AsyncUDPPacket::isMulticast()
```

!!! note "戻り値"
	bool



### isIPv6()



```c
bool AsyncUDPPacket::isIPv6()
```

!!! note "戻り値"
	bool



### interface()



```c
tcpip_adapter_if_t AsyncUDPPacket::interface()
```

!!! note "戻り値"
	tcpip_adapter_if_t



### localIP()



```c
IPAddress AsyncUDPPacket::localIP()
```

!!! note "戻り値"
	IPAddress



### localIPv6()



```c
IPv6Address AsyncUDPPacket::localIPv6()
```

!!! note "戻り値"
	IPv6Address



### localPort()



```c
uint16_t AsyncUDPPacket::localPort()
```

!!! note "戻り値"
	uint16_t



### remoteIP()



```c
IPAddress AsyncUDPPacket::remoteIP()
```

!!! note "戻り値"
	IPAddress



### remoteIPv6()



```c
IPv6Address AsyncUDPPacket::remoteIPv6()
```

!!! note "戻り値"
	IPv6Address



### remotePort()



```c
uint16_t AsyncUDPPacket::remotePort()
```

!!! note "戻り値"
	uint16_t



### remoteMac()



```c
void AsyncUDPPacket::remoteMac(uint8_t *mac)
```

!!! summary "引数"
	- uint8_t* `mac` 



### send()



```c
size_t AsyncUDPPacket::send(AsyncUDPMessage &message)
```

!!! summary "引数"
	- AsyncUDPMessage& `message` 

!!! note "戻り値"
	size_t



### available()



```c
int AsyncUDPPacket::available()
```

!!! note "戻り値"
	int



### read()



```c
size_t AsyncUDPPacket::read(uint8_t *data, size_t len)
```

!!! summary "引数"
	- uint8_t* `data` 
	- size_t `len` 

!!! note "戻り値"
	size_t



### read()



```c
int AsyncUDPPacket::read()
```

!!! note "戻り値"
	int



### peek()



```c
int AsyncUDPPacket::peek()
```

!!! note "戻り値"
	int



### flush()



```c
void AsyncUDPPacket::flush()
```



### write()



```c
size_t AsyncUDPPacket::write(const uint8_t *data, size_t len)
```

!!! summary "引数"
	- const* `data` 
	- size_t `len` 

!!! note "戻り値"
	size_t



### write()



```c
size_t AsyncUDPPacket::write(uint8_t data)
```

!!! summary "引数"
	- uint8_t `data` 

!!! note "戻り値"
	size_t



