# i2c

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/i2c.h>
```

上記宣言で利用できます。

## メンバー





















### i2c_driver_install()
I2C driver install


```c
esp_err_t i2c_driver_install(i2c_port_t i2c_num, i2c_mode_t mode, size_t slv_rx_buf_len, size_t slv_tx_buf_len, int intr_alloc_flags)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- i2c_mode_t `mode` I2C mode( master or slave ) 
	- size_t `slv_rx_buf_len` receiving buffer size for slave mode 
	- size_t `slv_tx_buf_len` 
	- int `intr_alloc_flags` 

!!! note "戻り値"
	esp_err_t



### i2c_driver_delete()
I2C driver delete


```c
esp_err_t i2c_driver_delete(i2c_port_t i2c_num)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number

!!! note "戻り値"
	esp_err_t 




### i2c_param_config()
I2C parameter initialization


```c
esp_err_t i2c_param_config(i2c_port_t i2c_num, const i2c_config_t *i2c_conf)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- i2c_config_tconst  * `i2c_conf` pointer to I2C parameter settings

!!! note "戻り値"
	esp_err_t 




### i2c_reset_tx_fifo()
reset I2C tx hardware fifo


```c
esp_err_t i2c_reset_tx_fifo(i2c_port_t i2c_num)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number

!!! note "戻り値"
	esp_err_t 




### i2c_reset_rx_fifo()
reset I2C rx fifo


```c
esp_err_t i2c_reset_rx_fifo(i2c_port_t i2c_num)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number

!!! note "戻り値"
	esp_err_t 




### i2c_isr_register()
I2C isr handler register


```c
esp_err_t i2c_isr_register(i2c_port_t i2c_num, void(*fn)(void *), void *arg, int intr_alloc_flags, intr_handle_t *handle)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- void(*)(void *) `fn` isr handler function 
	- void * `arg` parameter for isr handler function 
	- int `intr_alloc_flags` Flags used to allocate the interrupt. One or multiple (ORred) ESP_INTR_FLAG_* values. See esp_intr_alloc.h for more info. 
	- intr_handle_t * `handle` handle return from esp_intr_alloc.

!!! note "戻り値"
	esp_err_t 




### i2c_isr_free()
to delete and free I2C isr.


```c
esp_err_t i2c_isr_free(intr_handle_t handle)
```

!!! summary "引数"
	- intr_handle_t `handle` handle of isr.

!!! note "戻り値"
	esp_err_t 




### i2c_set_pin()
Configure GPIO signal for I2C sck and sda


```c
esp_err_t i2c_set_pin(i2c_port_t i2c_num, int sda_io_num, int scl_io_num, gpio_pullup_t sda_pullup_en, gpio_pullup_t scl_pullup_en, i2c_mode_t mode)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- int `sda_io_num` GPIO number for I2C sda signal 
	- int `scl_io_num` GPIO number for I2C scl signal 
	- gpio_pullup_t `sda_pullup_en` Whether to enable the internal pullup for sda pin 
	- gpio_pullup_t `scl_pullup_en` Whether to enable the internal pullup for scl pin 
	- i2c_mode_t `mode` I2C mode

!!! note "戻り値"
	esp_err_t 




### i2c_cmd_link_create()
Create and init I2C command link




```c
i2c_cmd_handle_t i2c_cmd_link_create()
```

!!! note "戻り値"
	i2c_cmd_handle_t



### i2c_cmd_link_delete()
Free I2C command link


```c
void i2c_cmd_link_delete(i2c_cmd_handle_t cmd_handle)
```

!!! summary "引数"
	- i2c_cmd_handle_t `cmd_handle` I2C command handle 

!!! note "戻り値"
	void



### i2c_master_start()
Queue command for I2C master to generate a start signal


```c
esp_err_t i2c_master_start(i2c_cmd_handle_t cmd_handle)
```

!!! summary "引数"
	- i2c_cmd_handle_t `cmd_handle` I2C cmd link

!!! note "戻り値"
	esp_err_t



### i2c_master_write_byte()
Queue command for I2C master to write one byte to I2C bus


```c
esp_err_t i2c_master_write_byte(i2c_cmd_handle_t cmd_handle, uint8_t data, bool ack_en)
```

!!! summary "引数"
	- i2c_cmd_handle_t `cmd_handle` I2C cmd link 
	- uint8_t `data` I2C one byte command to write to bus 
	- bool `ack_en` enable ack check for master

!!! note "戻り値"
	esp_err_t



