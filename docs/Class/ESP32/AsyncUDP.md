# AsyncUDP



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_async_u_d_p.html)

## メンバー

### AsyncUDP()



```c
AsyncUDP::AsyncUDP()
```



### ~AsyncUDP()



```c
AsyncUDP::~AsyncUDP()
```



### onPacket()



```c
void AsyncUDP::onPacket(AuPacketHandlerFunctionWithArg cb, void *arg=NULL)
```

!!! summary "引数"
	- AuPacketHandlerFunctionWithArg `cb` 
	- void * `arg` 



### onPacket()



```c
void AsyncUDP::onPacket(AuPacketHandlerFunction cb)
```

!!! summary "引数"
	- AuPacketHandlerFunction `cb` 



### listen()



```c
bool AsyncUDP::listen(const ip_addr_t *addr, uint16_t port)
```

!!! summary "引数"
	- const* `addr` 
	- uint16_t `port` 

!!! note "戻り値"
	bool



### listen()



```c
bool AsyncUDP::listen(const IPAddress addr, uint16_t port)
```

!!! summary "引数"
	- const `addr` 
	- uint16_t `port` 

!!! note "戻り値"
	bool



### listen()



```c
bool AsyncUDP::listen(const IPv6Address addr, uint16_t port)
```

!!! summary "引数"
	- const `addr` 
	- uint16_t `port` 

!!! note "戻り値"
	bool



### listen()



```c
bool AsyncUDP::listen(uint16_t port)
```

!!! summary "引数"
	- uint16_t `port` 

!!! note "戻り値"
	bool



### listenMulticast()



```c
bool AsyncUDP::listenMulticast(const ip_addr_t *addr, uint16_t port, uint8_t ttl=1, tcpip_adapter_if_t tcpip_if=TCPIP_ADAPTER_IF_MAX)
```

!!! summary "引数"
	- const* `addr` 
	- uint16_t `port` 
	- uint8_t `ttl` 
	- tcpip_adapter_if_t `tcpip_if` 

!!! note "戻り値"
	bool



### listenMulticast()



```c
bool AsyncUDP::listenMulticast(const IPAddress addr, uint16_t port, uint8_t ttl=1, tcpip_adapter_if_t tcpip_if=TCPIP_ADAPTER_IF_MAX)
```

!!! summary "引数"
	- const `addr` 
	- uint16_t `port` 
	- uint8_t `ttl` 
	- tcpip_adapter_if_t `tcpip_if` 

!!! note "戻り値"
	bool



### listenMulticast()



```c
bool AsyncUDP::listenMulticast(const IPv6Address addr, uint16_t port, uint8_t ttl=1, tcpip_adapter_if_t tcpip_if=TCPIP_ADAPTER_IF_MAX)
```

!!! summary "引数"
	- const `addr` 
	- uint16_t `port` 
	- uint8_t `ttl` 
	- tcpip_adapter_if_t `tcpip_if` 

!!! note "戻り値"
	bool



### connect()



```c
bool AsyncUDP::connect(const ip_addr_t *addr, uint16_t port)
```

!!! summary "引数"
	- const* `addr` 
	- uint16_t `port` 

!!! note "戻り値"
	bool



### connect()



```c
bool AsyncUDP::connect(const IPAddress addr, uint16_t port)
```

!!! summary "引数"
	- const `addr` 
	- uint16_t `port` 

!!! note "戻り値"
	bool



### connect()



```c
bool AsyncUDP::connect(const IPv6Address addr, uint16_t port)
```

!!! summary "引数"
	- const `addr` 
	- uint16_t `port` 

!!! note "戻り値"
	bool



### close()



```c
void AsyncUDP::close()
```



### writeTo()



```c
size_t AsyncUDP::writeTo(const uint8_t *data, size_t len, const ip_addr_t *addr, uint16_t port, tcpip_adapter_if_t tcpip_if=TCPIP_ADAPTER_IF_MAX)
```

!!! summary "引数"
	- const* `data` 
	- size_t `len` 
	- const* `addr` 
	- uint16_t `port` 
	- tcpip_adapter_if_t `tcpip_if` 

!!! note "戻り値"
	size_t



### writeTo()



```c
size_t AsyncUDP::writeTo(const uint8_t *data, size_t len, const IPAddress addr, uint16_t port, tcpip_adapter_if_t tcpip_if=TCPIP_ADAPTER_IF_MAX)
```

!!! summary "引数"
	- const* `data` 
	- size_t `len` 
	- const `addr` 
	- uint16_t `port` 
	- tcpip_adapter_if_t `tcpip_if` 

!!! note "戻り値"
	size_t



### writeTo()



```c
size_t AsyncUDP::writeTo(const uint8_t *data, size_t len, const IPv6Address addr, uint16_t port, tcpip_adapter_if_t tcpip_if=TCPIP_ADAPTER_IF_MAX)
```

