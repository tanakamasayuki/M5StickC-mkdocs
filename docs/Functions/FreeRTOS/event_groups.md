# event_groups



## メンバー











### xEventGroupCreate()



Example usage:  
```c
EventGroupHandle_t xEventGroupCreate(void) PRIVILEGED_FUNCTION
```

!!! note "戻り値"
	EventGroupHandle_t



### xEventGroupWaitBits()


This function cannot be called from an interrupt.
```c
EventBits_t xEventGroupWaitBits(EventGroupHandle_t xEventGroup, const EventBits_t uxBitsToWaitFor, const BaseType_t xClearOnExit, const BaseType_t xWaitForAllBits, TickType_t xTicksToWait) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- EventGroupHandle_t `xEventGroup` The event group in which the bits are being tested. The event group must have previously been created using a call to .
	- EventBits_tconst `uxBitsToWaitFor` A bitwise value that indicates the bit or bits to test inside the event group. For example, to wait for bit 0 and/or bit 2 set uxBitsToWaitFor to 0x05. To wait for bits 0 and/or bit 1 and/or bit 2 set uxBitsToWaitFor to 0x07. Etc.
	- BaseType_tconst `xClearOnExit` If xClearOnExit is set to pdTRUE then any bits within uxBitsToWaitFor that are set within the event group will be cleared before  returns if the wait condition was met (if the function returns for a reason other than a timeout). If xClearOnExit is set to pdFALSE then the bits set in the event group are not altered when the call to  returns.
	- BaseType_tconst `xWaitForAllBits` If xWaitForAllBits is set to pdTRUE then  will return when either all the bits in uxBitsToWaitFor are set or the specified block time expires. If xWaitForAllBits is set to pdFALSE then  will return when any one of the bits set in uxBitsToWaitFor is set or the specified block time expires. The block time is specified by the xTicksToWait parameter.
	- TickType_t `xTicksToWait` The maximum amount of time (specified in 'ticks') to wait for one/all (depending on the xWaitForAllBits value) of the bits specified by uxBitsToWaitFor to become set.

!!! note "戻り値"
	EventBits_t



### xEventGroupClearBits()


Clear bits within an event group. This function cannot be called from an interrupt.
```c
EventBits_t xEventGroupClearBits(EventGroupHandle_t xEventGroup, const EventBits_t uxBitsToClear) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- EventGroupHandle_t `xEventGroup` The event group in which the bits are to be cleared.
	- EventBits_tconst `uxBitsToClear` A bitwise value that indicates the bit or bits to clear in the event group. For example, to clear bit 3 only, set uxBitsToClear to 0x08. To clear bit 3 and bit 0 set uxBitsToClear to 0x09.

!!! note "戻り値"
	EventBits_t



### xEventGroupSetBits()


Setting bits in an event group will automatically unblock tasks that are blocked waiting for the bits.
```c
EventBits_t xEventGroupSetBits(EventGroupHandle_t xEventGroup, const EventBits_t uxBitsToSet) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- EventGroupHandle_t `xEventGroup` The event group in which the bits are to be set.
	- EventBits_tconst `uxBitsToSet` A bitwise value that indicates the bit or bits to set. For example, to set bit 3 only, set uxBitsToSet to 0x08. To set bit 3 and bit 0 set uxBitsToSet to 0x09.

!!! note "戻り値"
	EventBits_t



### xEventGroupSync()


The function will return before its block time expires if the bits specified by the uxBitsToWait parameter are set, or become set within that time. In this case all the bits specified by uxBitsToWait will be automatically cleared before the function returns.
```c
EventBits_t xEventGroupSync(EventGroupHandle_t xEventGroup, const EventBits_t uxBitsToSet, const EventBits_t uxBitsToWaitFor, TickType_t xTicksToWait) PRIVILEGED_FUNCTION
```

!!! summary "引数"
	- EventGroupHandle_t `xEventGroup` The event group in which the bits are being tested. The event group must have previously been created using a call to .
	- EventBits_tconst `uxBitsToSet` The bits to set in the event group before determining if, and possibly waiting for, all the bits specified by the uxBitsToWait parameter are set.
	- EventBits_tconst `uxBitsToWaitFor` A bitwise value that indicates the bit or bits to test inside the event group. For example, to wait for bit 0 and bit 2 set uxBitsToWaitFor to 0x05. To wait for bits 0 and bit 1 and bit 2 set uxBitsToWaitFor to 0x07. Etc.
	- TickType_t `xTicksToWait` The maximum amount of time (specified in 'ticks') to wait for all of the bits specified by uxBitsToWaitFor to become set.

!!! note "戻り値"
	EventBits_t



### xEventGroupGetBitsFromISR()


A version of  that can be called from an ISR.
```c
EventBits_t xEventGroupGetBitsFromISR(EventGroupHandle_t xEventGroup)
```

!!! summary "引数"
	- EventGroupHandle_t `xEventGroup` The event group being queried.

!!! note "戻り値"
	EventBits_t



### vEventGroupDelete()


Delete an event group that was previously created by a call to . Tasks that are blocked on the event group will be unblocked and obtain 0 as the event group's value.
```c
void vEventGroupDelete(EventGroupHandle_t xEventGroup)
```

!!! summary "引数"
	- EventGroupHandle_t `xEventGroup` The event group being deleted. 

!!! note "戻り値"
	void



