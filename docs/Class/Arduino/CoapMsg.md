# CoapMsg



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_coap_msg.html)

## メンバー









### CoapMsg()



```c
CoapMsg::CoapMsg(uint8_t *buffer, uint16_t bufferLen)
```

!!! summary "引数"
	- uint8_t * `buffer` 
	- uint16_t `bufferLen` 



### CoapMsg()



```c
CoapMsg::CoapMsg(uint8_t *buffer, uint16_t bufferLen, uint16_t packetLen)
```

!!! summary "引数"
	- uint8_t * `buffer` 
	- uint16_t `bufferLen` 
	- uint16_t `packetLen` 



### setType()



```c
void CoapMsg::setType(CoapMsg::Type msgType)
```

!!! summary "引数"
	- CoapMsg::Type `msgType` 



### getType()



```c
CoapMsg::Type CoapMsg::getType()
```

!!! note "戻り値"
	CoapMsg::Type



### setId()



```c
void CoapMsg::setId(uint16_t msgId)
```

!!! summary "引数"
	- uint16_t `msgId` 



### getId()



```c
uint16_t CoapMsg::getId()
```

!!! note "戻り値"
	uint16_t



### setCode()



```c
void CoapMsg::setCode(CoapMsg::Code code)
```

!!! summary "引数"
	- CoapMsg::Code `code` 



### getCode()



```c
CoapMsg::Code CoapMsg::getCode()
```

!!! note "戻り値"
	CoapMsg::Code



### getHTTPStatus()



```c
uint16_t CoapMsg::getHTTPStatus()
```

!!! note "戻り値"
	uint16_t



### setToken()



```c
CoapMsg::Result CoapMsg::setToken(const uint8_t *token, uint8_t tokenLen)
```

!!! summary "引数"
	- constuint8_t * `token` 
	- uint8_t `tokenLen` 

!!! note "戻り値"
	CoapMsg::Result



### getToken()



```c
uint8_t * CoapMsg::getToken()
```

!!! note "戻り値"
	uint8_t *



### getTokenLen()



```c
uint8_t CoapMsg::getTokenLen()
```

!!! note "戻り値"
	uint8_t



### addOption()



```c
CoapMsg::Result CoapMsg::addOption(CoapMsg::Option optionCode, const uint8_t *optionValue, uint16_t optionLen)
```

!!! summary "引数"
	- CoapMsg::Option `optionCode` 
	- constuint8_t * `optionValue` 
	- uint16_t `optionLen` 

!!! note "戻り値"
	CoapMsg::Result



### getOption()



```c
CoapMsg::Result CoapMsg::getOption(CoapMsg::Option optionCode, uint16_t index, uint8_t *&optionValue, uint16_t &optionLen)
```

!!! summary "引数"
	- CoapMsg::Option `optionCode` 
	- uint16_t `index` 
	- uint8_t *& `optionValue` 
	- uint16_t & `optionLen` 

!!! note "戻り値"
	CoapMsg::Result



### getOptionCount()



```c
uint16_t CoapMsg::getOptionCount(CoapMsg::Option optionCode)
```

!!! summary "引数"
	- CoapMsg::Option `optionCode` 

!!! note "戻り値"
	uint16_t



### getOptionLen()



```c
uint16_t CoapMsg::getOptionLen(CoapMsg::Option optionCode, uint16_t index)
```

!!! summary "引数"
	- CoapMsg::Option `optionCode` 
	- uint16_t `index` 

!!! note "戻り値"
	uint16_t



### getOptionValue()



```c
uint8_t * CoapMsg::getOptionValue(CoapMsg::Option optionCode, uint16_t index)
```

!!! summary "引数"
	- CoapMsg::Option `optionCode` 
	- uint16_t `index` 

!!! note "戻り値"
	uint8_t *



### setPayload()



```c
CoapMsg::Result CoapMsg::setPayload(const uint8_t *payload, uint16_t payloadLen)
```

!!! summary "引数"
	- constuint8_t * `payload` 
	- uint16_t `payloadLen` 

!!! note "戻り値"
	CoapMsg::Result



### getPayload()



```c
uint8_t * CoapMsg::getPayload()
```

!!! note "戻り値"
	uint8_t *



### getPayloadLen()



```c
uint16_t CoapMsg::getPayloadLen()
```

!!! note "戻り値"
	uint16_t



### getMsgBytes()



```c
uint8_t * CoapMsg::getMsgBytes()
```

!!! note "戻り値"
	uint8_t *



### getMsgLen()



```c
uint16_t CoapMsg::getMsgLen()
```

!!! note "戻り値"
	uint16_t



### isValid()



```c
bool CoapMsg::isValid()
```

!!! note "戻り値"
	bool



### getBlock1Size()



```c
uint16_t CoapMsg::getBlock1Size()
```

!!! note "戻り値"
	uint16_t



### getBlock1Num()



```c
uint32_t CoapMsg::getBlock1Num()
```

!!! note "戻り値"
	uint32_t



### getBlock1More()



```c
bool CoapMsg::getBlock1More()
```

!!! note "戻り値"
	bool



### getBlock2Size()



```c
uint16_t CoapMsg::getBlock2Size()
```

!!! note "戻り値"
	uint16_t



### getBlock2Num()



```c
uint32_t CoapMsg::getBlock2Num()
```

!!! note "戻り値"
	uint32_t



### getBlock2More()



```c
bool CoapMsg::getBlock2More()
```

!!! note "戻り値"
	bool



### convertToReset()


Convert this (existing received) message into a reset message. 
```c
void CoapMsg::convertToReset()
```



### convertToEmptyAck()



```c
void CoapMsg::convertToEmptyAck()
```



