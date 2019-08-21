# timers



## メンバー



















































### xTimerCreate()


Timers are created in the dormant state. The , , , ,  and  API functions can all be used to transition a timer into the active state.
```c
TimerHandle_t xTimerCreate(const char *const pcTimerName, const TickType_t xTimerPeriodInTicks, const UBaseType_t uxAutoReload, void *const pvTimerID, TimerCallbackFunction_t pxCallbackFunction) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- const char *const `pcTimerName` A text name that is assigned to the timer. This is done purely to assist debugging. The kernel itself only ever references a timer by its handle, and never by its name.
	- TickType_tconst `xTimerPeriodInTicks` The timer period. The time is defined in tick periods so the constant portTICK_PERIOD_MS can be used to convert a time that has been specified in milliseconds. For example, if the timer must expire after 100 ticks, then xTimerPeriodInTicks should be set to 100. Alternatively, if the timer must expire after 500ms, then xPeriod can be set to ( 500 / portTICK_PERIOD_MS ) provided configTICK_RATE_HZ is less than or equal to 1000.
	- UBaseType_tconst `uxAutoReload` If uxAutoReload is set to pdTRUE then the timer will expire repeatedly with a frequency set by the xTimerPeriodInTicks parameter. If uxAutoReload is set to pdFALSE then the timer will be a one-shot timer and enter the dormant state after it expires.
	- void *const `pvTimerID` An identifier that is assigned to the timer being created. Typically this would be used in the timer callback function to identify which timer expired when the same callback function is assigned to more than one timer.
	- TimerCallbackFunction_t `pxCallbackFunction` The function to call when the timer expires. Callback functions must have the prototype defined by TimerCallbackFunction_t, which is "void vCallbackFunction( TimerHandle_t xTimer );".

!!! note "戻り値"
	TimerHandle_t



### pvTimerGetTimerID()


See the  API function example usage scenario. 
```c
void* pvTimerGetTimerID(TimerHandle_t xTimer) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TimerHandle_t `xTimer` The timer being queried.

!!! note "戻り値"
	void *



### vTimerSetTimerID()


See the  API function example usage scenario. 
```c
void vTimerSetTimerID(TimerHandle_t xTimer, void *pvNewID) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TimerHandle_t `xTimer` The timer being updated.
	- void * `pvNewID` The ID to assign to the timer.

!!! note "戻り値"
	void



### xTimerIsTimerActive()


Timers are created in the dormant state. The , , , ,  and  API functions can all be used to transition a timer into the active state.
```c
BaseType_t xTimerIsTimerActive(TimerHandle_t xTimer) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TimerHandle_t `xTimer` The timer being queried.

!!! note "戻り値"
	BaseType_t



### xTimerGetTimerDaemonTaskHandle()


Simply returns the handle of the timer service/daemon task. It it not valid to call  before the scheduler has been started. 
```c
TaskHandle_t xTimerGetTimerDaemonTaskHandle(void)
```

!!! note "戻り値"
	TaskHandle_t



### xTimerGetPeriod()


Returns the period of a timer.
```c
TickType_t xTimerGetPeriod(TimerHandle_t xTimer) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TimerHandle_t `xTimer` The handle of the timer being queried.

!!! note "戻り値"
	TickType_t



### xTimerGetExpiryTime()


Returns the time in ticks at which the timer will expire. If this is less than the current tick count then the expiry time has overflowed from the current time.
```c
TickType_t xTimerGetExpiryTime(TimerHandle_t xTimer) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- TimerHandle_t `xTimer` The handle of the timer being queried.

!!! note "戻り値"
	TickType_t



### xTimerPendFunctionCallFromISR()


A mechanism is provided that allows the interrupt to return directly to the task that will subsequently execute the pended callback function. This allows the callback function to execute contiguously in time with the interrupt - just as if the callback had executed in the interrupt itself.
```c
BaseType_t xTimerPendFunctionCallFromISR(PendedFunction_t xFunctionToPend, void *pvParameter1, uint32_t ulParameter2, BaseType_t *pxHigherPriorityTaskWoken)
```

!!! summary "引数"
	- PendedFunction_t `xFunctionToPend` The function to execute from the timer service/ daemon task. The function must conform to the PendedFunction_t prototype.
	- void * `pvParameter1` The value of the callback function's first parameter. The parameter has a void * type to allow it to be used to pass any type. For example, unsigned longs can be cast to a void *, or the void * can be used to point to a structure.
	- uint32_t `ulParameter2` The value of the callback function's second parameter.
	- BaseType_t* `pxHigherPriorityTaskWoken` As mentioned above, calling this function will result in a message being sent to the timer daemon task. If the priority of the timer daemon task (which is set using configTIMER_TASK_PRIORITY in ) is higher than the priority of the currently running task (the task the interrupt interrupted) then *pxHigherPriorityTaskWoken will be set to pdTRUE within , indicating that a context switch should be requested before the interrupt exits. For that reason *pxHigherPriorityTaskWoken must be initialised to pdFALSE. See the example code below.

!!! note "戻り値"
	BaseType_t



### xTimerPendFunctionCall()


Used to defer the execution of a function to the RTOS daemon task (the timer service task, hence this function is implemented in timers.c and is prefixed with 'Timer').
```c
BaseType_t xTimerPendFunctionCall(PendedFunction_t xFunctionToPend, void *pvParameter1, uint32_t ulParameter2, TickType_t xTicksToWait)
```

!!! summary "引数"
	- PendedFunction_t `xFunctionToPend` The function to execute from the timer service/ daemon task. The function must conform to the PendedFunction_t prototype.
	- void * `pvParameter1` The value of the callback function's first parameter. The parameter has a void * type to allow it to be used to pass any type. For example, unsigned longs can be cast to a void *, or the void * can be used to point to a structure.
	- uint32_t `ulParameter2` The value of the callback function's second parameter.
	- TickType_t `xTicksToWait` Calling this function will result in a message being sent to the timer daemon task on a queue. xTicksToWait is the amount of time the calling task should remain in the Blocked state (so not using any processing time) for space to become available on the timer queue if the queue is found to be full.

!!! note "戻り値"
	BaseType_t



### pcTimerGetTimerName()


Returns the name that was assigned to a timer when the timer was created.
```c
const char* pcTimerGetTimerName(TimerHandle_t xTimer)
```

!!! summary "引数"
	- TimerHandle_t `xTimer` The handle of the timer being queried.

!!! note "戻り値"
	const char *



