# fs::SDFS



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classfs_1_1_s_d_f_s.html)

## メンバー

### SDFS()



```c
SDFS::SDFS(FSImplPtr impl)
```

!!! summary "引数"
	- FSImplPtr `impl` 



### begin()



```c
bool SDFS::begin(uint8_t ssPin=SS, SPIClass &spi=SPI, uint32_t frequency=4000000, const char *mountpoint="/sd", uint8_t max_files=5)
```

!!! summary "引数"
	- uint8_t `ssPin` 
	- SPIClass& `spi` 
	- uint32_t `frequency` 
	- constchar * `mountpoint` 
	- uint8_t `max_files` 

!!! note "戻り値"
	bool



### end()



```c
void SDFS::end()
```



### cardType()



```c
sdcard_type_t SDFS::cardType()
```

!!! note "戻り値"
	sdcard_type_t



### cardSize()



```c
uint64_t SDFS::cardSize()
```

!!! note "戻り値"
	uint64_t



### totalBytes()



```c
uint64_t SDFS::totalBytes()
```

!!! note "戻り値"
	uint64_t



### usedBytes()



```c
uint64_t SDFS::usedBytes()
```

!!! note "戻り値"
	uint64_t



