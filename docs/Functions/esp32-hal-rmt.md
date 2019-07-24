# 赤外線送受信(RMT)

M5StickCは赤外線送信は標準で可能です。受信をするためには別途受信用センサーを接続する必要があります。

## 利用例

- [Peripherals/赤外線送受信(Remote Control)](../../Peripherals/RMT/)

## メンバー

### rmtInit()


Initialize the object 
```c
rmt_obj_t* rmtInit(int pin, bool tx_not_rx, rmt_reserve_memsize_t memsize)
```

!!! summary "引数"
	- int `pin` 
	- bool `tx_not_rx` 
	- rmt_reserve_memsize_t `memsize` 

!!! note "戻り値"
	rmt_obj_t*



### rmtSetTick()


Sets the clock/divider of timebase the nearest tick to the supplied value in nanoseconds return the real actual tick value in ns 
```c
float rmtSetTick(rmt_obj_t *rmt, float tick)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` 
	- float `tick` 

!!! note "戻り値"
	float



### rmtWrite()


Sending data in one-go mode or continual mode (more data being send while updating buffers in interrupts) 
```c
bool rmtWrite(rmt_obj_t *rmt, rmt_data_t *data, size_t size)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` 
	- rmt_data_t* `data` 
	- size_t `size` 

!!! note "戻り値"
	bool



### rmtReadAsync()


Initiates async receive, event flag indicates data received 
```c
bool rmtReadAsync(rmt_obj_t *rmt, rmt_data_t *data, size_t size, void *eventFlag, bool waitForData, uint32_t timeout)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` 
	- rmt_data_t* `data` 
	- size_t `size` 
	- void * `eventFlag` 
	- bool `waitForData` 
	- uint32_t `timeout` 

!!! note "戻り値"
	bool



### rmtRead()


Initiates async receive with automatic buffering and callback with data from ISR 
```c
bool rmtRead(rmt_obj_t *rmt, rmt_rx_data_cb_t cb)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` 
	- rmt_rx_data_cb_t `cb` 

!!! note "戻り値"
	bool



### rmtBeginReceive()


Start reception 
```c
bool rmtBeginReceive(rmt_obj_t *rmt)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` 

!!! note "戻り値"
	bool



### rmtReceiveCompleted()


Checks if reception completes 
```c
bool rmtReceiveCompleted(rmt_obj_t *rmt)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` 

!!! note "戻り値"
	bool



### rmtReadData()


Reads the data for particular channel 
```c
bool rmtReadData(rmt_obj_t *rmt, uint32_t *data, size_t size)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` 
	- uint32_t * `data` 
	- size_t `size` 

!!! note "戻り値"
	bool



### rmtSetRxThreshold()


Setting threshold for Rx completed 
```c
bool rmtSetRxThreshold(rmt_obj_t *rmt, uint32_t value)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` 
	- uint32_t `value` 

!!! note "戻り値"
	bool



### rmtSetCarrier()


Setting carrier 
```c
bool rmtSetCarrier(rmt_obj_t *rmt, bool carrier_en, bool carrier_level, uint32_t low, uint32_t high)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` 
	- bool `carrier_en` 
	- bool `carrier_level` 
	- uint32_t `low` 
	- uint32_t `high` 

!!! note "戻り値"
	bool



### rmtSetFilter()


Setting input filter 
```c
bool rmtSetFilter(rmt_obj_t *rmt, bool filter_en, uint32_t filter_level)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` 
	- bool `filter_en` 
	- uint32_t `filter_level` 

!!! note "戻り値"
	bool



### rmtDeinit()


Deinitialize the driver 
```c
bool rmtDeinit(rmt_obj_t *rmt)
```

!!! summary "引数"
	- rmt_obj_t* `rmt` 

!!! note "戻り値"
	bool



