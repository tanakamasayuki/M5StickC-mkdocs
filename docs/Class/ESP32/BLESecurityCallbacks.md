# BLESecurityCallbacks



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_b_l_e_security_callbacks.html)

## メンバー

### ~BLESecurityCallbacks()



```c
virtual BLESecurityCallbacks::~BLESecurityCallbacks()
```



### onPassKeyRequest()
Its request from peer device to input authentication pin code displayed on peer device. It requires that our device is capable to input 6-digits code by end user



```c
virtual uint32_t BLESecurityCallbacks::onPassKeyRequest()=0
```

!!! note "戻り値"
	uint32_t Return 6-digits integer value from input device 



### onPassKeyNotify()
Provide us 6-digits code to perform authentication. It requires that our device is capable to display this code to end user


```c
virtual void BLESecurityCallbacks::onPassKeyNotify(uint32_t pass_key)=0
```

!!! summary "引数"
	- uint32_t `pass_key` 



### onSecurityRequest()
Here we can make decision if we want to let negotiate authorization with peer device or not return Return true if we accept this peer device request


```c
virtual bool BLESecurityCallbacks::onSecurityRequest()=0
```

!!! note "戻り値"
	bool



### onAuthenticationComplete()


Provide us information when authentication process is completed 
```c
virtual void BLESecurityCallbacks::onAuthenticationComplete(esp_ble_auth_cmpl_t)=0
```

!!! summary "引数"
	- esp_ble_auth_cmpl_t `` 



### onConfirmPIN()



```c
virtual bool BLESecurityCallbacks::onConfirmPIN(uint32_t pin)=0
```

!!! summary "引数"
	- uint32_t `pin` 

!!! note "戻り値"
	bool