!!! summary "引数"
	- const* `data` 
	- size_t `len` 
	- const `addr` 
	- uint16_t `port` 
	- tcpip_adapter_if_t `tcpip_if` 

!!! note "戻り値"
	size_t



### write()



```c
size_t AsyncUDP::write(const uint8_t *data, size_t len)
```

!!! summary "引数"
	- const* `data` 
	- size_t `len` 

!!! note "戻り値"
	size_t



### write()



```c
size_t AsyncUDP::write(uint8_t data)
```

!!! summary "引数"
	- uint8_t `data` 

!!! note "戻り値"
	size_t



### broadcastTo()



```c
size_t AsyncUDP::broadcastTo(uint8_t *data, size_t len, uint16_t port, tcpip_adapter_if_t tcpip_if=TCPIP_ADAPTER_IF_MAX)
```

!!! summary "引数"
	- uint8_t* `data` 
	- size_t `len` 
	- uint16_t `port` 
	- tcpip_adapter_if_t `tcpip_if` 

!!! note "戻り値"
	size_t



### broadcastTo()



```c
size_t AsyncUDP::broadcastTo(const char *data, uint16_t port, tcpip_adapter_if_t tcpip_if=TCPIP_ADAPTER_IF_MAX)
```

!!! summary "引数"
	- constchar * `data` 
	- uint16_t `port` 
	- tcpip_adapter_if_t `tcpip_if` 

!!! note "戻り値"
	size_t



### broadcast()



```c
size_t AsyncUDP::broadcast(uint8_t *data, size_t len)
```

!!! summary "引数"
	- uint8_t* `data` 
	- size_t `len` 

!!! note "戻り値"
	size_t



### broadcast()



```c
size_t AsyncUDP::broadcast(const char *data)
```

!!! summary "引数"
	- constchar * `data` 

!!! note "戻り値"
	size_t



### sendTo()



```c
size_t AsyncUDP::sendTo(AsyncUDPMessage &message, const ip_addr_t *addr, uint16_t port, tcpip_adapter_if_t tcpip_if=TCPIP_ADAPTER_IF_MAX)
```

!!! summary "引数"
	- AsyncUDPMessage& `message` 
	- const* `addr` 
	- uint16_t `port` 
	- tcpip_adapter_if_t `tcpip_if` 

!!! note "戻り値"
	size_t



### sendTo()



```c
size_t AsyncUDP::sendTo(AsyncUDPMessage &message, const IPAddress addr, uint16_t port, tcpip_adapter_if_t tcpip_if=TCPIP_ADAPTER_IF_MAX)
```

!!! summary "引数"
	- AsyncUDPMessage& `message` 
	- const `addr` 
	- uint16_t `port` 
	- tcpip_adapter_if_t `tcpip_if` 

!!! note "戻り値"
	size_t



### sendTo()



```c
size_t AsyncUDP::sendTo(AsyncUDPMessage &message, const IPv6Address addr, uint16_t port, tcpip_adapter_if_t tcpip_if=TCPIP_ADAPTER_IF_MAX)
```

!!! summary "引数"
	- AsyncUDPMessage& `message` 
	- const `addr` 
	- uint16_t `port` 
	- tcpip_adapter_if_t `tcpip_if` 

!!! note "戻り値"
	size_t



### send()



```c
size_t AsyncUDP::send(AsyncUDPMessage &message)
```

!!! summary "引数"
	- AsyncUDPMessage& `message` 

!!! note "戻り値"
	size_t



### broadcastTo()



```c
size_t AsyncUDP::broadcastTo(AsyncUDPMessage &message, uint16_t port, tcpip_adapter_if_t tcpip_if=TCPIP_ADAPTER_IF_MAX)
```

!!! summary "引数"
	- AsyncUDPMessage& `message` 
	- uint16_t `port` 
	- tcpip_adapter_if_t `tcpip_if` 

!!! note "戻り値"
	size_t



### broadcast()



```c
size_t AsyncUDP::broadcast(AsyncUDPMessage &message)
```

!!! summary "引数"
	- AsyncUDPMessage& `message` 

!!! note "戻り値"
	size_t



### listenIP()



```c
IPAddress AsyncUDP::listenIP()
```

!!! note "戻り値"
	IPAddress



### listenIPv6()



```c
IPv6Address AsyncUDP::listenIPv6()
```

!!! note "戻り値"
	IPv6Address



### connected()



```c
bool AsyncUDP::connected()
```

!!! note "戻り値"
	bool



### operator bool()



```c
AsyncUDP::operator bool()
```



### _s_recv()



```c
void AsyncUDP::_s_recv(void *arg, udp_pcb *upcb, pbuf *p, const ip_addr_t *addr, uint16_t port, struct netif *netif)
```

!!! summary "引数"
	- void * `arg` 
	- udp_pcb * `upcb` 
	- pbuf* `p` 
	- const* `addr` 
	- uint16_t `port` 
	- netifstruct  * `netif` 



