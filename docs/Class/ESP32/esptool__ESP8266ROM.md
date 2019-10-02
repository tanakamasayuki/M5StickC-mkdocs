# esptool::ESP8266ROM



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classesptool_1_1_e_s_p8266_r_o_m.html)

## メンバー

###  CHIP_NAME

```c
string esptool.ESP8266ROM::CHIP_NAME
```


###  IS_STUB

```c
bool esptool.ESP8266ROM::IS_STUB
```


###  DATE_REG_VALUE

```c
int esptool.ESP8266ROM::DATE_REG_VALUE
```


###  ESP_OTP_MAC0

```c
int esptool.ESP8266ROM::ESP_OTP_MAC0
```


###  ESP_OTP_MAC1

```c
int esptool.ESP8266ROM::ESP_OTP_MAC1
```


###  ESP_OTP_MAC3

```c
int esptool.ESP8266ROM::ESP_OTP_MAC3
```


###  SPI_REG_BASE

```c
int esptool.ESP8266ROM::SPI_REG_BASE
```


###  SPI_W0_OFFS

```c
int esptool.ESP8266ROM::SPI_W0_OFFS
```


###  SPI_HAS_MOSI_DLEN_REG

```c
bool esptool.ESP8266ROM::SPI_HAS_MOSI_DLEN_REG
```


###  FLASH_SIZES

```c
dictionary esptool.ESP8266ROM::FLASH_SIZES
```


###  BOOTLOADER_FLASH_OFFSET

```c
int esptool.ESP8266ROM::BOOTLOADER_FLASH_OFFSET
```


### get_efuses()



```c
def esptool.ESP8266ROM.get_efuses(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### get_chip_description()



```c
def esptool.ESP8266ROM.get_chip_description(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### get_chip_features()



```c
def esptool.ESP8266ROM.get_chip_features(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### flash_spi_attach()


 
```c
def esptool.ESP8266ROM.flash_spi_attach(self, hspi_arg)
```

!!! summary "引数"
	- hspi_arg `` 

!!! note "戻り値"
	def



### flash_set_parameters()


 
```c
def esptool.ESP8266ROM.flash_set_parameters(self, size)
```

!!! summary "引数"
	- size `` 

!!! note "戻り値"
	def



### chip_id()


 
```c
def esptool.ESP8266ROM.chip_id(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### read_mac()


 
```c
def esptool.ESP8266ROM.read_mac(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### get_erase_size()


 
```c
def esptool.ESP8266ROM.get_erase_size(self, offset, size)
```

!!! summary "引数"
	- size `` 

!!! note "戻り値"
	def



### override_vddsdio()



```c
def esptool.ESP8266ROM.override_vddsdio(self, new_voltage)
```

!!! summary "引数"
	- new_voltage `` 

!!! note "戻り値"
	def



