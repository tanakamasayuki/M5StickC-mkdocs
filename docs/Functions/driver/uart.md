# uart

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/uart.h>
```

上記宣言で利用できます。

## メンバー

### uart_set_word_length()
Set UART data bits.


```c
esp_err_t uart_set_word_length(uart_port_t uart_num, uart_word_length_t data_bit)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uart_word_length_t `data_bit` UART data bits

!!! note "戻り値"
	esp_err_t 




### uart_get_word_length()
Get UART data bits.


```c
esp_err_t uart_get_word_length(uart_port_t uart_num, uart_word_length_t *data_bit)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uart_word_length_t* `data_bit` Pointer to accept value of UART data bits.

!!! note "戻り値"
	esp_err_t 




### uart_set_stop_bits()
Set UART stop bits.


```c
esp_err_t uart_set_stop_bits(uart_port_t uart_num, uart_stop_bits_t stop_bits)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uart_stop_bits_t `stop_bits` UART stop bits

!!! note "戻り値"
	esp_err_t 




### uart_get_stop_bits()
Get UART stop bits.


```c
esp_err_t uart_get_stop_bits(uart_port_t uart_num, uart_stop_bits_t *stop_bits)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uart_stop_bits_t* `stop_bits` Pointer to accept value of UART stop bits.

!!! note "戻り値"
	esp_err_t 




### uart_set_parity()
Set UART parity mode.


```c
esp_err_t uart_set_parity(uart_port_t uart_num, uart_parity_t parity_mode)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uart_parity_t `parity_mode` the enum of uart parity configuration

!!! note "戻り値"
	esp_err_t 




### uart_get_parity()
Get UART parity mode.


```c
esp_err_t uart_get_parity(uart_port_t uart_num, uart_parity_t *parity_mode)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uart_parity_t* `parity_mode` Pointer to accept value of UART parity mode.

!!! note "戻り値"
	esp_err_t 




### uart_set_baudrate()
Set UART baud rate.


```c
esp_err_t uart_set_baudrate(uart_port_t uart_num, uint32_t baudrate)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uint32_t `baudrate` UART baud rate.

!!! note "戻り値"
	esp_err_t 




### uart_get_baudrate()
Get UART baud rate.


```c
esp_err_t uart_get_baudrate(uart_port_t uart_num, uint32_t *baudrate)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uint32_t * `baudrate` Pointer to accept value of UART baud rate

!!! note "戻り値"
	esp_err_t 




### uart_set_line_inverse()
Set UART line inverse mode


```c
esp_err_t uart_set_line_inverse(uart_port_t uart_num, uint32_t inverse_mask)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uint32_t `inverse_mask` Choose the wires that need to be inverted. Inverse_mask should be chosen from UART_INVERSE_RXD / UART_INVERSE_TXD / UART_INVERSE_RTS / UART_INVERSE_CTS, combined with OR operation.

!!! note "戻り値"
	esp_err_t 




### uart_set_hw_flow_ctrl()
Set hardware flow control.


```c
esp_err_t uart_set_hw_flow_ctrl(uart_port_t uart_num, uart_hw_flowcontrol_t flow_ctrl, uint8_t rx_thresh)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uart_hw_flowcontrol_t `flow_ctrl` Hardware flow control mode 
	- uint8_t `rx_thresh` Threshold of Hardware RX flow control (0 ~ UART_FIFO_LEN). Only when UART_HW_FLOWCTRL_RTS is set, will the rx_thresh value be set.

!!! note "戻り値"
	esp_err_t 




### uart_set_sw_flow_ctrl()
Set software flow control.


```c
esp_err_t uart_set_sw_flow_ctrl(uart_port_t uart_num, bool enable, uint8_t rx_thresh_xon, uint8_t rx_thresh_xoff)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- bool `enable` switch on or off 
	- uint8_t `rx_thresh_xon` low water mark 
	- uint8_t `rx_thresh_xoff` high water mark

