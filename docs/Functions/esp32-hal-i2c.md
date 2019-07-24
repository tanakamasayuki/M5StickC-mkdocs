# 低レベルI2C

この関数群を通常使うことはありません。[TwoWire](../../Class/ESP32/TwoWire/)クラスを利用して呼び出してください。

## 利用例

- [Peripherals/I2C](../../Peripherals/I2C/)

## メンバー

### i2cInit()



```c
i2c_t* i2cInit(uint8_t i2c_num, int8_t sda, int8_t scl, uint32_t clk_speed)
```

!!! summary "引数"
	- uint8_t `i2c_num` 
	- int8_t `sda` 
	- int8_t `scl` 
	- uint32_t `clk_speed` 

!!! note "戻り値"
	i2c_t*



### i2cRelease()



```c
void i2cRelease(i2c_t *i2c)
```

!!! summary "引数"
	- i2c_t* `i2c` 

!!! note "戻り値"
	void



### i2cWrite()



```c
i2c_err_t i2cWrite(i2c_t *i2c, uint16_t address, uint8_t *buff, uint16_t size, bool sendStop, uint16_t timeOutMillis)
```

!!! summary "引数"
	- i2c_t* `i2c` 
	- uint16_t `address` 
	- uint8_t * `buff` 
	- uint16_t `size` 
	- bool `sendStop` 
	- uint16_t `timeOutMillis` 

!!! note "戻り値"
	i2c_err_t



### i2cRead()



```c
i2c_err_t i2cRead(i2c_t *i2c, uint16_t address, uint8_t *buff, uint16_t size, bool sendStop, uint16_t timeOutMillis, uint32_t *readCount)
```

!!! summary "引数"
	- i2c_t* `i2c` 
	- uint16_t `address` 
	- uint8_t * `buff` 
	- uint16_t `size` 
	- bool `sendStop` 
	- uint16_t `timeOutMillis` 
	- uint32_t * `readCount` 

!!! note "戻り値"
	i2c_err_t



### i2cFlush()



```c
i2c_err_t i2cFlush(i2c_t *i2c)
```

!!! summary "引数"
	- i2c_t* `i2c` 

!!! note "戻り値"
	i2c_err_t



### i2cSetFrequency()



```c
i2c_err_t i2cSetFrequency(i2c_t *i2c, uint32_t clk_speed)
```

!!! summary "引数"
	- i2c_t* `i2c` 
	- uint32_t `clk_speed` 

!!! note "戻り値"
	i2c_err_t



### i2cGetFrequency()



```c
uint32_t i2cGetFrequency(i2c_t *i2c)
```

!!! summary "引数"
	- i2c_t* `i2c` 

!!! note "戻り値"
	uint32_t



### i2cGetStatus()



```c
uint32_t i2cGetStatus(i2c_t *i2c)
```

!!! summary "引数"
	- i2c_t* `i2c` 

!!! note "戻り値"
	uint32_t



### i2cAttachSCL()



```c
i2c_err_t i2cAttachSCL(i2c_t *i2c, int8_t scl)
```

!!! summary "引数"
	- i2c_t* `i2c` 
	- int8_t `scl` 

!!! note "戻り値"
	i2c_err_t



### i2cDetachSCL()



```c
i2c_err_t i2cDetachSCL(i2c_t *i2c, int8_t scl)
```

!!! summary "引数"
	- i2c_t* `i2c` 
	- int8_t `scl` 

!!! note "戻り値"
	i2c_err_t



### i2cAttachSDA()



```c
i2c_err_t i2cAttachSDA(i2c_t *i2c, int8_t sda)
```

!!! summary "引数"
	- i2c_t* `i2c` 
	- int8_t `sda` 

!!! note "戻り値"
	i2c_err_t



### i2cDetachSDA()



```c
i2c_err_t i2cDetachSDA(i2c_t *i2c, int8_t sda)
```

!!! summary "引数"
	- i2c_t* `i2c` 
	- int8_t `sda` 

!!! note "戻り値"
	i2c_err_t



### i2cProcQueue()



```c
i2c_err_t i2cProcQueue(i2c_t *i2c, uint32_t *readCount, uint16_t timeOutMillis)
```

!!! summary "引数"
	- i2c_t* `i2c` 
	- uint32_t * `readCount` 
	- uint16_t `timeOutMillis` 

!!! note "戻り値"
	i2c_err_t



### i2cAddQueueWrite()



```c
i2c_err_t i2cAddQueueWrite(i2c_t *i2c, uint16_t i2cDeviceAddr, uint8_t *dataPtr, uint16_t dataLen, bool SendStop, EventGroupHandle_t event)
```

!!! summary "引数"
	- i2c_t* `i2c` 
	- uint16_t `i2cDeviceAddr` 
	- uint8_t * `dataPtr` 
	- uint16_t `dataLen` 
	- bool `SendStop` 
	- EventGroupHandle_t `event` 

!!! note "戻り値"
	i2c_err_t



### i2cAddQueueRead()



```c
i2c_err_t i2cAddQueueRead(i2c_t *i2c, uint16_t i2cDeviceAddr, uint8_t *dataPtr, uint16_t dataLen, bool SendStop, EventGroupHandle_t event)
```

!!! summary "引数"
	- i2c_t* `i2c` 
	- uint16_t `i2cDeviceAddr` 
	- uint8_t * `dataPtr` 
	- uint16_t `dataLen` 
	- bool `SendStop` 
	- EventGroupHandle_t `event` 

!!! note "戻り値"
	i2c_err_t



### i2cDebug()



```c
uint32_t i2cDebug(i2c_t *, uint32_t setBits, uint32_t resetBits)
```

!!! summary "引数"
	- i2c_t* `` 
	- uint32_t `setBits` 
	- uint32_t `resetBits` 

!!! note "戻り値"
	uint32_t



