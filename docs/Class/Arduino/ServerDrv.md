# ServerDrv



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_server_drv.html)

## メンバー

### startServer()



```c
void ServerDrv::startServer(uint16_t port, uint8_t sock, uint8_t protMode=TCP_MODE)
```

!!! summary "引数"
	- uint16_t `port` 
	- uint8_t `sock` 
	- uint8_t `protMode` 



### startClient()



```c
void ServerDrv::startClient(uint32_t ipAddress, uint16_t port, uint8_t sock, uint8_t protMode=TCP_MODE)
```

!!! summary "引数"
	- uint32_t `ipAddress` 
	- uint16_t `port` 
	- uint8_t `sock` 
	- uint8_t `protMode` 



### stopClient()



```c
void ServerDrv::stopClient(uint8_t sock)
```

!!! summary "引数"
	- uint8_t `sock` 



### getServerState()



```c
uint8_t ServerDrv::getServerState(uint8_t sock)
```

!!! summary "引数"
	- uint8_t `sock` 

!!! note "戻り値"
	uint8_t



### getClientState()



```c
uint8_t ServerDrv::getClientState(uint8_t sock)
```

!!! summary "引数"
	- uint8_t `sock` 

!!! note "戻り値"
	uint8_t



### getData()



```c
bool ServerDrv::getData(uint8_t sock, uint8_t *data, uint8_t peek=0)
```

!!! summary "引数"
	- uint8_t `sock` 
	- uint8_t * `data` 
	- uint8_t `peek` 

!!! note "戻り値"
	bool



### getDataBuf()



```c
bool ServerDrv::getDataBuf(uint8_t sock, uint8_t *data, uint16_t *len)
```

!!! summary "引数"
	- uint8_t `sock` 
	- uint8_t * `data` 
	- uint16_t * `len` 

!!! note "戻り値"
	bool



### insertDataBuf()



```c
bool ServerDrv::insertDataBuf(uint8_t sock, const uint8_t *_data, uint16_t _dataLen)
```

!!! summary "引数"
	- uint8_t `sock` 
	- constuint8_t * `_data` 
	- uint16_t `_dataLen` 

!!! note "戻り値"
	bool



### sendData()



```c
bool ServerDrv::sendData(uint8_t sock, const uint8_t *data, uint16_t len)
```

!!! summary "引数"
	- uint8_t `sock` 
	- constuint8_t * `data` 
	- uint16_t `len` 

!!! note "戻り値"
	bool



### sendUdpData()



```c
bool ServerDrv::sendUdpData(uint8_t sock)
```

!!! summary "引数"
	- uint8_t `sock` 

!!! note "戻り値"
	bool



### availData()



```c
uint16_t ServerDrv::availData(uint8_t sock)
```

!!! summary "引数"
	- uint8_t `sock` 

!!! note "戻り値"
	uint16_t



### checkDataSent()



```c
uint8_t ServerDrv::checkDataSent(uint8_t sock)
```

!!! summary "引数"
	- uint8_t `sock` 

!!! note "戻り値"
	uint8_t