!!! note "戻り値"
	esp_err_t 




### uart_get_hw_flow_ctrl()
Get hardware flow control mode


```c
esp_err_t uart_get_hw_flow_ctrl(uart_port_t uart_num, uart_hw_flowcontrol_t *flow_ctrl)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uart_hw_flowcontrol_t* `flow_ctrl` Option for different flow control mode.

!!! note "戻り値"
	esp_err_t 




### uart_clear_intr_status()
Clear UART interrupt status


```c
esp_err_t uart_clear_intr_status(uart_port_t uart_num, uint32_t clr_mask)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uint32_t `clr_mask` Bit mask of the interrupt status to be cleared. The bit mask should be composed from the fields of register UART_INT_CLR_REG.

!!! note "戻り値"
	esp_err_t 




### uart_enable_intr_mask()
Set UART interrupt enable


```c
esp_err_t uart_enable_intr_mask(uart_port_t uart_num, uint32_t enable_mask)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uint32_t `enable_mask` Bit mask of the enable bits. The bit mask should be composed from the fields of register UART_INT_ENA_REG.

!!! note "戻り値"
	esp_err_t 




### uart_disable_intr_mask()
Clear UART interrupt enable bits


```c
esp_err_t uart_disable_intr_mask(uart_port_t uart_num, uint32_t disable_mask)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uint32_t `disable_mask` Bit mask of the disable bits. The bit mask should be composed from the fields of register UART_INT_ENA_REG.

!!! note "戻り値"
	esp_err_t 




### uart_enable_rx_intr()
Enable UART RX interrupt (RX_FULL & RX_TIMEOUT INTERRUPT)


```c
esp_err_t uart_enable_rx_intr(uart_port_t uart_num)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2

!!! note "戻り値"
	esp_err_t 




### uart_disable_rx_intr()
Disable UART RX interrupt (RX_FULL & RX_TIMEOUT INTERRUPT)


```c
esp_err_t uart_disable_rx_intr(uart_port_t uart_num)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2

!!! note "戻り値"
	esp_err_t 




### uart_disable_tx_intr()
Disable UART TX interrupt (TX_FULL & TX_TIMEOUT INTERRUPT)


```c
esp_err_t uart_disable_tx_intr(uart_port_t uart_num)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2

!!! note "戻り値"
	esp_err_t 




### uart_enable_tx_intr()
Enable UART TX interrupt (TX_FULL & TX_TIMEOUT INTERRUPT)


```c
esp_err_t uart_enable_tx_intr(uart_port_t uart_num, int enable, int thresh)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- int `enable` 1: enable; 0: disable 
	- int `thresh` Threshold of TX interrupt, 0 ~ UART_FIFO_LEN

!!! note "戻り値"
	esp_err_t 




### uart_isr_register()
Register UART interrupt handler (ISR).


```c
esp_err_t uart_isr_register(uart_port_t uart_num, void(*fn)(void *), void *arg, int intr_alloc_flags, uart_isr_handle_t *handle)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- void(*)(void *) `fn` Interrupt handler function. 
	- void * `arg` parameter for handler function 
	- int `intr_alloc_flags` Flags used to allocate the interrupt. One or multiple (ORred) ESP_INTR_FLAG_* values. See esp_intr_alloc.h for more info. 
	- uart_isr_handle_t* `handle` Pointer to return handle. If non-NULL, a handle for the interrupt will be returned here.

!!! note "戻り値"
	esp_err_t



### uart_isr_free()
Free UART interrupt handler registered by uart_isr_register. Must be called on the same core as uart_isr_register was called.


```c
esp_err_t uart_isr_free(uart_port_t uart_num)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2

!!! note "戻り値"
	esp_err_t 




### uart_set_pin()
Set UART pin number


