# BLEClientCallbacks

Callbacks associated with a BLE client. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_client_callbacks.html)

## メンバー

### ~BLEClientCallbacks()



```c
virtual BLEClientCallbacks::~BLEClientCallbacks()
```



### onConnect()



```c
virtual void BLEClientCallbacks::onConnect(BLEClient *pClient)=0
```

!!! summary "引数"
	- BLEClient* `pClient` 



### onDisconnect()



```c
virtual void BLEClientCallbacks::onDisconnect(BLEClient *pClient)=0
```

!!! summary "引数"
	- BLEClient* `pClient` 



