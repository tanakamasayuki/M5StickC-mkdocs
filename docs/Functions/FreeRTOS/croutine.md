# croutine



## メンバー

























### xCoRoutineCreate()



```c
BaseType_t xCoRoutineCreate(crCOROUTINE_CODE pxCoRoutineCode, UBaseType_t uxPriority, UBaseType_t uxIndex)
```

!!! summary "引数"
	- crCOROUTINE_CODE `pxCoRoutineCode` 
	- UBaseType_t `uxPriority` 
	- UBaseType_t `uxIndex` 

!!! note "戻り値"
	BaseType_t



### vCoRoutineSchedule()



```c
void vCoRoutineSchedule(void)
```

!!! note "戻り値"
	void



### vCoRoutineAddToDelayedList()



```c
void vCoRoutineAddToDelayedList(TickType_t xTicksToDelay, List_t *pxEventList)
```

!!! summary "引数"
	- TickType_t `xTicksToDelay` 
	- List_t* `pxEventList` 

!!! note "戻り値"
	void



### xCoRoutineRemoveFromEventList()



```c
BaseType_t xCoRoutineRemoveFromEventList(const List_t *pxEventList)
```

!!! summary "引数"
	- List_tconst  * `pxEventList` 

!!! note "戻り値"
	BaseType_t



