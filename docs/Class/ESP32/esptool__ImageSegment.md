# esptool::ImageSegment



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classesptool_1_1_image_segment.html)

## メンバー

###  addr

```c
esptool.ImageSegment::addr
```


###  data

```c
esptool.ImageSegment::data
```


###  file_offs

```c
esptool.ImageSegment::file_offs
```


###  include_in_checksum

```c
esptool.ImageSegment::include_in_checksum
```


### __init__()



```c
def esptool.ImageSegment.__init__(self, addr, data, file_offs=None)
```

!!! summary "引数"
	- file_offs `` 

!!! note "戻り値"
	def



### copy_with_new_addr()


 
```c
def esptool.ImageSegment.copy_with_new_addr(self, new_addr)
```

!!! summary "引数"
	- new_addr `` 

!!! note "戻り値"
	def



### split_image()


 
```c
def esptool.ImageSegment.split_image(self, split_len)
```

!!! summary "引数"
	- split_len `` 

!!! note "戻り値"
	def



### __repr__()



```c
def esptool.ImageSegment.__repr__(self)
```

!!! summary "引数"
	- self `` 

!!! note "戻り値"
	def



### pad_to_alignment()



```c
def esptool.ImageSegment.pad_to_alignment(self, alignment)
```

!!! summary "引数"
	- alignment `` 

!!! note "戻り値"
	def



