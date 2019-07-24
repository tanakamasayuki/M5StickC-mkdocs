# BLEDescriptorCallbacks

Callbacks that can be associated with a BLE descriptors to inform of events. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_descriptor_callbacks.html)

## メンバー

### ~BLEDescriptorCallbacks()



```c
BLEDescriptorCallbacks::~BLEDescriptorCallbacks()
```



### onRead()
Callback function to support a read request.


```c
void BLEDescriptorCallbacks::onRead(BLEDescriptor *pDescriptor)
```

!!! summary "引数"
	- BLEDescriptor* `pDescriptor` The descriptor that is the source of the event. 



### onWrite()
Callback function to support a write request.


```c
void BLEDescriptorCallbacks::onWrite(BLEDescriptor *pDescriptor)
```

!!! summary "引数"
	- BLEDescriptor* `pDescriptor` The descriptor that is the source of the event. 



