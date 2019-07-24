# CoapMessageLayer



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_coap_message_layer.html)

## メンバー





###  ACK_TIMEOUT

```c
const uint32_t CoapMessageLayer::ACK_TIMEOUT
```


###  MAX_ACK_TIMEOUT

```c
const uint32_t CoapMessageLayer::MAX_ACK_TIMEOUT
```


###  MAX_RETRANSMIT

```c
const uint8_t CoapMessageLayer::MAX_RETRANSMIT
```


###  MAX_TRANSMIT_SPAN

```c
const uint32_t CoapMessageLayer::MAX_TRANSMIT_SPAN
```


###  MAX_TRANSMIT_WAIT

```c
const uint32_t CoapMessageLayer::MAX_TRANSMIT_WAIT
```


### CoapMessageLayer()



```c
CoapMessageLayer::CoapMessageLayer(uint8_t *rxBuffer, uint16_t rxLen, TembooCoAPIPStack &ipStack)
```

!!! summary "引数"
	- uint8_t * `rxBuffer` 
	- uint16_t `rxLen` 
	- TembooCoAPIPStack& `ipStack` 



### reliableSend()



```c
CoapMessageLayer::Result CoapMessageLayer::reliableSend(CoapMsg &msg, IPAddress destAddr, uint16_t destPort)
```

!!! summary "引数"
	- CoapMsg& `msg` 
	- IPAddress `destAddr` 
	- uint16_t `destPort` 

!!! note "戻り値"
	Result



### cancelReliableSend()



```c
CoapMessageLayer::Result CoapMessageLayer::cancelReliableSend()
```

!!! note "戻り値"
	Result



### acceptMsg()



```c
CoapMessageLayer::Result CoapMessageLayer::acceptMsg(CoapMsg &msg)
```

!!! summary "引数"
	- CoapMsg& `msg` 

!!! note "戻り値"
	Result



### acceptMsg()



```c
CoapMessageLayer::Result CoapMessageLayer::acceptMsg(CoapMsg &msg, IPAddress addr, uint16_t port)
```

!!! summary "引数"
	- CoapMsg& `msg` 
	- IPAddress `addr` 
	- uint16_t `port` 

!!! note "戻り値"
	Result



### rejectMsg()



```c
CoapMessageLayer::Result CoapMessageLayer::rejectMsg(CoapMsg &msg)
```

!!! summary "引数"
	- CoapMsg& `msg` 

!!! note "戻り値"
	Result



### rejectMsg()



```c
CoapMessageLayer::Result CoapMessageLayer::rejectMsg(CoapMsg &msg, IPAddress addr, uint16_t port)
```

!!! summary "引数"
	- CoapMsg& `msg` 
	- IPAddress `addr` 
	- uint16_t `port` 

!!! note "戻り値"
	Result



### loop()



```c
CoapMessageLayer::Result CoapMessageLayer::loop()
```

!!! note "戻り値"
	Result



### getLastResult()



```c
Result CoapMessageLayer::getLastResult()
```

!!! note "戻り値"
	Result



### getRXByteCount()



```c
uint16_t CoapMessageLayer::getRXByteCount()
```

!!! note "戻り値"
	uint16_t



### setState()



```c
void CoapMessageLayer::setState(State state)
```

!!! summary "引数"
	- State `state` 



