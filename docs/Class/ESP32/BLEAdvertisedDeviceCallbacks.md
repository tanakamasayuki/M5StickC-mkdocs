# BLEAdvertisedDeviceCallbacks

A callback handler for callbacks associated device scanning. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_advertised_device_callbacks.html)

## メンバー

### ~BLEAdvertisedDeviceCallbacks()



```c
virtual BLEAdvertisedDeviceCallbacks::~BLEAdvertisedDeviceCallbacks()
```



### onResult()
Called when a new scan result is detected.

As we are scanning, we will find new devices. When found, this call back is invoked with a reference to the device that was found. During any individual scan, a device will only be detected one time. 
```c
virtual void BLEAdvertisedDeviceCallbacks::onResult(BLEAdvertisedDevice advertisedDevice)=0
```

!!! summary "引数"
	- BLEAdvertisedDevice `advertisedDevice` 



