# sdmmc_host

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/sdmmc_host.h>
```

上記宣言で利用できます。

## メンバー

















### sdmmc_host_init()
Initialize SDMMC host peripheral




```c
esp_err_t sdmmc_host_init()
```

!!! note "戻り値"
	esp_err_t



### sdmmc_host_init_slot()
Initialize given slot of SDMMC peripheral

Card detect and write protect signals can be routed to arbitrary GPIOs using GPIO matrix.
```c
esp_err_t sdmmc_host_init_slot(int slot, const sdmmc_slot_config_t *slot_config)
```

!!! summary "引数"
	- int `slot` slot number (SDMMC_HOST_SLOT_0 or SDMMC_HOST_SLOT_1) 
	- sdmmc_slot_config_tconst  * `slot_config` additional configuration for the slot 

!!! note "戻り値"
	esp_err_t



### sdmmc_host_set_bus_width()
Select bus width to be used for data transfer

SD/MMC card must be initialized prior to this command, and a command to set bus width has to be sent to the card (e.g. SD_APP_SET_BUS_WIDTH)
```c
esp_err_t sdmmc_host_set_bus_width(int slot, size_t width)
```

!!! summary "引数"
	- int `slot` slot number (SDMMC_HOST_SLOT_0 or SDMMC_HOST_SLOT_1) 
	- size_t `width` bus width (1, 4, or 8 for slot 0; 1 or 4 for slot 1) 

!!! note "戻り値"
	esp_err_t



### sdmmc_host_get_slot_width()
Get bus width configured in  to be used for data transfer


```c
size_t sdmmc_host_get_slot_width(int slot)
```

!!! summary "引数"
	- int `slot` slot number (SDMMC_HOST_SLOT_0 or SDMMC_HOST_SLOT_1) 

!!! note "戻り値"
	size_t configured bus width of the specified slot. 



### sdmmc_host_set_card_clk()
Set card clock frequency

Currently only integer fractions of 40MHz clock can be used. For High Speed cards, 40MHz can be used. For Default Speed cards, 20MHz can be used.
```c
esp_err_t sdmmc_host_set_card_clk(int slot, uint32_t freq_khz)
```

!!! summary "引数"
	- int `slot` slot number (SDMMC_HOST_SLOT_0 or SDMMC_HOST_SLOT_1) 
	- uint32_t `freq_khz` card clock frequency, in kHz 

!!! note "戻り値"
	esp_err_t



### sdmmc_host_set_bus_ddr_mode()
Enable or disable DDR mode of SD interface


```c
esp_err_t sdmmc_host_set_bus_ddr_mode(int slot, bool ddr_enabled)
```

!!! summary "引数"
	- int `slot` slot number (SDMMC_HOST_SLOT_0 or SDMMC_HOST_SLOT_1) 
	- bool `ddr_enabled` enable or disable DDR mode 

!!! note "戻り値"
	esp_err_t 




### sdmmc_host_do_transaction()
Send command to the card and get response

This function returns when command is sent and response is received, or data is transferred, or timeout occurs.
```c
esp_err_t sdmmc_host_do_transaction(int slot, sdmmc_command_t *cmdinfo)
```

!!! summary "引数"
	- int `slot` slot number (SDMMC_HOST_SLOT_0 or SDMMC_HOST_SLOT_1) 
	- sdmmc_command_t* `cmdinfo` pointer to structure describing command and data to transfer 

!!! note "戻り値"
	esp_err_t



### sdmmc_host_io_int_enable()
Enable IO interrupts

This function configures the host to accept SDIO interrupts.
```c
esp_err_t sdmmc_host_io_int_enable(int slot)
```

!!! summary "引数"
	- int `slot` slot number (SDMMC_HOST_SLOT_0 or SDMMC_HOST_SLOT_1) 

!!! note "戻り値"
	esp_err_t



### sdmmc_host_io_int_wait()
Block until an SDIO interrupt is received, or timeout occurs


```c
esp_err_t sdmmc_host_io_int_wait(int slot, TickType_t timeout_ticks)
```

!!! summary "引数"
	- int `slot` slot number (SDMMC_HOST_SLOT_0 or SDMMC_HOST_SLOT_1) 
	- TickType_t `timeout_ticks` number of RTOS ticks to wait for the interrupt 

!!! note "戻り値"
	esp_err_t 




### sdmmc_host_deinit()
Disable SDMMC host and release allocated resources




```c
esp_err_t sdmmc_host_deinit()
```

!!! note "戻り値"
	esp_err_t



### sdmmc_host_pullup_en()
Enable the pull-ups of sd pins.


```c
esp_err_t sdmmc_host_pullup_en(int slot, int width)
```

!!! summary "引数"
	- int `slot` Slot to use, normally set it to 1. 
	- int `width` Bit width of your configuration, 1 or 4.

!!! note "戻り値"
	esp_err_t



