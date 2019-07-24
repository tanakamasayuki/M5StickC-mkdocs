# CoapRRLayer



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_coap_r_r_layer.html)

## メンバー





### CoapRRLayer()



```c
CoapRRLayer::CoapRRLayer(CoapMessageLayer &messageLayer, uint8_t *rxBuffer, uint16_t rxBufferLen)
```

!!! summary "引数"
	- CoapMessageLayer& `messageLayer` 
	- uint8_t * `rxBuffer` 
	- uint16_t `rxBufferLen` 



### reliableSend()



```c
CoapRRLayer::Result CoapRRLayer::reliableSend(CoapMsg &msg, char *token, IPAddress addr, uint16_t port)
```

!!! summary "引数"
	- CoapMsg& `msg` 
	- char * `token` 
	- IPAddress `addr` 
	- uint16_t `port` 

!!! note "戻り値"
	Result



### send()



```c
Result CoapRRLayer::send(CoapMsg &msg, char *token, IPAddress addr, uint16_t port)
```

!!! summary "引数"
	- CoapMsg& `msg` 
	- char * `token` 
	- IPAddress `addr` 
	- uint16_t `port` 

!!! note "戻り値"
	Result



### loop()



```c
CoapRRLayer::Result CoapRRLayer::loop()
```

!!! note "戻り値"
	Result



### getLastResult()



```c
Result CoapRRLayer::getLastResult()
```

!!! note "戻り値"
	Result



### setState()



```c
void CoapRRLayer::setState(State state)
```

!!! summary "引数"
	- State `state` 



### getRxByteCount()



```c
int16_t CoapRRLayer::getRxByteCount()
```

!!! note "戻り値"
	int16_t



