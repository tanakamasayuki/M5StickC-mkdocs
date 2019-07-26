# spi_common

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/spi_common.h>
```

上記宣言で利用できます。

## メンバー





























### spicommon_periph_claim()
Try to claim a SPI peripheral

Call this if your driver wants to manage a SPI peripheral.
```c
bool spicommon_periph_claim(spi_host_device_t host)
```

!!! summary "引数"
	- spi_host_device_t `host` Peripheral to claim 

!!! note "戻り値"
	bool



### spicommon_periph_free()
Return the SPI peripheral so another driver can claim it.


```c
bool spicommon_periph_free(spi_host_device_t host)
```

!!! summary "引数"
	- spi_host_device_t `host` Peripheral to return 

!!! note "戻り値"
	bool True if peripheral is returned successfully; false if peripheral was free to claim already. 



### spicommon_dma_chan_claim()
Try to claim a SPI DMA channel

Call this if your driver wants to use SPI with a DMA channnel.
```c
bool spicommon_dma_chan_claim(int dma_chan)
```

!!! summary "引数"
	- int `dma_chan` channel to claim

!!! note "戻り値"
	bool



### spicommon_dma_chan_free()
Return the SPI DMA channel so other driver can claim it, or just to power down DMA.


```c
bool spicommon_dma_chan_free(int dma_chan)
```

!!! summary "引数"
	- int `dma_chan` channel to return

!!! note "戻り値"
	bool True if success; false otherwise. 



### spicommon_bus_initialize_io()
Connect a SPI peripheral to GPIO pins

This routine is used to connect a SPI peripheral to the IO-pads and DMA channel given in the arguments. Depending on the IO-pads requested, the routing is done either using the IO_mux or using the GPIO matrix.
```c
esp_err_t spicommon_bus_initialize_io(spi_host_device_t host, const spi_bus_config_t *bus_config, int dma_chan, uint32_t flags, uint32_t *flags_o)
```

!!! summary "引数"
	- spi_host_device_t `host` SPI peripheral to be routed 
	- spi_bus_config_tconst  * `bus_config` Pointer to a spi_bus_config struct detailing the GPIO pins 
	- int `dma_chan` DMA-channel (1 or 2) to use, or 0 for no DMA. 
	- uint32_t `flags` Combination of SPICOMMON_BUSFLAG_* flags, set to ensure the pins set are capable with some functions:

	- uint32_t * `flags_o` A SPICOMMON_BUSFLAG_* flag combination of bus abilities will be written to this address. Leave to NULL if not needed.


!!! note "戻り値"
	esp_err_t



### spicommon_bus_free_io()
Free the IO used by a SPI peripheral


```c
esp_err_t spicommon_bus_free_io(spi_host_device_t host) __attribute__((deprecated))
```

!!! summary "引数"
	- spi_host_device_t `host` SPI peripheral to be freed

!!! note "戻り値"
	esp_err_t



### spicommon_bus_free_io_cfg()
Free the IO used by a SPI peripheral


```c
esp_err_t spicommon_bus_free_io_cfg(const spi_bus_config_t *bus_cfg)
```

!!! summary "引数"
	- spi_bus_config_tconst  * `bus_cfg` Bus config struct which defines which pins to be used.

!!! note "戻り値"
	esp_err_t 




### spicommon_cs_initialize()
Initialize a Chip Select pin for a specific SPI peripheral


```c
void spicommon_cs_initialize(spi_host_device_t host, int cs_io_num, int cs_num, int force_gpio_matrix)
```

!!! summary "引数"
	- spi_host_device_t `host` SPI peripheral 
	- int `cs_io_num` GPIO pin to route 
	- int `cs_num` CS id to route 
	- int `force_gpio_matrix` If true, CS will always be routed through the GPIO matrix. If false, if the GPIO number allows it, the routing will happen through the IO_mux. 

!!! note "戻り値"
	void



### spicommon_cs_free()
Free a chip select line


```c
void spicommon_cs_free(spi_host_device_t host, int cs_num) __attribute__((deprecated))
```

!!! summary "引数"
	- spi_host_device_t `host` SPI peripheral 
	- int `cs_num` CS id to free 

!!! note "戻り値"
	void



### spicommon_cs_free_io()
Free a chip select line


```c
void spicommon_cs_free_io(int cs_gpio_num)
```

!!! summary "引数"
	- int `cs_gpio_num` CS gpio num to free 

!!! note "戻り値"
	void



### spicommon_setup_dma_desc_links()
Setup a DMA link chain

This routine will set up a chain of linked DMA descriptors in the array pointed to by . Enough DMA descriptors will be used to fit the buffer of  bytes in, and the descriptors will point to the corresponding positions in  and linked together. The end result is that feeding  into DMA hardware results in the entirety  bytes of  being read or written.
```c
void spicommon_setup_dma_desc_links(lldesc_t *dmadesc, int len, const uint8_t *data, bool isrx)
```

!!! summary "引数"
	- lldesc_t * `dmadesc` Pointer to array of DMA descriptors big enough to be able to convey  bytes 
	- int `len` Length of buffer 
	- const uint8_t * `data` Data buffer to use for DMA transfer 
	- bool `isrx` True if data is to be written into , false if it's to be read from . 

!!! note "戻り値"
	void



### spicommon_hw_for_host()
Get the position of the hardware registers for a specific SPI host


```c
spi_dev_t* spicommon_hw_for_host(spi_host_device_t host)
```

!!! summary "引数"
	- spi_host_device_t `host` The SPI host

!!! note "戻り値"
	spi_dev_t * A register descriptor stuct pointer, pointed at the hardware registers 



### spicommon_irqsource_for_host()
Get the IRQ source for a specific SPI host


```c
int spicommon_irqsource_for_host(spi_host_device_t host)
```

!!! summary "引数"
	- spi_host_device_t `host` The SPI host

!!! note "戻り値"
	int The hosts IRQ source 



### spicommon_dmaworkaround_req_reset()
Request a reset for a certain DMA channel


Essentially, when a reset is needed, a driver can request this using spicommon_dmaworkaround_req_reset. This is supposed to be called with an user-supplied function as an argument. If both DMA channels are idle, this call will reset the DMA subsystem and return true. If the other DMA channel is still busy, it will return false; as soon as the other DMA channel is done, however, it will reset the DMA subsystem and call the callback. The callback is then supposed to be used to continue the SPI drivers activity.
```c
bool spicommon_dmaworkaround_req_reset(int dmachan, dmaworkaround_cb_t cb, void *arg)
```

!!! summary "引数"
	- int `dmachan` DMA channel associated with the SPI host that needs a reset 
	- dmaworkaround_cb_t `cb` Callback to call in case DMA channel cannot be reset immediately 
	- void * `arg` Argument to the callback

!!! note "戻り値"
	bool



### spicommon_dmaworkaround_reset_in_progress()
Check if a DMA reset is requested but has not completed yet



```c
bool spicommon_dmaworkaround_reset_in_progress()
```

!!! note "戻り値"
	bool True when a DMA reset is requested but hasn't completed yet. False otherwise. 



### spicommon_dmaworkaround_idle()
Mark a DMA channel as idle.

A call to this function tells the workaround logic that this channel will not be affected by a global SPI DMA reset. 
```c
void spicommon_dmaworkaround_idle(int dmachan)
```

!!! summary "引数"
	- int `dmachan` 

!!! note "戻り値"
	void



### spicommon_dmaworkaround_transfer_active()
Mark a DMA channel as active.

A call to this function tells the workaround logic that this channel will be affected by a global SPI DMA reset, and a reset like that should not be attempted. 
```c
void spicommon_dmaworkaround_transfer_active(int dmachan)
```

!!! summary "引数"
	- int `dmachan` 

!!! note "戻り値"
	void



