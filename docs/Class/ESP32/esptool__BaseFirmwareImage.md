# esptool::BaseFirmwareImage



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classesptool_1_1_base_firmware_image.html)

## メンバー

###  SEG_HEADER_LEN

```c
int esptool.BaseFirmwareImage::SEG_HEADER_LEN
```


###  SHA256_DIGEST_LEN

```c
int esptool.BaseFirmwareImage::SHA256_DIGEST_LEN
```


###  segments

```c
esptool.BaseFirmwareImage::segments
```


###  entrypoint

```c
esptool.BaseFirmwareImage::entrypoint
```


###  elf_sha256

```c
esptool.BaseFirmwareImage::elf_sha256
```


###  elf_sha256_offset

```c
esptool.BaseFirmwareImage::elf_sha256_offset
```


### __init__()



```c
def esptool.BaseFirmwareImage.__init__(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### load_common_header()



```c
def esptool.BaseFirmwareImage.load_common_header(self, load_file, expected_magic)
```

!!! summary "引数"
	- expected_magic `` 

!!! note "戻り値"
	def



### verify()



```c
def esptool.BaseFirmwareImage.verify(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### load_segment()


 
```c
def esptool.BaseFirmwareImage.load_segment(self, f, is_irom_segment=False)
```

!!! summary "引数"
	- is_irom_segment `` 

!!! note "戻り値"
	def



### warn_if_unusual_segment()



```c
def esptool.BaseFirmwareImage.warn_if_unusual_segment(self, offset, size, is_irom_segment)
```

!!! summary "引数"
	- is_irom_segment `` 

!!! note "戻り値"
	def



### maybe_patch_segment_data()


 
```c
def esptool.BaseFirmwareImage.maybe_patch_segment_data(self, f, segment_data)
```

!!! summary "引数"
	- segment_data `` 

!!! note "戻り値"
	def



### save_segment()


 
```c
def esptool.BaseFirmwareImage.save_segment(self, f, segment, checksum=None)
```

!!! summary "引数"
	- checksum `` 

!!! note "戻り値"
	def



### read_checksum()


 
```c
def esptool.BaseFirmwareImage.read_checksum(self, f)
```

!!! summary "引数"
	- f `` 

!!! note "戻り値"
	def



### calculate_checksum()


 
```c
def esptool.BaseFirmwareImage.calculate_checksum(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### append_checksum()


 
```c
def esptool.BaseFirmwareImage.append_checksum(self, f, checksum)
```

!!! summary "引数"
	- checksum `` 

!!! note "戻り値"
	def



### write_common_header()



```c
def esptool.BaseFirmwareImage.write_common_header(self, f, segments)
```

!!! summary "引数"
	- segments `` 

!!! note "戻り値"
	def



### is_irom_addr()


 
```c
def esptool.BaseFirmwareImage.is_irom_addr(self, addr)
```

!!! summary "引数"
	- addr `` 

!!! note "戻り値"
	def



### get_irom_segment()



```c
def esptool.BaseFirmwareImage.get_irom_segment(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### get_non_irom_segments()



```c
def esptool.BaseFirmwareImage.get_non_irom_segments(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