```c
esp_err_t uart_set_pin(uart_port_t uart_num, int tx_io_num, int rx_io_num, int rts_io_num, int cts_io_num)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- int `tx_io_num` UART TX pin GPIO number. 
	- int `rx_io_num` UART RX pin GPIO number. 
	- int `rts_io_num` UART RTS pin GPIO number. 
	- int `cts_io_num` UART CTS pin GPIO number.

!!! note "戻り値"
	esp_err_t



### uart_set_rts()
Manually set the UART RTS pin level.


```c
esp_err_t uart_set_rts(uart_port_t uart_num, int level)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- int `level` 1: RTS output low (active); 0: RTS output high (block)

!!! note "戻り値"
	esp_err_t



### uart_set_dtr()
Manually set the UART DTR pin level.


```c
esp_err_t uart_set_dtr(uart_port_t uart_num, int level)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- int `level` 1: DTR output low; 0: DTR output high

!!! note "戻り値"
	esp_err_t 




### uart_set_tx_idle_num()
Set UART idle interval after tx FIFO is empty


```c
esp_err_t uart_set_tx_idle_num(uart_port_t uart_num, uint16_t idle_num)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uint16_t `idle_num` idle interval after tx FIFO is empty(unit: the time it takes to send one bit under current baudrate)

!!! note "戻り値"
	esp_err_t 




### uart_param_config()
Set UART configuration parameters.


```c
esp_err_t uart_param_config(uart_port_t uart_num, const uart_config_t *uart_config)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uart_config_tconst  * `uart_config` UART parameter settings

!!! note "戻り値"
	esp_err_t 




### uart_intr_config()
Configure UART interrupts.


```c
esp_err_t uart_intr_config(uart_port_t uart_num, const uart_intr_config_t *intr_conf)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uart_intr_config_tconst  * `intr_conf` UART interrupt settings

!!! note "戻り値"
	esp_err_t 




### uart_driver_install()
Install UART driver.

UART ISR handler will be attached to the same CPU core that this function is running on.
```c
esp_err_t uart_driver_install(uart_port_t uart_num, int rx_buffer_size, int tx_buffer_size, int queue_size, QueueHandle_t *uart_queue, int intr_alloc_flags)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- int `rx_buffer_size` UART RX ring buffer size. 
	- int `tx_buffer_size` UART TX ring buffer size. If set to zero, driver will not use TX buffer, TX function will block task until all data have been sent out. 
	- int `queue_size` UART event queue size/depth. 
	- QueueHandle_t * `uart_queue` UART event queue handle (out param). On success, a new queue handle is written here to provide access to UART events. If set to NULL, driver will not use an event queue. 
	- int `intr_alloc_flags` Flags used to allocate the interrupt. One or multiple (ORred) ESP_INTR_FLAG_* values. See esp_intr_alloc.h for more info. Do not set ESP_INTR_FLAG_IRAM here (the driver's ISR handler is not located in IRAM)

!!! note "戻り値"
	esp_err_t



### uart_driver_delete()
Uninstall UART driver.


```c
esp_err_t uart_driver_delete(uart_port_t uart_num)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2

!!! note "戻り値"
	esp_err_t 




### uart_wait_tx_done()
Wait until UART TX FIFO is empty.


```c
esp_err_t uart_wait_tx_done(uart_port_t uart_num, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- TickType_t `ticks_to_wait` Timeout, count in RTOS ticks

!!! note "戻り値"
	esp_err_t 




### uart_tx_chars()
Send data to the UART port from a given buffer and length.


```c
int uart_tx_chars(uart_port_t uart_num, const char *buffer, uint32_t len)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- const char * `buffer` data buffer address 
	- uint32_t `len` data length to send

!!! note "戻り値"
	int



### uart_write_bytes()
Send data to the UART port from a given buffer and length,

