# fs::SDMMCFS



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classfs_1_1_s_d_m_m_c_f_s.html)

## メンバー

### SDMMCFS()



```c
SDMMCFS::SDMMCFS(FSImplPtr impl)
```

!!! summary "引数"
	- FSImplPtr `impl` 



### begin()



```c
bool SDMMCFS::begin(const char *mountpoint="/sdcard", bool mode1bit=false)
```

!!! summary "引数"
	- constchar * `mountpoint` 
	- bool `mode1bit` 

!!! note "戻り値"
	bool



### end()



```c
void SDMMCFS::end()
```



### cardType()



```c
sdcard_type_t SDMMCFS::cardType()
```

!!! note "戻り値"
	sdcard_type_t



### cardSize()



```c
uint64_t SDMMCFS::cardSize()
```

!!! note "戻り値"
	uint64_t



### totalBytes()



```c
uint64_t SDMMCFS::totalBytes()
```

!!! note "戻り値"
	uint64_t



### usedBytes()



```c
uint64_t SDMMCFS::usedBytes()
```

!!! note "戻り値"
	uint64_t



