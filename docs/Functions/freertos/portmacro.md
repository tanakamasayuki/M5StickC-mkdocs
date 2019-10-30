# portmacro



## メンバー































































































### vPortAssertIfInISR()



```c
void vPortAssertIfInISR()
```

!!! note "戻り値"
	void



### vPortCPUInitializeMutex()



```c
void vPortCPUInitializeMutex(portMUX_TYPE *mux)
```

!!! summary "引数"
	- portMUX_TYPE* `mux` 

!!! note "戻り値"
	void



### vTaskExitCritical()



```c
void vTaskExitCritical(portMUX_TYPE *mux)
```

!!! summary "引数"
	- portMUX_TYPE* `mux` 

!!! note "戻り値"
	void



### vTaskEnterCritical()



```c
void vTaskEnterCritical(portMUX_TYPE *mux)
```

!!! summary "引数"
	- portMUX_TYPE* `mux` 

!!! note "戻り値"
	void



### vPortCPUAcquireMutex()



```c
void vPortCPUAcquireMutex(portMUX_TYPE *mux)
```

!!! summary "引数"
	- portMUX_TYPE* `mux` 

!!! note "戻り値"
	void



### vPortCPUAcquireMutexTimeout()
Acquire a portmux spinlock with a timeout


```c
bool vPortCPUAcquireMutexTimeout(portMUX_TYPE *mux, int timeout_cycles)
```

!!! summary "引数"
	- portMUX_TYPE* `mux` Pointer to portmux to acquire. 
	- int `timeout_cycles` Timeout to spin, in CPU cycles. Pass portMUX_NO_TIMEOUT to wait forever, portMUX_TRY_LOCK to try a single time to acquire the lock.

!!! note "戻り値"
	bool true if mutex is successfully acquired, false on timeout. 



### vPortCPUReleaseMutex()



```c
void vPortCPUReleaseMutex(portMUX_TYPE *mux)
```

!!! summary "引数"
	- portMUX_TYPE* `mux` 

!!! note "戻り値"
	void



### portENTER_CRITICAL_NESTED()



```c
static unsigned portENTER_CRITICAL_NESTED()
```

!!! note "戻り値"
	unsigned



### uxPortCompareSet()



```c
static void uxPortCompareSet(volatile uint32_t *addr, uint32_t compare, uint32_t *set)
```

!!! summary "引数"
	- volatile uint32_t * `addr` 
	- uint32_t `compare` 
	- uint32_t * `set` 

!!! note "戻り値"
	void



### vPortYield()



```c
void vPortYield(void)
```

!!! note "戻り値"
	void



### _frxt_setup_switch()



```c
void _frxt_setup_switch(void)
```

!!! note "戻り値"
	void



### xPortGetCoreID()



```c
static uint32_t xPortGetCoreID()
```

!!! note "戻り値"
	uint32_t



### esp_vApplicationIdleHook()



```c
void esp_vApplicationIdleHook(void)
```

!!! note "戻り値"
	void



### esp_vApplicationTickHook()



```c
void esp_vApplicationTickHook(void)
```

!!! note "戻り値"
	void



### _xt_coproc_release()



```c
void _xt_coproc_release(volatile void *coproc_sa_base)
```

!!! summary "引数"
	- volatile void * `coproc_sa_base` 

!!! note "戻り値"
	void



### vApplicationSleep()



```c
void vApplicationSleep(TickType_t xExpectedIdleTime)
```

!!! summary "引数"
	- TickType_t `xExpectedIdleTime` 

!!! note "戻り値"
	void