Otherwise, if the 'tx_buffer_size' > 0, this function will return after copying all the data to tx ring buffer, UART ISR will then move data from the ring buffer to TX FIFO gradually.
```c
int uart_write_bytes(uart_port_t uart_num, const char *src, size_t size)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- const char * `src` data buffer address 
	- size_t `size` data length to send

!!! note "戻り値"
	int



### uart_write_bytes_with_break()
Send data to the UART port from a given buffer and length,

Otherwise, if the 'tx_buffer_size' > 0, this function will return after copying all the data to tx ring buffer, UART ISR will then move data from the ring buffer to TX FIFO gradually. After all data sent out, send a break signal.
```c
int uart_write_bytes_with_break(uart_port_t uart_num, const char *src, size_t size, int brk_len)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- const char * `src` data buffer address 
	- size_t `size` data length to send 
	- int `brk_len` break signal duration(unit: the time it takes to send one bit at current baudrate)

!!! note "戻り値"
	int



### uart_read_bytes()
UART read bytes from UART buffer


```c
int uart_read_bytes(uart_port_t uart_num, uint8_t *buf, uint32_t length, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2 
	- uint8_t * `buf` pointer to the buffer. 
	- uint32_t `length` data length 
	- TickType_t `ticks_to_wait` sTimeout, count in RTOS ticks

!!! note "戻り値"
	int 




### uart_flush()
Alias of uart_flush_input. UART ring buffer flush. This will discard all data in the UART RX buffer.


```c
esp_err_t uart_flush(uart_port_t uart_num)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2

!!! note "戻り値"
	esp_err_t



### uart_flush_input()
Clear input buffer, discard all the data is in the ring-buffer.


```c
esp_err_t uart_flush_input(uart_port_t uart_num)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART_NUM_0, UART_NUM_1 or UART_NUM_2

!!! note "戻り値"
	esp_err_t



### uart_get_buffered_data_len()
UART get RX ring buffer cached data length


```c
esp_err_t uart_get_buffered_data_len(uart_port_t uart_num, size_t *size)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART port number. 
	- size_t * `size` Pointer of size_t to accept cached data length

!!! note "戻り値"
	esp_err_t 




### uart_disable_pattern_det_intr()
UART disable pattern detect function. Designed for applications like 'AT commands'. When the hardware detects a series of one same character, the interrupt will be triggered.


```c
esp_err_t uart_disable_pattern_det_intr(uart_port_t uart_num)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART port number.

!!! note "戻り値"
	esp_err_t 




### uart_enable_pattern_det_intr()
UART enable pattern detect function. Designed for applications like 'AT commands'. When the hardware detect a series of one same character, the interrupt will be triggered.


```c
esp_err_t uart_enable_pattern_det_intr(uart_port_t uart_num, char pattern_chr, uint8_t chr_num, int chr_tout, int post_idle, int pre_idle)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART port number. 
	- char `pattern_chr` character of the pattern 
	- uint8_t `chr_num` number of the character, 8bit value. 
	- int `chr_tout` timeout of the interval between each pattern characters, 24bit value, unit is APB (80Mhz) clock cycle. When the duration is less than this value, it will not take this data as at_cmd char 
	- int `post_idle` idle time after the last pattern character, 24bit value, unit is APB (80Mhz) clock cycle. When the duration is less than this value, it will not take the previous data as the last at_cmd char 
	- int `pre_idle` idle time before the first pattern character, 24bit value, unit is APB (80Mhz) clock cycle. When the duration is less than this value, it will not take this data as the first at_cmd char

!!! note "戻り値"
	esp_err_t 




### uart_pattern_pop_pos()
Return the nearest detected pattern position in buffer. The positions of the detected pattern are saved in a queue, this function will dequeue the first pattern position and move the pointer to next pattern position.


