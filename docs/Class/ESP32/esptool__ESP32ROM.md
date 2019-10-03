# esptool::ESP32ROM



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classesptool_1_1_e_s_p32_r_o_m.html)

## メンバー

###  CHIP_NAME

```c
string esptool.ESP32ROM::CHIP_NAME
```


###  IMAGE_CHIP_ID

```c
int esptool.ESP32ROM::IMAGE_CHIP_ID
```


###  IS_STUB

```c
bool esptool.ESP32ROM::IS_STUB
```


###  DATE_REG_VALUE

```c
int esptool.ESP32ROM::DATE_REG_VALUE
```


###  IROM_MAP_START

```c
int esptool.ESP32ROM::IROM_MAP_START
```


###  IROM_MAP_END

```c
int esptool.ESP32ROM::IROM_MAP_END
```


###  DROM_MAP_START

```c
int esptool.ESP32ROM::DROM_MAP_START
```


###  DROM_MAP_END

```c
int esptool.ESP32ROM::DROM_MAP_END
```


###  STATUS_BYTES_LENGTH

```c
int esptool.ESP32ROM::STATUS_BYTES_LENGTH
```


###  SPI_REG_BASE

```c
int esptool.ESP32ROM::SPI_REG_BASE
```


###  EFUSE_REG_BASE

```c
int esptool.ESP32ROM::EFUSE_REG_BASE
```


###  DR_REG_SYSCON_BASE

```c
int esptool.ESP32ROM::DR_REG_SYSCON_BASE
```


###  SPI_W0_OFFS

```c
int esptool.ESP32ROM::SPI_W0_OFFS
```


###  SPI_HAS_MOSI_DLEN_REG

```c
bool esptool.ESP32ROM::SPI_HAS_MOSI_DLEN_REG
```


###  UART_CLKDIV_REG

```c
int esptool.ESP32ROM::UART_CLKDIV_REG
```


###  XTAL_CLK_DIVIDER

```c
int esptool.ESP32ROM::XTAL_CLK_DIVIDER
```


###  FLASH_SIZES

```c
dictionary esptool.ESP32ROM::FLASH_SIZES
```


###  BOOTLOADER_FLASH_OFFSET

```c
int esptool.ESP32ROM::BOOTLOADER_FLASH_OFFSET
```


###  OVERRIDE_VDDSDIO_CHOICES

```c
list esptool.ESP32ROM::OVERRIDE_VDDSDIO_CHOICES
```


###  MEMORY_MAP

```c
list esptool.ESP32ROM::MEMORY_MAP
```


### is_flash_encryption_key_valid()


 
```c
def esptool.ESP32ROM.is_flash_encryption_key_valid(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### get_flash_crypt_config()


 
```c
def esptool.ESP32ROM.get_flash_crypt_config(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### get_chip_description()



```c
def esptool.ESP32ROM.get_chip_description(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### get_chip_features()



```c
def esptool.ESP32ROM.get_chip_features(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### read_efuse()


 
```c
def esptool.ESP32ROM.read_efuse(self, n)
```

!!! summary "引数"
	- n `` 

!!! note "戻り値"
	def



### chip_id()



```c
def esptool.ESP32ROM.chip_id(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### read_mac()


 
```c
def esptool.ESP32ROM.read_mac(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### get_erase_size()



```c
def esptool.ESP32ROM.get_erase_size(self, offset, size)
```

!!! summary "引数"
	- size `` 

!!! note "戻り値"
	def



### override_vddsdio()



```c
def esptool.ESP32ROM.override_vddsdio(self, new_voltage)
```

!!! summary "引数"
	- new_voltage `` 

!!! note "戻り値"
	def



