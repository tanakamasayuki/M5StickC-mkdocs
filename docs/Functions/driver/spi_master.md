# spi_master

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/spi_master.h>
```

上記宣言で利用できます。

## メンバー

























































### spi_bus_initialize()
Initialize a SPI bus


```c
esp_err_t spi_bus_initialize(spi_host_device_t host, const spi_bus_config_t *bus_config, int dma_chan)
```

!!! summary "引数"
	- spi_host_device_t `host` SPI peripheral that controls this bus 
	- spi_bus_config_tconst  * `bus_config` Pointer to a  struct specifying how the host should be initialized 
	- int `dma_chan` Either channel 1 or 2, or 0 in the case when no DMA is required. Selecting a DMA channel for a SPI bus allows transfers on the bus to have sizes only limited by the amount of internal memory. Selecting no DMA channel (by passing the value 0) limits the amount of bytes transfered to a maximum of 32.

!!! note "戻り値"
	esp_err_t



### spi_bus_free()
Free a SPI bus


```c
esp_err_t spi_bus_free(spi_host_device_t host)
```

!!! summary "引数"
	- spi_host_device_t `host` SPI peripheral to free 

!!! note "戻り値"
	esp_err_t



### spi_bus_add_device()
Allocate a device on a SPI bus

This initializes the internal structures for a device, plus allocates a CS pin on the indicated SPI master peripheral and routes it to the indicated GPIO. All SPI master devices have three CS pins and can thus control up to three devices.
```c
esp_err_t spi_bus_add_device(spi_host_device_t host, const spi_device_interface_config_t *dev_config, spi_device_handle_t *handle)
```

!!! summary "引数"
	- spi_host_device_t `host` SPI peripheral to allocate device on 
	- spi_device_interface_config_tconst  * `dev_config` SPI interface protocol config for the device 
	- spi_device_handle_t* `handle` Pointer to variable to hold the device handle 

!!! note "戻り値"
	esp_err_t



### spi_bus_remove_device()
Remove a device from the SPI bus


```c
esp_err_t spi_bus_remove_device(spi_device_handle_t handle)
```

!!! summary "引数"
	- spi_device_handle_t `handle` Device handle to free 

!!! note "戻り値"
	esp_err_t 




### spi_device_queue_trans()
Queue a SPI transaction for interrupt transaction execution. Get the result by .


```c
esp_err_t spi_device_queue_trans(spi_device_handle_t handle, spi_transaction_t *trans_desc, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- spi_device_handle_t `handle` Device handle obtained using spi_host_add_dev 
	- spi_transaction_t* `trans_desc` Description of transaction to execute 
	- TickType_t `ticks_to_wait` Ticks to wait until there's room in the queue; use portMAX_DELAY to never time out. 

!!! note "戻り値"
	esp_err_t



### spi_device_get_trans_result()
Get the result of a SPI transaction queued earlier by .

This routine will wait until a transaction to the given device succesfully completed. It will then return the description of the completed transaction so software can inspect the result and e.g. free the memory or re-use the buffers.
```c
esp_err_t spi_device_get_trans_result(spi_device_handle_t handle, spi_transaction_t **trans_desc, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- spi_device_handle_t `handle` Device handle obtained using spi_host_add_dev 
	- spi_transaction_t** `trans_desc` Pointer to variable able to contain a pointer to the description of the transaction that is executed. The descriptor should not be modified until the descriptor is returned by spi_device_get_trans_result. 
	- TickType_t `ticks_to_wait` Ticks to wait until there's a returned item; use portMAX_DELAY to never time out. 

!!! note "戻り値"
	esp_err_t



### spi_device_transmit()
Send a SPI transaction, wait for it to complete, and return the result

This function is the equivalent of calling  followed by . Do not use this when there is still a transaction separately queued (started) from  or polling_start/transmit that hasn't been finalized.
```c
esp_err_t spi_device_transmit(spi_device_handle_t handle, spi_transaction_t *trans_desc)
```

!!! summary "引数"
	- spi_device_handle_t `handle` Device handle obtained using spi_host_add_dev 
	- spi_transaction_t* `trans_desc` Description of transaction to execute 

!!! note "戻り値"
	esp_err_t



### spi_device_polling_start()
Immediately start a polling transaction.


```c
esp_err_t spi_device_polling_start(spi_device_handle_t handle, spi_transaction_t *trans_desc, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- spi_device_handle_t `handle` Device handle obtained using spi_host_add_dev 
	- spi_transaction_t* `trans_desc` Description of transaction to execute 
	- TickType_t `ticks_to_wait` Ticks to wait until there's room in the queue; currently only portMAX_DELAY is supported.

!!! note "戻り値"
	esp_err_t



### spi_device_polling_end()
Poll until the polling transaction ends.

This routine will not return until the transaction to the given device has succesfully completed. The task is not blocked, but actively busy-spins for the transaction to be completed.
```c
esp_err_t spi_device_polling_end(spi_device_handle_t handle, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- spi_device_handle_t `handle` Device handle obtained using spi_host_add_dev 
	- TickType_t `ticks_to_wait` Ticks to wait until there's a returned item; use portMAX_DELAY to never time out. 

!!! note "戻り値"
	esp_err_t



### spi_device_polling_transmit()
Send a polling transaction, wait for it to complete, and return the result

This function is the equivalent of calling  followed by . Do not use this when there is still a transaction that hasn't been finalized.
```c
esp_err_t spi_device_polling_transmit(spi_device_handle_t handle, spi_transaction_t *trans_desc)
```

!!! summary "引数"
	- spi_device_handle_t `handle` Device handle obtained using spi_host_add_dev 
	- spi_transaction_t* `trans_desc` Description of transaction to execute 

!!! note "戻り値"
	esp_err_t



### spi_device_acquire_bus()
Occupy the SPI bus for a device to do continuous transactions.

Transactions to all other devices will be put off until  is called.
```c
esp_err_t spi_device_acquire_bus(spi_device_handle_t device, TickType_t wait)
```

!!! summary "引数"
	- spi_device_handle_t `device` The device to occupy the bus. 
	- TickType_t `wait` Time to wait before the the bus is occupied by the device. Currently MUST set to portMAX_DELAY.

!!! note "戻り値"
	esp_err_t



### spi_device_release_bus()
Release the SPI bus occupied by the device. All other devices can start sending transactions.


```c
void spi_device_release_bus(spi_device_handle_t dev)
```

!!! summary "引数"
	- spi_device_handle_t `dev` The device to release the bus. 

!!! note "戻り値"
	void



### spi_cal_clock()
Calculate the working frequency that is most close to desired frequency, and also the register value.


```c
int spi_cal_clock(int fapb, int hz, int duty_cycle, uint32_t *reg_o)
```

!!! summary "引数"
	- int `fapb` The frequency of apb clock, should be . 
	- int `hz` Desired working frequency 
	- int `duty_cycle` Duty cycle of the spi clock 
	- uint32_t * `reg_o` Output of value to be set in clock register, or NULL if not needed. 

!!! note "戻り値"
	int Actual working frequency that most fit. 



### spi_get_timing()
Calculate the timing settings of specified frequency and settings.


```c
void spi_get_timing(bool gpio_is_used, int input_delay_ns, int eff_clk, int *dummy_o, int *cycles_remain_o)
```

!!! summary "引数"
	- bool `gpio_is_used` True if using GPIO matrix, or False if iomux pins are used. 
	- int `input_delay_ns` Input delay from SCLK launch edge to MISO data valid. 
	- int `eff_clk` Effective clock frequency (in Hz) from spi_cal_clock. 
	- int * `dummy_o` Address of dummy bits used output. Set to NULL if not needed. 
	- int * `cycles_remain_o` Address of cycles remaining (after dummy bits are used) output.


!!! note "戻り値"
	void



### spi_get_freq_limit()
Get the frequency limit of current configurations. SPI master working at this limit is OK, while above the limit, full duplex mode and DMA will not work, and dummy bits will be aplied in the half duplex mode.


```c
int spi_get_freq_limit(bool gpio_is_used, int input_delay_ns)
```

!!! summary "引数"
	- bool `gpio_is_used` True if using GPIO matrix, or False if native pins are used. 
	- int `input_delay_ns` Input delay from SCLK launch edge to MISO data valid. 

!!! note "戻り値"
	int Frequency limit of current configurations. 



