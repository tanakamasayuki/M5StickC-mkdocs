# sdio_slave

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/sdio_slave.h>
```

上記宣言で利用できます。

## メンバー



















### sdio_slave_initialize()


Initialize the sdio slave driver
```c
esp_err_t sdio_slave_initialize(sdio_slave_config_t *config)
```

!!! summary "引数"
	- sdio_slave_config_t* `config` Configuration of the sdio slave driver.

!!! note "戻り値"
	esp_err_t



### sdio_slave_deinit()


De-initialize the sdio slave driver to release the resources. 
```c
void sdio_slave_deinit()
```

!!! note "戻り値"
	void



### sdio_slave_start()





```c
esp_err_t sdio_slave_start()
```

!!! note "戻り値"
	esp_err_t



### sdio_slave_stop()




```c
void sdio_slave_stop()
```

!!! note "戻り値"
	void



### sdio_slave_reset()




```c
esp_err_t sdio_slave_reset()
```

!!! note "戻り値"
	esp_err_t



### sdio_slave_recv_register_buf()


Register buffer used for receiving. All buffers should be registered before used, and then can be used (again) in the driver by the handle returned.
```c
sdio_slave_buf_handle_t sdio_slave_recv_register_buf(uint8_t *start)
```

!!! summary "引数"
	- uint8_t * `start` The start address of the buffer.

!!! note "戻り値"
	sdio_slave_buf_handle_t



### sdio_slave_recv_unregister_buf()


Unregister buffer from driver, and free the space used by the descriptor pointing to the buffer.
```c
esp_err_t sdio_slave_recv_unregister_buf(sdio_slave_buf_handle_t handle)
```

!!! summary "引数"
	- sdio_slave_buf_handle_t `handle` Handle to the buffer to release.

!!! note "戻り値"
	esp_err_t



### sdio_slave_recv_load_buf()


Load buffer to the queue waiting to receive data. The driver takes ownership of the buffer until the buffer is returned by  after the transaction is finished.
```c
esp_err_t sdio_slave_recv_load_buf(sdio_slave_buf_handle_t handle)
```

!!! summary "引数"
	- sdio_slave_buf_handle_t `handle` Handle to the buffer ready to receive data.

!!! note "戻り値"
	esp_err_t



### sdio_slave_recv()


Get received data if exist. The driver returns the ownership of the buffer to the app.
```c
esp_err_t sdio_slave_recv(sdio_slave_buf_handle_t *handle_ret, uint8_t **out_addr, size_t *out_len, TickType_t wait)
```

!!! summary "引数"
	- sdio_slave_buf_handle_t* `handle_ret` Handle to the buffer holding received data. Use this handle in  to receive in the same buffer again. 
	- uint8_t ** `out_addr` Output of the start address, set to NULL if not needed. 
	- size_t * `out_len` Actual length of the data in the buffer, set to NULL if not needed. 
	- TickType_t `wait` Time to wait before data received.

!!! note "戻り値"
	esp_err_t



### sdio_slave_recv_get_buf()


Retrieve the buffer corresponding to a handle.
```c
uint8_t* sdio_slave_recv_get_buf(sdio_slave_buf_handle_t handle, size_t *len_o)
```

!!! summary "引数"
	- sdio_slave_buf_handle_t `handle` Handle to get the buffer. 
	- size_t * `len_o` Output of buffer length

!!! note "戻り値"
	uint8_t *



### sdio_slave_send_queue()


Put a new sending transfer into the send queue. The driver takes ownership of the buffer until the buffer is returned by  after the transaction is finished.
```c
esp_err_t sdio_slave_send_queue(uint8_t *addr, size_t len, void *arg, TickType_t wait)
```

!!! summary "引数"
	- uint8_t * `addr` Address for data to be sent. The buffer should be DMA capable and 32-bit aligned. 
	- size_t `len` Length of the data, should not be longer than 4092 bytes (may support longer in the future). 
	- void * `arg` Argument to returned in . The argument can be used to indicate which transaction is done, or as a parameter for a callback. Set to NULL if not needed. 
	- TickType_t `wait` Time to wait if the buffer is full.

!!! note "戻り値"
	esp_err_t



### sdio_slave_send_get_finished()



```c
esp_err_t sdio_slave_send_get_finished(void **out_arg, TickType_t wait)
```

!!! summary "引数"
	- void ** `out_arg` Argument of the finished transaction. Set to NULL if unused. 
	- TickType_t `wait` Time to wait if there's no finished sending transaction.

!!! note "戻り値"
	esp_err_t ESP_ERR_TIMEOUT if no transaction finished, or ESP_OK if succeed. 



### sdio_slave_transmit()


Start a new sending transfer, and wait for it (blocked) to be finished.
```c
esp_err_t sdio_slave_transmit(uint8_t *addr, size_t len)
```

!!! summary "引数"
	- uint8_t * `addr` Start address of the buffer to send 
	- size_t `len` Length of buffer to send.

!!! note "戻り値"
	esp_err_t



### sdio_slave_read_reg()


Read the spi slave register shared with host.
```c
uint8_t sdio_slave_read_reg(int pos)
```

!!! summary "引数"
	- int `pos` register address, 0-27 or 32-63.

!!! note "戻り値"
	uint8_t



### sdio_slave_write_reg()


Write the spi slave register shared with host.
```c
esp_err_t sdio_slave_write_reg(int pos, uint8_t reg)
```

!!! summary "引数"
	- int `pos` register address, 0-11, 14-15, 18-19, 24-27 and 32-63, other address are reserved. 
	- uint8_t `reg` the value to write.

!!! note "戻り値"
	esp_err_t



### sdio_slave_get_host_intena()




```c
sdio_slave_hostint_t sdio_slave_get_host_intena()
```

!!! note "戻り値"
	sdio_slave_hostint_t



### sdio_slave_set_host_intena()


Set the interrupt enable for host.
```c
void sdio_slave_set_host_intena(sdio_slave_hostint_t ena)
```

!!! summary "引数"
	- sdio_slave_hostint_t `ena` Enable mask for host interrupt. 

!!! note "戻り値"
	void



### sdio_slave_send_host_int()


Interrupt the host by general purpose interrupt.
```c
esp_err_t sdio_slave_send_host_int(uint8_t pos)
```

!!! summary "引数"
	- uint8_t `pos` Interrupt num, 0-7.

!!! note "戻り値"
	esp_err_t



### sdio_slave_clear_host_int()


Clear general purpose interrupt to host.
```c
void sdio_slave_clear_host_int(uint8_t mask)
```

!!! summary "引数"
	- uint8_t `mask` Interrupt bits to clear, by bit mask. 

!!! note "戻り値"
	void



### sdio_slave_wait_int()


Wait for general purpose interrupt from host.
```c
esp_err_t sdio_slave_wait_int(int pos, TickType_t wait)
```

!!! summary "引数"
	- int `pos` Interrupt source number to wait for. is set. 
	- TickType_t `wait` Time to wait before interrupt triggered.

!!! note "戻り値"
	esp_err_t



