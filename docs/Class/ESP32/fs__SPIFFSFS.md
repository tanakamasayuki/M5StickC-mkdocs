# fs::SPIFFSFS



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classfs_1_1_s_p_i_f_f_s_f_s.html)

## メンバー

### SPIFFSFS()



```c
SPIFFSFS::SPIFFSFS()
```



### begin()



```c
bool SPIFFSFS::begin(bool formatOnFail=false, const char *basePath="/spiffs", uint8_t maxOpenFiles=10)
```

!!! summary "引数"
	- bool `formatOnFail` 
	- constchar * `basePath` 
	- uint8_t `maxOpenFiles` 

!!! note "戻り値"
	bool



### format()



```c
bool SPIFFSFS::format()
```

!!! note "戻り値"
	bool



### totalBytes()



```c
size_t SPIFFSFS::totalBytes()
```

!!! note "戻り値"
	size_t



### usedBytes()



```c
size_t SPIFFSFS::usedBytes()
```

!!! note "戻り値"
	size_t



### end()



```c
void SPIFFSFS::end()
```



