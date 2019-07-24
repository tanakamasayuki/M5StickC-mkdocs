# TembooCoAPIPStack



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_temboo_co_a_p_i_p_stack.html)

## メンバー



### TembooCoAPIPStack()



```c
TembooCoAPIPStack::TembooCoAPIPStack(UDP &udp)
```

!!! summary "引数"
	- UDP& `udp` 



### sendDatagram()



```c
int TembooCoAPIPStack::sendDatagram(IPAddress address, uint16_t port, uint8_t *data, size_t len)
```

!!! summary "引数"
	- IPAddress `address` 
	- uint16_t `port` 
	- uint8_t * `data` 
	- size_t `len` 

!!! note "戻り値"
	int



### recvDatagram()



```c
int TembooCoAPIPStack::recvDatagram(uint8_t *buffer, size_t maxLen, int32_t &count)
```

!!! summary "引数"
	- uint8_t * `buffer` 
	- size_t `maxLen` 
	- int32_t & `count` 

!!! note "戻り値"
	int



### getRemoteAddress()



```c
IPAddress TembooCoAPIPStack::getRemoteAddress()
```

!!! note "戻り値"
	IPAddress



### getRemotePort()



```c
uint16_t TembooCoAPIPStack::getRemotePort()
```

!!! note "戻り値"
	uint16_t



