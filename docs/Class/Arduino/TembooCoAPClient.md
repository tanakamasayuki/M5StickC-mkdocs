# TembooCoAPClient



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_temboo_co_a_p_client.html)

## メンバー





### TembooCoAPClient()



```c
TembooCoAPClient::TembooCoAPClient(TembooCoAPIPStack &ipStack, IPAddress gatewayAddress, uint16_t gatewayPort=DEFAULT_COAP_PORT)
```

!!! summary "引数"
	- TembooCoAPIPStack& `ipStack` 
	- IPAddress `gatewayAddress` 
	- uint16_t `gatewayPort` 



### ~TembooCoAPClient()



```c
TembooCoAPClient::~TembooCoAPClient()
```



### begin()



```c
void TembooCoAPClient::begin(long seed)
```

!!! summary "引数"
	- long `seed` 



### write()



```c
TembooCoAPClient::Result TembooCoAPClient::write(uint8_t value)
```

!!! summary "引数"
	- uint8_t `value` 

!!! note "戻り値"
	Result



### write()



```c
TembooCoAPClient::Result TembooCoAPClient::write(uint8_t *value, uint16_t len)
```

!!! summary "引数"
	- uint8_t * `value` 
	- uint16_t `len` 

!!! note "戻り値"
	Result



### clearData()



```c
void TembooCoAPClient::clearData()
```



### loop()



```c
TembooCoAPClient::Result TembooCoAPClient::loop()
```

!!! note "戻り値"
	Result



### sendChoreoRequest()



```c
TembooCoAPClient::Result TembooCoAPClient::sendChoreoRequest()
```

!!! note "戻り値"
	Result



### getPacketBuffer()



```c
uint8_t* TembooCoAPClient::getPacketBuffer()
```

!!! note "戻り値"
	uint8_t *



### getPacketBufferSize()



```c
int32_t TembooCoAPClient::getPacketBufferSize()
```

!!! note "戻り値"
	int32_t



### getPacketLength()



```c
int32_t TembooCoAPClient::getPacketLength()
```

!!! note "戻り値"
	int32_t



### getRespHttpCode()



```c
int16_t TembooCoAPClient::getRespHttpCode()
```

!!! note "戻り値"
	int16_t



### getState()



```c
State TembooCoAPClient::getState()
```

!!! note "戻り値"
	State



### sendBlockRequest()



```c
TembooCoAPClient::Result TembooCoAPClient::sendBlockRequest(uint16_t msgID, uint32_t blockNum)
```

!!! summary "引数"
	- uint16_t `msgID` 
	- uint32_t `blockNum` 

!!! note "戻り値"
	Result



### resetChoreo()



```c
void TembooCoAPClient::resetChoreo()
```



### getMessageState()



```c
int TembooCoAPClient::getMessageState()
```

!!! note "戻り値"
	int



### requestTime()



```c
Result TembooCoAPClient::requestTime(uint16_t msgID)
```

!!! summary "引数"
	- uint16_t `msgID` 

!!! note "戻り値"
	Result



