# CPU

CPUクロックなどの変更が可能です。

## メンバー





### addApbChangeCallback()



```c
bool addApbChangeCallback(void *arg, apb_change_cb_t cb)
```

!!! summary "引数"
	- void * `arg` 
	- apb_change_cb_t `cb` 

!!! note "戻り値"
	bool



### removeApbChangeCallback()



```c
bool removeApbChangeCallback(void *arg, apb_change_cb_t cb)
```

!!! summary "引数"
	- void * `arg` 
	- apb_change_cb_t `cb` 

!!! note "戻り値"
	bool



### setCpuFrequencyMhz()



```c
bool setCpuFrequencyMhz(uint32_t cpu_freq_mhz)
```

!!! summary "引数"
	- uint32_t `cpu_freq_mhz` 

!!! note "戻り値"
	bool



### getCpuFrequencyMhz()



```c
uint32_t getCpuFrequencyMhz()
```

!!! note "戻り値"
	uint32_t



### getXtalFrequencyMhz()



```c
uint32_t getXtalFrequencyMhz()
```

!!! note "戻り値"
	uint32_t



### getApbFrequency()



```c
uint32_t getApbFrequency()
```

!!! note "戻り値"
	uint32_t



