# BLEServerCallbacks

Callbacks associated with the operation of a BLE server. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_server_callbacks.html)

## メンバー

### ~BLEServerCallbacks()



```c
virtual BLEServerCallbacks::~BLEServerCallbacks()
```



### onConnect()
Handle a new client connection.

When a new client connects, we are invoked.
```c
void BLEServerCallbacks::onConnect(BLEServer *pServer)
```

!!! summary "引数"
	- BLEServer* `pServer` A reference to the BLE server that received the client connection. 



### onConnect()



```c
void BLEServerCallbacks::onConnect(BLEServer *pServer, esp_ble_gatts_cb_param_t *param)
```

!!! summary "引数"
	- BLEServer* `pServer` 
	- esp_ble_gatts_cb_param_t* `param` 



### onDisconnect()
Handle an existing client disconnection.

When an existing client disconnects, we are invoked.
```c
void BLEServerCallbacks::onDisconnect(BLEServer *pServer)
```

!!! summary "引数"
	- BLEServer* `pServer` A reference to the BLE server that received the existing client disconnection. 



