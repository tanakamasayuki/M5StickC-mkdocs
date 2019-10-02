# esptool::ESPLoader



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classesptool_1_1_e_s_p_loader.html)

## メンバー

###  CHIP_NAME

```c
string esptool.ESPLoader::CHIP_NAME
```


###  IS_STUB

```c
bool esptool.ESPLoader::IS_STUB
```


###  DEFAULT_PORT

```c
string esptool.ESPLoader::DEFAULT_PORT
```


###  ESP_FLASH_BEGIN

```c
int esptool.ESPLoader::ESP_FLASH_BEGIN
```


###  ESP_FLASH_DATA

```c
int esptool.ESPLoader::ESP_FLASH_DATA
```


###  ESP_FLASH_END

```c
int esptool.ESPLoader::ESP_FLASH_END
```


###  ESP_MEM_BEGIN

```c
int esptool.ESPLoader::ESP_MEM_BEGIN
```


###  ESP_MEM_END

```c
int esptool.ESPLoader::ESP_MEM_END
```


###  ESP_MEM_DATA

```c
int esptool.ESPLoader::ESP_MEM_DATA
```


###  ESP_SYNC

```c
int esptool.ESPLoader::ESP_SYNC
```


###  ESP_WRITE_REG

```c
int esptool.ESPLoader::ESP_WRITE_REG
```


###  ESP_READ_REG

```c
int esptool.ESPLoader::ESP_READ_REG
```


###  ESP_SPI_SET_PARAMS

```c
int esptool.ESPLoader::ESP_SPI_SET_PARAMS
```


###  ESP_SPI_ATTACH

```c
int esptool.ESPLoader::ESP_SPI_ATTACH
```


###  ESP_CHANGE_BAUDRATE

```c
int esptool.ESPLoader::ESP_CHANGE_BAUDRATE
```


###  ESP_FLASH_DEFL_BEGIN

```c
int esptool.ESPLoader::ESP_FLASH_DEFL_BEGIN
```


###  ESP_FLASH_DEFL_DATA

```c
int esptool.ESPLoader::ESP_FLASH_DEFL_DATA
```


###  ESP_FLASH_DEFL_END

```c
int esptool.ESPLoader::ESP_FLASH_DEFL_END
```


###  ESP_SPI_FLASH_MD5

```c
int esptool.ESPLoader::ESP_SPI_FLASH_MD5
```


###  ESP_ERASE_FLASH

```c
int esptool.ESPLoader::ESP_ERASE_FLASH
```


###  ESP_ERASE_REGION

```c
int esptool.ESPLoader::ESP_ERASE_REGION
```


###  ESP_READ_FLASH

```c
int esptool.ESPLoader::ESP_READ_FLASH
```


###  ESP_RUN_USER_CODE

```c
int esptool.ESPLoader::ESP_RUN_USER_CODE
```


###  ESP_RAM_BLOCK

```c
int esptool.ESPLoader::ESP_RAM_BLOCK
```


###  FLASH_WRITE_SIZE

```c
int esptool.ESPLoader::FLASH_WRITE_SIZE
```


###  ESP_ROM_BAUD

```c
int esptool.ESPLoader::ESP_ROM_BAUD
```


###  ESP_IMAGE_MAGIC

```c
int esptool.ESPLoader::ESP_IMAGE_MAGIC
```


###  ESP_CHECKSUM_MAGIC

```c
int esptool.ESPLoader::ESP_CHECKSUM_MAGIC
```


###  FLASH_SECTOR_SIZE

```c
int esptool.ESPLoader::FLASH_SECTOR_SIZE
```


###  UART_DATA_REG_ADDR

```c
int esptool.ESPLoader::UART_DATA_REG_ADDR
```


###  IROM_MAP_START

```c
int esptool.ESPLoader::IROM_MAP_START
```


###  IROM_MAP_END

```c
int esptool.ESPLoader::IROM_MAP_END
```


###  STATUS_BYTES_LENGTH

```c
int esptool.ESPLoader::STATUS_BYTES_LENGTH
```


###  in_bootloader

```c
esptool.ESPLoader::in_bootloader
```


### __init__()


 
```c
def esptool.ESPLoader.__init__(self, port=DEFAULT_PORT, baud=ESP_ROM_BAUD, trace_enabled=False)
```

!!! summary "引数"
	- trace_enabled `` 

!!! note "戻り値"
	def



### read()



