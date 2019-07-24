# BLEScanResults

The result of having performed a scan. When a scan completes, we have a set of found devices. Each device is described by a  object. The number of items in the set is given by . We can retrieve a device by calling  passing in the index (starting at 0) of the desired device. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_b_l_e_scan_results.html)

## メンバー

### dump()
Dump the scan results to the log.


```c
void BLEScanResults::dump()
```



### getCount()
Return the count of devices found in the last scan.



```c
int BLEScanResults::getCount()
```

!!! note "戻り値"
	int The number of devices found in the last scan. 



### getDevice()
Return the specified device at the given index. The index should be between 0 and -1.


```c
BLEAdvertisedDevice BLEScanResults::getDevice(uint32_t i)
```

!!! summary "引数"
	- uint32_t `i` The index of the device. 

!!! note "戻り値"
	BLEAdvertisedDevice The device at the specified index. 



