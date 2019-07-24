# SpiDrv



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_spi_drv.html)

## メンバー

### begin()



```c
void SpiDrv::begin()
```



### end()



```c
void SpiDrv::end()
```



### spiDriverInit()



```c
static void SpiDrv::spiDriverInit()
```



### spiSlaveSelect()



```c
void SpiDrv::spiSlaveSelect()
```



### spiSlaveDeselect()



```c
void SpiDrv::spiSlaveDeselect()
```



### spiTransfer()



```c
char SpiDrv::spiTransfer(volatile char data)
```

!!! summary "引数"
	- volatilechar `data` 

!!! note "戻り値"
	char



### waitForSlaveReady()



```c
void SpiDrv::waitForSlaveReady()
```



### waitSpiChar()



```c
int SpiDrv::waitSpiChar(unsigned char waitChar)
```

!!! summary "引数"
	- unsigned char `waitChar` 

!!! note "戻り値"
	int



### readAndCheckChar()



```c
int SpiDrv::readAndCheckChar(char checkChar, char *readChar)
```

!!! summary "引数"
	- char `checkChar` 
	- char * `readChar` 

!!! note "戻り値"
	int



### readChar()



```c
char SpiDrv::readChar()
```

!!! note "戻り値"
	char



### waitResponseParams()



```c
int SpiDrv::waitResponseParams(uint8_t cmd, uint8_t numParam, tParam *params)
```

!!! summary "引数"
	- uint8_t `cmd` 
	- uint8_t `numParam` 
	- tParam* `params` 

!!! note "戻り値"
	int



### waitResponseCmd()



```c
int SpiDrv::waitResponseCmd(uint8_t cmd, uint8_t numParam, uint8_t *param, uint8_t *param_len)
```

!!! summary "引数"
	- uint8_t `cmd` 
	- uint8_t `numParam` 
	- uint8_t * `param` 
	- uint8_t * `param_len` 

!!! note "戻り値"
	int



### waitResponseData8()



```c
int SpiDrv::waitResponseData8(uint8_t cmd, uint8_t *param, uint8_t *param_len)
```

!!! summary "引数"
	- uint8_t `cmd` 
	- uint8_t * `param` 
	- uint8_t * `param_len` 

!!! note "戻り値"
	int



### waitResponseData16()



```c
int SpiDrv::waitResponseData16(uint8_t cmd, uint8_t *param, uint16_t *param_len)
```

!!! summary "引数"
	- uint8_t `cmd` 
	- uint8_t * `param` 
	- uint16_t * `param_len` 

!!! note "戻り値"
	int



### waitResponse()



```c
int SpiDrv::waitResponse(uint8_t cmd, uint8_t *numParamRead, uint8_t **params, uint8_t maxNumParams)
```

!!! summary "引数"
	- uint8_t `cmd` 
	- uint8_t * `numParamRead` 
	- uint8_t ** `params` 
	- uint8_t `maxNumParams` 

!!! note "戻り値"
	int



### sendParam()



```c
void SpiDrv::sendParam(uint8_t *param, uint8_t param_len, uint8_t lastParam=NO_LAST_PARAM)
```

!!! summary "引数"
	- uint8_t * `param` 
	- uint8_t `param_len` 
	- uint8_t `lastParam` 



### sendParamLen8()



```c
void SpiDrv::sendParamLen8(uint8_t param_len)
```

!!! summary "引数"
	- uint8_t `param_len` 



### sendParamLen16()



```c
void SpiDrv::sendParamLen16(uint16_t param_len)
```

!!! summary "引数"
	- uint16_t `param_len` 



### readParamLen8()



```c
uint8_t SpiDrv::readParamLen8(uint8_t *param_len=NULL)
```

!!! summary "引数"
	- uint8_t * `param_len` 

!!! note "戻り値"
	uint8_t



### readParamLen16()



```c
uint16_t SpiDrv::readParamLen16(uint16_t *param_len=NULL)
```

!!! summary "引数"
	- uint16_t * `param_len` 

!!! note "戻り値"
	uint16_t



### sendBuffer()



```c
void SpiDrv::sendBuffer(uint8_t *param, uint16_t param_len, uint8_t lastParam=NO_LAST_PARAM)
```

!!! summary "引数"
	- uint8_t * `param` 
	- uint16_t `param_len` 
	- uint8_t `lastParam` 



### sendParam()



```c
void SpiDrv::sendParam(uint16_t param, uint8_t lastParam=NO_LAST_PARAM)
```

!!! summary "引数"
	- uint16_t `param` 
	- uint8_t `lastParam` 



### sendCmd()



```c
void SpiDrv::sendCmd(uint8_t cmd, uint8_t numParam)
```

!!! summary "引数"
	- uint8_t `cmd` 
	- uint8_t `numParam` 



