# spi_slave

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/spi_slave.h>
```

上記宣言で利用できます。

## メンバー











### spi_slave_initialize()
Initialize a SPI bus as a slave interface


```c
esp_err_t spi_slave_initialize(spi_host_device_t host, const spi_bus_config_t *bus_config, const spi_slave_interface_config_t *slave_config, int dma_chan)
```

!!! summary "引数"
	- spi_host_device_t `host` SPI peripheral to use as a SPI slave interface 
	- spi_bus_config_tconst  * `bus_config` Pointer to a  struct specifying how the host should be initialized 
	- spi_slave_interface_config_tconst  * `slave_config` Pointer to a  struct specifying the details for the slave interface 
	- int `dma_chan` Either 1 or 2. A SPI bus used by this driver must have a DMA channel associated with it. The SPI hardware has two DMA channels to share. This parameter indicates which one to use.

!!! note "戻り値"
	esp_err_t



### spi_slave_free()
Free a SPI bus claimed as a SPI slave interface


```c
esp_err_t spi_slave_free(spi_host_device_t host)
```

!!! summary "引数"
	- spi_host_device_t `host` SPI peripheral to free 

!!! note "戻り値"
	esp_err_t 




### spi_slave_queue_trans()
Queue a SPI transaction for execution

This function hands over ownership of the buffers in  to the SPI slave driver; the application is not to access this memory until  is called to hand ownership back to the application.
```c
esp_err_t spi_slave_queue_trans(spi_host_device_t host, const spi_slave_transaction_t *trans_desc, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- spi_host_device_t `host` SPI peripheral that is acting as a slave 
	- spi_slave_transaction_tconst  * `trans_desc` Description of transaction to execute. Not const because we may want to write status back into the transaction description. 
	- TickType_t `ticks_to_wait` Ticks to wait until there's room in the queue; use portMAX_DELAY to never time out. 

!!! note "戻り値"
	esp_err_t



### spi_slave_get_trans_result()
Get the result of a SPI transaction queued earlier

It is mandatory to eventually use this function for any transaction queued by .
```c
esp_err_t spi_slave_get_trans_result(spi_host_device_t host, spi_slave_transaction_t **trans_desc, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- spi_host_device_t `host` SPI peripheral to that is acting as a slave 
	- spi_slave_transaction_t** `trans_desc` Pointer to variable able to contain a pointer to the description of the transaction that is executed 
	- TickType_t `ticks_to_wait` Ticks to wait until there's a returned item; use portMAX_DELAY to never time out. 

!!! note "戻り値"
	esp_err_t



### spi_slave_transmit()
Do a SPI transaction

Essentially does the same as spi_slave_queue_trans followed by spi_slave_get_trans_result. Do not use this when there is still a transaction queued that hasn't been finalized using spi_slave_get_trans_result.
```c
esp_err_t spi_slave_transmit(spi_host_device_t host, spi_slave_transaction_t *trans_desc, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- spi_host_device_t `host` SPI peripheral to that is acting as a slave 
	- spi_slave_transaction_t* `trans_desc` Pointer to variable able to contain a pointer to the description of the transaction that is executed. Not const because we may want to write status back into the transaction description. 
	- TickType_t `ticks_to_wait` Ticks to wait until there's a returned item; use portMAX_DELAY to never time out. 

!!! note "戻り値"
	esp_err_t



