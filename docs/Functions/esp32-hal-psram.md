# PSRAM(psram)

M5StickCはPSRAMを搭載していません。

## メンバー

### psramInit()



```c
bool psramInit()
```

!!! note "戻り値"
	bool



### psramFound()



```c
bool psramFound()
```

!!! note "戻り値"
	bool



### ps_malloc()



```c
void* ps_malloc(size_t size)
```

!!! summary "引数"
	- size_t `size` 

!!! note "戻り値"
	void *



### ps_calloc()



```c
void* ps_calloc(size_t n, size_t size)
```

!!! summary "引数"
	- size_t `n` 
	- size_t `size` 

!!! note "戻り値"
	void *



### ps_realloc()



```c
void* ps_realloc(void *ptr, size_t size)
```

!!! summary "引数"
	- void * `ptr` 
	- size_t `size` 

!!! note "戻り値"
	void *



