# BLEScan

Perform and manage BLE scans. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_scan.html)

## メンバー

### setActiveScan()
Should we perform an active or passive scan? The default is a passive scan. An active scan means that we will wish a scan response.


```c
void BLEScan::setActiveScan(bool active)
```

!!! summary "引数"
	- bool `active` If true, we perform an active scan otherwise a passive scan. 



### setAdvertisedDeviceCallbacks()
Set the call backs to be invoked.


```c
void BLEScan::setAdvertisedDeviceCallbacks(BLEAdvertisedDeviceCallbacks *pAdvertisedDeviceCallbacks, bool wantDuplicates=false)
```

!!! summary "引数"
	- BLEAdvertisedDeviceCallbacks* `pAdvertisedDeviceCallbacks` Call backs to be invoked. 
	- bool `wantDuplicates` True if we wish to be called back with duplicates. Default is false. 



### setInterval()
Set the interval to scan.


```c
void BLEScan::setInterval(uint16_t intervalMSecs)
```

!!! summary "引数"
	- uint16_t `intervalMSecs` 



### setWindow()
Set the window to actively scan.


```c
void BLEScan::setWindow(uint16_t windowMSecs)
```

!!! summary "引数"
	- uint16_t `windowMSecs` How long to actively scan. 



### start()
Start scanning.


```c
bool BLEScan::start(uint32_t duration, void(*scanCompleteCB)(BLEScanResults), bool is_continue=false)
```

!!! summary "引数"
	- uint32_t `duration` The duration in seconds for which to scan. 
	- BLEScanResultsvoid(*)() `scanCompleteCB` A function to be called when scanning has completed. 
	- bool `is_continue` 

!!! note "戻り値"
	bool True if scan started or false if there was an error. 



### start()
Start scanning and block until scanning has been completed.


```c
BLEScanResults BLEScan::start(uint32_t duration, bool is_continue=false)
```

!!! summary "引数"
	- uint32_t `duration` The duration in seconds for which to scan. 
	- bool `is_continue` 

!!! note "戻り値"
	BLEScanResults The . 



### stop()
Stop an in progress scan.



```c
void BLEScan::stop()
```



### erase()



```c
void BLEScan::erase(BLEAddress address)
```

!!! summary "引数"
	- BLEAddress `address` 



### getResults()



```c
BLEScanResults BLEScan::getResults()
```

!!! note "戻り値"
	BLEScanResults



### clearResults()



```c
void BLEScan::clearResults()
```