### i2c_master_write()
Queue command for I2C master to write buffer to I2C bus


```c
esp_err_t i2c_master_write(i2c_cmd_handle_t cmd_handle, uint8_t *data, size_t data_len, bool ack_en)
```

!!! summary "引数"
	- i2c_cmd_handle_t `cmd_handle` I2C cmd link 
	- uint8_t * `data` data to send 
	- size_t `data_len` 
	- bool `ack_en` 

!!! note "戻り値"
	esp_err_t



### i2c_master_read_byte()
Queue command for I2C master to read one byte from I2C bus


```c
esp_err_t i2c_master_read_byte(i2c_cmd_handle_t cmd_handle, uint8_t *data, i2c_ack_type_t ack)
```

!!! summary "引数"
	- i2c_cmd_handle_t `cmd_handle` I2C cmd link 
	- uint8_t * `data` pointer accept the data byte 
	- i2c_ack_type_t `ack` 

!!! note "戻り値"
	esp_err_t



### i2c_master_read()
Queue command for I2C master to read data from I2C bus


```c
esp_err_t i2c_master_read(i2c_cmd_handle_t cmd_handle, uint8_t *data, size_t data_len, i2c_ack_type_t ack)
```

!!! summary "引数"
	- i2c_cmd_handle_t `cmd_handle` I2C cmd link 
	- uint8_t * `data` data buffer to accept the data from bus 
	- size_t `data_len` 
	- i2c_ack_type_t `ack` 

!!! note "戻り値"
	esp_err_t



### i2c_master_stop()
Queue command for I2C master to generate a stop signal


```c
esp_err_t i2c_master_stop(i2c_cmd_handle_t cmd_handle)
```

!!! summary "引数"
	- i2c_cmd_handle_t `cmd_handle` I2C cmd link

!!! note "戻り値"
	esp_err_t



### i2c_master_cmd_begin()
I2C master send queued commands. This function will trigger sending all queued commands. The task will be blocked until all the commands have been sent out. The I2C APIs are not thread-safe, if you want to use one I2C port in different tasks, you need to take care of the multi-thread issue.


