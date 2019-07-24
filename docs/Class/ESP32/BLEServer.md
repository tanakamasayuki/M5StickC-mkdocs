# BLEServer

The model of a BLE server. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_server.html)

## メンバー

###  m_appId

```c
uint16_t BLEServer::m_appId
```


### getConnectedCount()
Return the number of connected clients.



```c
uint32_t BLEServer::getConnectedCount()
```

!!! note "戻り値"
	uint32_t The number of connected clients. 



### createService()
Create a BLE Service.


```c
BLEService * BLEServer::createService(const char *uuid)
```

!!! summary "引数"
	- constchar * `uuid` The UUID of the new service. 

!!! note "戻り値"
	BLEService* A reference to the new service object. 



### createService()
Create a BLE Service.


```c
BLEService * BLEServer::createService(BLEUUID uuid, uint32_t numHandles=15, uint8_t inst_id=0)
```

!!! summary "引数"
	- BLEUUID `uuid` The UUID of the new service. 
	- uint32_t `numHandles` The maximum number of handles associated with this service. 
	- uint8_t `inst_id` With multiple services with the same UUID we need to provide inst_id value different for each service. 

!!! note "戻り値"
	BLEService* A reference to the new service object. 



### getAdvertising()
Retrieve the advertising object that can be used to advertise the existence of the server.



```c
BLEAdvertising * BLEServer::getAdvertising()
```

!!! note "戻り値"
	BLEAdvertising* An advertising object. 



### setCallbacks()
Set the server callbacks.

As a BLE server operates, it will generate server level events such as a new client connecting or a previous client disconnecting. This function can be called to register a callback handler that will be invoked when these events are detected.
```c
void BLEServer::setCallbacks(BLEServerCallbacks *pCallbacks)
```

!!! summary "引数"
	- BLEServerCallbacks* `pCallbacks` The callbacks to be invoked. 



### startAdvertising()
Start advertising.

Start the server advertising its existence. This is a convenience function and is equivalent to retrieving the advertising object and invoking start upon it. 
```c
void BLEServer::startAdvertising()
```



### removeService()



```c
void BLEServer::removeService(BLEService *service)
```

!!! summary "引数"
	- BLEService* `service` 



### getServiceByUUID()
Get a BLE Service by its UUID


```c
BLEService * BLEServer::getServiceByUUID(const char *uuid)
```

!!! summary "引数"
	- constchar * `uuid` The UUID of the new service. 

!!! note "戻り値"
	BLEService* A reference to the service object. 



### getServiceByUUID()
Get a BLE Service by its UUID


```c
BLEService * BLEServer::getServiceByUUID(BLEUUID uuid)
```

!!! summary "引数"
	- BLEUUID `uuid` The UUID of the new service. 

!!! note "戻り値"
	BLEService* A reference to the service object. 



### connect()


Allow to connect GATT server to peer device Probably can be used in ANCS for iPhone 
```c
bool BLEServer::connect(BLEAddress address)
```

!!! summary "引数"
	- BLEAddress `address` 

!!! note "戻り値"
	bool



### updateConnParams()


Update connection parameters can be called only after connection has been established 
```c
void BLEServer::updateConnParams(esp_bd_addr_t remote_bda, uint16_t minInterval, uint16_t maxInterval, uint16_t latency, uint16_t timeout)
```

!!! summary "引数"
	- esp_bd_addr_t `remote_bda` 
	- uint16_t `minInterval` 
	- uint16_t `maxInterval` 
	- uint16_t `latency` 
	- uint16_t `timeout` 



### getPeerDevices()



```c
std::map< uint16_t, conn_status_t > BLEServer::getPeerDevices(bool client)
```

!!! summary "引数"
	- bool `client` 

!!! note "戻り値"
	std::map< ,  >



### addPeerDevice()



```c
void BLEServer::addPeerDevice(void *peer, bool is_client, uint16_t conn_id)
```

!!! summary "引数"
	- void * `peer` 
	- bool `is_client` 
	- uint16_t `conn_id` 



### removePeerDevice()



```c
void BLEServer::removePeerDevice(uint16_t conn_id, bool client)
```

!!! summary "引数"
	- uint16_t `conn_id` 
	- bool `client` 



### getServerByConnId()



```c
BLEServer* BLEServer::getServerByConnId(uint16_t conn_id)
```

!!! summary "引数"
	- uint16_t `conn_id` 

!!! note "戻り値"
	BLEServer*



### updatePeerMTU()



```c
void BLEServer::updatePeerMTU(uint16_t connId, uint16_t mtu)
```

!!! summary "引数"
	- uint16_t `connId` 
	- uint16_t `mtu` 



### getPeerMTU()



```c
uint16_t BLEServer::getPeerMTU(uint16_t conn_id)
```

!!! summary "引数"
	- uint16_t `conn_id` 

!!! note "戻り値"
	uint16_t



### getConnId()



```c
uint16_t BLEServer::getConnId()
```

!!! note "戻り値"
	uint16_t



