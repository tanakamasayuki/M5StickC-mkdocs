# sdspi_host

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/sdspi_host.h>
```

上記宣言で利用できます。

## メンバー









### sdspi_host_init()
Initialize SD SPI driver




```c
esp_err_t sdspi_host_init()
```

!!! note "戻り値"
	esp_err_t



### sdspi_host_init_slot()
Initialize SD SPI driver for the specific SPI controller


```c
esp_err_t sdspi_host_init_slot(int slot, const sdspi_slot_config_t *slot_config)
```

!!! summary "引数"
	- int `slot` SPI controller to use (HSPI_HOST or VSPI_HOST) 
	- sdspi_slot_config_tconst  * `slot_config` pointer to slot configuration structure

!!! note "戻り値"
	esp_err_t



### sdspi_host_do_transaction()
Send command to the card and get response

This function returns when command is sent and response is received, or data is transferred, or timeout occurs.
```c
esp_err_t sdspi_host_do_transaction(int slot, sdmmc_command_t *cmdinfo)
```

!!! summary "引数"
	- int `slot` SPI controller (HSPI_HOST or VSPI_HOST) 
	- sdmmc_command_t* `cmdinfo` pointer to structure describing command and data to transfer 

!!! note "戻り値"
	esp_err_t



### sdspi_host_set_card_clk()
Set card clock frequency

Currently only integer fractions of 40MHz clock can be used. For High Speed cards, 40MHz can be used. For Default Speed cards, 20MHz can be used.
```c
esp_err_t sdspi_host_set_card_clk(int slot, uint32_t freq_khz)
```

!!! summary "引数"
	- int `slot` SPI controller (HSPI_HOST or VSPI_HOST) 
	- uint32_t `freq_khz` card clock frequency, in kHz 

!!! note "戻り値"
	esp_err_t



### sdspi_host_deinit()
Release resources allocated using sdspi_host_init




```c
esp_err_t sdspi_host_deinit()
```

!!! note "戻り値"
	esp_err_t