```c
esp_err_t i2c_master_cmd_begin(i2c_port_t i2c_num, i2c_cmd_handle_t cmd_handle, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- i2c_cmd_handle_t `cmd_handle` I2C command handler 
	- TickType_t `ticks_to_wait` maximum wait ticks.

!!! note "戻り値"
	esp_err_t



### i2c_slave_write_buffer()
I2C slave write data to internal ringbuffer, when tx fifo empty, isr will fill the hardware fifo from the internal ringbuffer


```c
int i2c_slave_write_buffer(i2c_port_t i2c_num, uint8_t *data, int size, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- uint8_t * `data` data pointer to write into internal buffer 
	- int `size` data size 
	- TickType_t `ticks_to_wait` Maximum waiting ticks

!!! note "戻り値"
	int



### i2c_slave_read_buffer()
I2C slave read data from internal buffer. When I2C slave receive data, isr will copy received data from hardware rx fifo to internal ringbuffer. Then users can read from internal ringbuffer.


```c
int i2c_slave_read_buffer(i2c_port_t i2c_num, uint8_t *data, size_t max_size, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- uint8_t * `data` data pointer to write into internal buffer 
	- size_t `max_size` Maximum data size to read 
	- TickType_t `ticks_to_wait` Maximum waiting ticks

!!! note "戻り値"
	int



### i2c_set_period()
set I2C master clock period


```c
esp_err_t i2c_set_period(i2c_port_t i2c_num, int high_period, int low_period)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- int `high_period` clock cycle number during SCL is high level, high_period is a 14 bit value 
	- int `low_period` clock cycle number during SCL is low level, low_period is a 14 bit value

!!! note "戻り値"
	esp_err_t 




### i2c_get_period()
get I2C master clock period


```c
esp_err_t i2c_get_period(i2c_port_t i2c_num, int *high_period, int *low_period)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- int * `high_period` pointer to get clock cycle number during SCL is high level, will get a 14 bit value 
	- int * `low_period` pointer to get clock cycle number during SCL is low level, will get a 14 bit value

!!! note "戻り値"
	esp_err_t 




### i2c_filter_enable()
enable hardware filter on I2C bus Sometimes the I2C bus is disturbed by high frequency noise(about 20ns), or the rising edge of the SCL clock is very slow, these may cause the master state machine broken. enable hardware filter can filter out high frequency interference and make the master more stable.


```c
esp_err_t i2c_filter_enable(i2c_port_t i2c_num, uint8_t cyc_num)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- uint8_t `cyc_num` the APB cycles need to be filtered(0<= cyc_num <=7). When the period of a pulse is less than cyc_num * APB_cycle, the I2C controller will ignore this pulse.

!!! note "戻り値"
	esp_err_t



### i2c_filter_disable()
disable filter on I2C bus


```c
esp_err_t i2c_filter_disable(i2c_port_t i2c_num)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number

!!! note "戻り値"
	esp_err_t 




### i2c_set_start_timing()
set I2C master start signal timing


```c
esp_err_t i2c_set_start_timing(i2c_port_t i2c_num, int setup_time, int hold_time)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- int `setup_time` clock number between the falling-edge of SDA and rising-edge of SCL for start mark, it's a 10-bit value. 
	- int `hold_time` clock num between the falling-edge of SDA and falling-edge of SCL for start mark, it's a 10-bit value.

!!! note "戻り値"
	esp_err_t 




### i2c_get_start_timing()
get I2C master start signal timing


```c
esp_err_t i2c_get_start_timing(i2c_port_t i2c_num, int *setup_time, int *hold_time)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- int * `setup_time` pointer to get setup time 
	- int * `hold_time` pointer to get hold time

!!! note "戻り値"
	esp_err_t 




### i2c_set_stop_timing()
set I2C master stop signal timing


```c
esp_err_t i2c_set_stop_timing(i2c_port_t i2c_num, int setup_time, int hold_time)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- int `setup_time` clock num between the rising-edge of SCL and the rising-edge of SDA, it's a 10-bit value. 
	- int `hold_time` clock number after the STOP bit's rising-edge, it's a 14-bit value.

!!! note "戻り値"
	esp_err_t 




### i2c_get_stop_timing()
get I2C master stop signal timing


```c
esp_err_t i2c_get_stop_timing(i2c_port_t i2c_num, int *setup_time, int *hold_time)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- int * `setup_time` pointer to get setup time. 
	- int * `hold_time` pointer to get hold time.

!!! note "戻り値"
	esp_err_t 




### i2c_set_data_timing()
set I2C data signal timing


```c
esp_err_t i2c_set_data_timing(i2c_port_t i2c_num, int sample_time, int hold_time)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- int `sample_time` clock number I2C used to sample data on SDA after the rising-edge of SCL, it's a 10-bit value 
	- int `hold_time` clock number I2C used to hold the data after the falling-edge of SCL, it's a 10-bit value

!!! note "戻り値"
	esp_err_t 




### i2c_get_data_timing()
get I2C data signal timing


```c
esp_err_t i2c_get_data_timing(i2c_port_t i2c_num, int *sample_time, int *hold_time)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- int * `sample_time` pointer to get sample time 
	- int * `hold_time` pointer to get hold time

!!! note "戻り値"
	esp_err_t 




### i2c_set_timeout()
set I2C timeout value


```c
esp_err_t i2c_set_timeout(i2c_port_t i2c_num, int timeout)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- int `timeout` timeout value for I2C bus (unit: APB 80Mhz clock cycle) 

!!! note "戻り値"
	esp_err_t 




### i2c_get_timeout()
get I2C timeout value


```c
esp_err_t i2c_get_timeout(i2c_port_t i2c_num, int *timeout)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- int * `timeout` pointer to get timeout value 

!!! note "戻り値"
	esp_err_t 




### i2c_set_data_mode()
set I2C data transfer mode


```c
esp_err_t i2c_set_data_mode(i2c_port_t i2c_num, i2c_trans_mode_t tx_trans_mode, i2c_trans_mode_t rx_trans_mode)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- i2c_trans_mode_t `tx_trans_mode` I2C sending data mode 
	- i2c_trans_mode_t `rx_trans_mode` I2C receving data mode

!!! note "戻り値"
	esp_err_t 




### i2c_get_data_mode()
get I2C data transfer mode


```c
esp_err_t i2c_get_data_mode(i2c_port_t i2c_num, i2c_trans_mode_t *tx_trans_mode, i2c_trans_mode_t *rx_trans_mode)
```

!!! summary "引数"
	- i2c_port_t `i2c_num` I2C port number 
	- i2c_trans_mode_t* `tx_trans_mode` pointer to get I2C sending data mode 
	- i2c_trans_mode_t* `rx_trans_mode` pointer to get I2C receiving data mode

!!! note "戻り値"
	esp_err_t 