The following APIs will modify the pattern position info: uart_flush_input, uart_read_bytes, uart_driver_delete, uart_pop_pattern_pos It is the application's responsibility to ensure atomic access to the pattern queue and the rx data buffer when using pattern detect feature.
```c
int uart_pattern_pop_pos(uart_port_t uart_num)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART port number 

!!! note "戻り値"
	int



### uart_pattern_get_pos()
Return the nearest detected pattern position in buffer. The positions of the detected pattern are saved in a queue, This function do nothing to the queue.


The following APIs will modify the pattern position info: uart_flush_input, uart_read_bytes, uart_driver_delete, uart_pop_pattern_pos It is the application's responsibility to ensure atomic access to the pattern queue and the rx data buffer when using pattern detect feature.
```c
int uart_pattern_get_pos(uart_port_t uart_num)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART port number 

!!! note "戻り値"
	int



### uart_pattern_queue_reset()
Allocate a new memory with the given length to save record the detected pattern position in rx buffer.


```c
esp_err_t uart_pattern_queue_reset(uart_port_t uart_num, int queue_length)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART port number 
	- int `queue_length` Max queue length for the detected pattern. If the queue length is not large enough, some pattern positions might be lost. Set this value to the maximum number of patterns that could be saved in data buffer at the same time. 

!!! note "戻り値"
	esp_err_t 




### uart_set_mode()
UART set communication mode


```c
esp_err_t uart_set_mode(uart_port_t uart_num, uart_mode_t mode)
```

!!! summary "引数"
	- uart_port_t `uart_num` Uart number to configure 
	- uart_mode_t `mode` UART UART mode to set

!!! note "戻り値"
	esp_err_t



### uart_set_rx_timeout()
UART set threshold timeout for TOUT feature


```c
esp_err_t uart_set_rx_timeout(uart_port_t uart_num, const uint8_t tout_thresh)
```

!!! summary "引数"
	- uart_port_t `uart_num` Uart number to configure 
	- const uint8_t `tout_thresh` This parameter defines timeout threshold in uart symbol periods. The maximum value of threshold is 126. tout_thresh = 1, defines TOUT interrupt timeout equal to transmission time of one symbol (~11 bit) on current baudrate. If the time is expired the UART_RXFIFO_TOUT_INT interrupt is triggered. If tout_thresh == 0, the TOUT feature is disabled.

!!! note "戻り値"
	esp_err_t 




### uart_get_collision_flag()
Returns collision detection flag for RS485 mode Function returns the collision detection flag into variable pointed by collision_flag. *collision_flag = true, if collision detected else it is equal to false. This function should be executed when actual transmission is completed (after ).


```c
esp_err_t uart_get_collision_flag(uart_port_t uart_num, bool *collision_flag)
```

!!! summary "引数"
	- uart_port_t `uart_num` Uart number to configure 
	- bool * `collision_flag` Pointer to variable of type bool to return collision flag.

!!! note "戻り値"
	esp_err_t 




### uart_set_wakeup_threshold()
Set the number of RX pin signal edges for light sleep wakeup

The character that triggers wakeup is not received by UART (i.e. it can not be obtained from UART FIFO). Depending on the baud rate, a few characters after that will also not be received. Note that when the chip enters and exits light sleep mode, APB frequency will be changing. To make sure that UART has correct baud rate all the time, select REF_TICK as UART clock source, by setting use_ref_tick field in  to true.
```c
esp_err_t uart_set_wakeup_threshold(uart_port_t uart_num, int wakeup_threshold)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART number 
	- int `wakeup_threshold` number of RX edges for light sleep wakeup, value is 3 .. 0x3ff. 

!!! note "戻り値"
	esp_err_t



### uart_get_wakeup_threshold()
Get the number of RX pin signal edges for light sleep wakeup.

See description of uart_set_wakeup_threshold for the explanation of UART wakeup feature.
```c
esp_err_t uart_get_wakeup_threshold(uart_port_t uart_num, int *out_wakeup_threshold)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART number 
	- int * `out_wakeup_threshold` output, set to the current value of wakeup threshold for the given UART. 

!!! note "戻り値"
	esp_err_t



