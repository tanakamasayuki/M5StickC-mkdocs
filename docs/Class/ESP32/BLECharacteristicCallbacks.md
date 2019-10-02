# BLECharacteristicCallbacks

Callbacks that can be associated with a BLE characteristic to inform of events. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_characteristic_callbacks.html)

## メンバー



### ~BLECharacteristicCallbacks()



```c
BLECharacteristicCallbacks::~BLECharacteristicCallbacks()
```



### onRead()
Callback function to support a read request.


```c
void BLECharacteristicCallbacks::onRead(BLECharacteristic *pCharacteristic)
```

!!! summary "引数"
	- BLECharacteristic* `pCharacteristic` The characteristic that is the source of the event. 



### onWrite()
Callback function to support a write request.


```c
void BLECharacteristicCallbacks::onWrite(BLECharacteristic *pCharacteristic)
```

!!! summary "引数"
	- BLECharacteristic* `pCharacteristic` The characteristic that is the source of the event. 



### onNotify()
Callback function to support a Notify request.


```c
void BLECharacteristicCallbacks::onNotify(BLECharacteristic *pCharacteristic)
```

!!! summary "引数"
	- BLECharacteristic* `pCharacteristic` The characteristic that is the source of the event. 



### onStatus()
Callback function to support a Notify/Indicate Status report.


```c
void BLECharacteristicCallbacks::onStatus(BLECharacteristic *pCharacteristic, Status s, uint32_t code)
```

!!! summary "引数"
	- BLECharacteristic* `pCharacteristic` The characteristic that is the source of the event. 
	- Status `s` Status of the notification/indication 
	- uint32_t `code` Additional code of underlying errors 