```c
def esptool.ESPLoader.read(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### write()



```c
def esptool.ESPLoader.write(self, packet)
```

!!! summary "引数"
	- packet `` 

!!! note "戻り値"
	def



### trace()



```c
def esptool.ESPLoader.trace(self, message, *format_args)
```

!!! summary "引数"
	- message `` 
	- * `format_args` 

!!! note "戻り値"
	def



### command()



```c
def esptool.ESPLoader.command(self, op=None, data=b"", chk=0, wait_response=True, timeout=DEFAULT_TIMEOUT)
```

!!! summary "引数"
	- timeout `` 

!!! note "戻り値"
	def



### check_command()


 
```c
def esptool.ESPLoader.check_command(self, op_description, op=None, data=b'', chk=0, timeout=DEFAULT_TIMEOUT)
```

!!! summary "引数"
	- timeout `` 

!!! note "戻り値"
	def



### flush_input()



```c
def esptool.ESPLoader.flush_input(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### sync()



```c
def esptool.ESPLoader.sync(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### connect()


 
```c
def esptool.ESPLoader.connect(self, mode='default_reset')
```

!!! summary "引数"
	- mode `` 

!!! note "戻り値"
	def



### read_reg()



```c
def esptool.ESPLoader.read_reg(self, addr)
```

!!! summary "引数"
	- addr `` 

!!! note "戻り値"
	def



### write_reg()



```c
def esptool.ESPLoader.write_reg(self, addr, value, mask=0xFFFFFFFF, delay_us=0)
```

!!! summary "引数"
	- delay_us `` 

!!! note "戻り値"
	def



### mem_begin()



```c
def esptool.ESPLoader.mem_begin(self, size, blocks, blocksize, offset)
```

!!! summary "引数"
	- offset `` 

!!! note "戻り値"
	def



### mem_block()



```c
def esptool.ESPLoader.mem_block(self, data, seq)
```

!!! summary "引数"
	- seq `` 

!!! note "戻り値"
	def



### mem_finish()



```c
def esptool.ESPLoader.mem_finish(self, entrypoint=0)
```

!!! summary "引数"
	- entrypoint `` 

!!! note "戻り値"
	def



### flash_begin()



```c
def esptool.ESPLoader.flash_begin(self, size, offset)
```

!!! summary "引数"
	- offset `` 

!!! note "戻り値"
	def



### flash_block()



```c
def esptool.ESPLoader.flash_block(self, data, seq, timeout=DEFAULT_TIMEOUT)
```

!!! summary "引数"
	- timeout `` 

!!! note "戻り値"
	def



### flash_finish()



```c
def esptool.ESPLoader.flash_finish(self, reboot=False)
```

!!! summary "引数"
	- reboot `` 

!!! note "戻り値"
	def



### run()



```c
def esptool.ESPLoader.run(self, reboot=False)
```

!!! summary "引数"
	- reboot `` 

!!! note "戻り値"
	def



### flash_id()



```c
def esptool.ESPLoader.flash_id(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### parse_flash_size_arg()



```c
def esptool.ESPLoader.parse_flash_size_arg(self, arg)
```

!!! summary "引数"
	- arg `` 

!!! note "戻り値"
	def



### run_stub()



```c
def esptool.ESPLoader.run_stub(self, stub=None)
```

!!! summary "引数"
	- stub `` 

!!! note "戻り値"
	def



### flash_defl_begin()


 
```c
def esptool.ESPLoader.flash_defl_begin(self, size, compsize, offset)
```

!!! summary "引数"
	- offset `` 

!!! note "戻り値"
	def



### flash_defl_block()



```c
def esptool.ESPLoader.flash_defl_block(self, data, seq, timeout=DEFAULT_TIMEOUT)
```

!!! summary "引数"
	- timeout `` 

!!! note "戻り値"
	def



### flash_defl_finish()



```c
def esptool.ESPLoader.flash_defl_finish(self, reboot=False)
```

!!! summary "引数"
	- reboot `` 

!!! note "戻り値"
	def



### flash_md5sum()



```c
def esptool.ESPLoader.flash_md5sum(self, addr, size)
```

!!! summary "引数"
	- size `` 

!!! note "戻り値"
	def



### change_baud()



```c
def esptool.ESPLoader.change_baud(self, baud)
```

!!! summary "引数"
	- baud `` 

!!! note "戻り値"
	def



### erase_flash()



```c
def esptool.ESPLoader.erase_flash(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### erase_region()



```c
def esptool.ESPLoader.erase_region(self, offset, size)
```

!!! summary "引数"
	- size `` 

!!! note "戻り値"
	def



### read_flash()



```c
def esptool.ESPLoader.read_flash(self, offset, length, progress_fn=None)
```

!!! summary "引数"
	- progress_fn `` 

!!! note "戻り値"
	def



### flash_spi_attach()


 
```c
def esptool.ESPLoader.flash_spi_attach(self, hspi_arg)
```

!!! summary "引数"
	- hspi_arg `` 

!!! note "戻り値"
	def



### flash_set_parameters()


 
```c
def esptool.ESPLoader.flash_set_parameters(self, size)
```

!!! summary "引数"
	- size `` 

!!! note "戻り値"
	def



### run_spiflash_command()


 
```c
def esptool.ESPLoader.run_spiflash_command(self, spiflash_command, data=b"", read_bits=0)
```

!!! summary "引数"
	- read_bits `` 

!!! note "戻り値"
	def



### read_status()


 
```c
def esptool.ESPLoader.read_status(self, num_bytes=2)
```

!!! summary "引数"
	- num_bytes `` 

!!! note "戻り値"
	def



### write_status()


 
```c
def esptool.ESPLoader.write_status(self, new_status, num_bytes=2, set_non_volatile=False)
```

!!! summary "引数"
	- set_non_volatile `` 

!!! note "戻り値"
	def



### hard_reset()



```c
def esptool.ESPLoader.hard_reset(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### soft_reset()



```c
def esptool.ESPLoader.soft_reset(self, stay_in_bootloader)
```

!!! summary "引数"
	- stay_in_bootloader `` 

!!! note "戻り値"
	def



### detect_chip()


 
```c
def esptool.ESPLoader.detect_chip(port=DEFAULT_PORT, baud=ESP_ROM_BAUD, connect_mode='default_reset', trace_enabled=False)
```

!!! summary "引数"
	- trace_enabled `` 

!!! note "戻り値"
	def



### checksum()



```c
def esptool.ESPLoader.checksum(data, state=ESP_CHECKSUM_MAGIC)
```

!!! summary "引数"
	- state `` 

!!! note "戻り値"
	def



