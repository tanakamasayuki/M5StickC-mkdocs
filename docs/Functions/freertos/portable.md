# portable



## メンバー













### pxPortInitialiseStack()



```c
StackType_t* pxPortInitialiseStack(StackType_t *pxTopOfStack, TaskFunction_t pxCode, void *pvParameters) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- StackType_t* `pxTopOfStack` 
	- TaskFunction_t `pxCode` 
	- void * `pvParameters` 

!!! note "戻り値"
	StackType_t*



### xPortStartScheduler()



```c
BaseType_t xPortStartScheduler(void) PRIVILEGED_FUNCTION
```

!!! note "戻り値"
	BaseType_t



### vPortEndScheduler()



```c
void vPortEndScheduler(void) PRIVILEGED_FUNCTION
```

!!! note "戻り値"
	void



### vPortYieldOtherCore()



```c
void vPortYieldOtherCore(BaseType_t coreid) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- BaseType_t `coreid` 

!!! note "戻り値"
	void



### vPortSetStackWatchpoint()



```c
void vPortSetStackWatchpoint(void *pxStackStart)
```

!!! summary "引数"
	- void * `pxStackStart` 

!!! note "戻り値"
	void



### xPortInIsrContext()



```c
BaseType_t xPortInIsrContext()
```

!!! note "戻り値"
	BaseType_t



### xPortInterruptedFromISRContext()



```c
BaseType_t xPortInterruptedFromISRContext()
```

!!! note "戻り値"
	BaseType_t



### xPortGetCoreID()



```c
static uint32_t IRAM_ATTR xPortGetCoreID()
```

!!! note "戻り値"
	uint32_t IRAM_ATTR



### xPortGetTickRateHz()



```c
uint32_t xPortGetTickRateHz(void)
```

!!! note "戻り値"
	uint32_t



### uxPortCompareSetExtram()



```c
void uxPortCompareSetExtram(volatile uint32_t *addr, uint32_t compare, uint32_t *set)
```

!!! summary "引数"
	- volatile uint32_t * `addr` 
	- uint32_t `compare` 
	- uint32_t * `set` 

!!! note "戻り値"
	void



