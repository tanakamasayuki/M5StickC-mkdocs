# 低レベルUART(uart)

この関数群を通常使うことはありません。[HardwareSerial](../../Class/ESP32/HardwareSerial/)クラスを利用して呼び出してください。

## 利用例

- [Peripherals/シリアル通信(UART)](../../Peripherals/UART/)

## メンバー


### uartBegin()



```c
uart_t* uartBegin(uint8_t uart_nr, uint32_t baudrate, uint32_t config, int8_t rxPin, int8_t txPin, uint16_t queueLen, bool inverted)
```

!!! summary "引数"
	- uint8_t `uart_nr` 
	- uint32_t `baudrate` 
	- uint32_t `config` 
	- int8_t `rxPin` 
	- int8_t `txPin` 
	- uint16_t `queueLen` 
	- bool `inverted` 

!!! note "戻り値"
	uart_t*



### uartEnd()



```c
void uartEnd(uart_t *uart)
```

!!! summary "引数"
	- uart_t* `uart` 

!!! note "戻り値"
	void



### uartAvailable()



```c
uint32_t uartAvailable(uart_t *uart)
```

!!! summary "引数"
	- uart_t* `uart` 

!!! note "戻り値"
	uint32_t



### uartAvailableForWrite()



```c
uint32_t uartAvailableForWrite(uart_t *uart)
```

!!! summary "引数"
	- uart_t* `uart` 

!!! note "戻り値"
	uint32_t



### uartRead()



```c
uint8_t uartRead(uart_t *uart)
```

!!! summary "引数"
	- uart_t* `uart` 

!!! note "戻り値"
	uint8_t



### uartPeek()



```c
uint8_t uartPeek(uart_t *uart)
```

!!! summary "引数"
	- uart_t* `uart` 

!!! note "戻り値"
	uint8_t



### uartWrite()



```c
void uartWrite(uart_t *uart, uint8_t c)
```

!!! summary "引数"
	- uart_t* `uart` 
	- uint8_t `c` 

!!! note "戻り値"
	void



### uartWriteBuf()



```c
void uartWriteBuf(uart_t *uart, const uint8_t *data, size_t len)
```

!!! summary "引数"
	- uart_t* `uart` 
	- const uint8_t * `data` 
	- size_t `len` 

!!! note "戻り値"
	void



### uartFlush()



```c
void uartFlush(uart_t *uart)
```

!!! summary "引数"
	- uart_t* `uart` 

!!! note "戻り値"
	void



### uartSetBaudRate()



```c
void uartSetBaudRate(uart_t *uart, uint32_t baud_rate)
```

!!! summary "引数"
	- uart_t* `uart` 
	- uint32_t `baud_rate` 

!!! note "戻り値"
	void



### uartGetBaudRate()



```c
uint32_t uartGetBaudRate(uart_t *uart)
```

!!! summary "引数"
	- uart_t* `uart` 

!!! note "戻り値"
	uint32_t



### uartResizeRxBuffer()



```c
size_t uartResizeRxBuffer(uart_t *uart, size_t new_size)
```

!!! summary "引数"
	- uart_t* `uart` 
	- size_t `new_size` 

!!! note "戻り値"
	size_t



### uartSetDebug()



```c
void uartSetDebug(uart_t *uart)
```

!!! summary "引数"
	- uart_t* `uart` 

!!! note "戻り値"
	void



### uartGetDebug()



```c
int uartGetDebug()
```

!!! note "戻り値"
	int



### uartDetectBaudrate()



```c
unsigned long uartDetectBaudrate(uart_t *uart)
```

!!! summary "引数"
	- uart_t* `uart` 

!!! note "戻り値"
	unsigned long



### uartRxActive()



```c
bool uartRxActive(uart_t *uart)
```

!!! summary "引数"
	- uart_t* `uart` 

!!! note "戻り値"
	bool



