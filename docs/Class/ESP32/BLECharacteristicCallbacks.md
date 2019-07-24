# BLECharacteristicCallbacks

Callbacks that can be associated with a BLE characteristic to inform of events. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_characteristic_callbacks.html)

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



