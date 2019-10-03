# esptool::ESP32FirmwareImage



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classesptool_1_1_e_s_p32_firmware_image.html)

## メンバー

###  ROM_LOADER

```c
esptool.ESP32FirmwareImage::ROM_LOADER
```


###  WP_PIN_DISABLED

```c
int esptool.ESP32FirmwareImage::WP_PIN_DISABLED
```


###  EXTENDED_HEADER_STRUCT_FMT

```c
string esptool.ESP32FirmwareImage::EXTENDED_HEADER_STRUCT_FMT
```


###  IROM_ALIGN

```c
int esptool.ESP32FirmwareImage::IROM_ALIGN
```


###  secure_pad

```c
esptool.ESP32FirmwareImage::secure_pad
```


###  flash_mode

```c
esptool.ESP32FirmwareImage::flash_mode
```


###  flash_size_freq

```c
esptool.ESP32FirmwareImage::flash_size_freq
```


###  version

```c
esptool.ESP32FirmwareImage::version
```


###  wp_pin

```c
esptool.ESP32FirmwareImage::wp_pin
```


###  clk_drv

```c
esptool.ESP32FirmwareImage::clk_drv
```


###  q_drv

```c
esptool.ESP32FirmwareImage::q_drv
```


###  d_drv

```c
esptool.ESP32FirmwareImage::d_drv
```


###  cs_drv

```c
esptool.ESP32FirmwareImage::cs_drv
```


###  hd_drv

```c
esptool.ESP32FirmwareImage::hd_drv
```


###  wp_drv

```c
esptool.ESP32FirmwareImage::wp_drv
```


###  min_rev

```c
esptool.ESP32FirmwareImage::min_rev
```


###  append_digest

```c
esptool.ESP32FirmwareImage::append_digest
```


###  checksum

```c
esptool.ESP32FirmwareImage::checksum
```


###  stored_digest

```c
esptool.ESP32FirmwareImage::stored_digest
```


###  calc_digest

```c
esptool.ESP32FirmwareImage::calc_digest
```


###  IROM_ALIGN

```c
esptool.ESP32FirmwareImage::IROM_ALIGN
```


### __init__()



```c
def esptool.ESP32FirmwareImage.__init__(self, load_file=None)
```

!!! summary "引数"
	- load_file `` 

!!! note "戻り値"
	def



### is_flash_addr()



```c
def esptool.ESP32FirmwareImage.is_flash_addr(self, addr)
```

!!! summary "引数"
	- addr `` 

!!! note "戻り値"
	def



### default_output_name()


 
```c
def esptool.ESP32FirmwareImage.default_output_name(self, input_file)
```

!!! summary "引数"
	- input_file `` 

!!! note "戻り値"
	def



### warn_if_unusual_segment()



```c
def esptool.ESP32FirmwareImage.warn_if_unusual_segment(self, offset, size, is_irom_segment)
```

!!! summary "引数"
	- is_irom_segment `` 

!!! note "戻り値"
	def



### save()



```c
def esptool.ESP32FirmwareImage.save(self, filename)
```

!!! summary "引数"
	- filename `` 

!!! note "戻り値"
	def



### save_flash_segment()


 
```c
def esptool.ESP32FirmwareImage.save_flash_segment(self, f, segment, checksum=None)
```

!!! summary "引数"
	- checksum `` 

!!! note "戻り値"
	def



### load_extended_header()



```c
def esptool.ESP32FirmwareImage.load_extended_header(self, load_file)
```

!!! summary "引数"
	- load_file `` 

!!! note "戻り値"
	def



### save_extended_header()



```c
def esptool.ESP32FirmwareImage.save_extended_header(self, save_file)
```

!!! summary "引数"
	- save_file `` 

!!! note "戻り値"
	def



