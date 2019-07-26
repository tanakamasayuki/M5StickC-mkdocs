# rtc_cntl

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/rtc_cntl.h>
```

上記宣言で利用できます。

## メンバー

### rtc_isr_register()
Register a handler for specific RTC_CNTL interrupts

Multiple handlers can be registered using this function. Whenever an RTC interrupt happens, all handlers with matching rtc_intr_mask values will be called.
```c
esp_err_t rtc_isr_register(intr_handler_t handler, void *handler_arg, uint32_t rtc_intr_mask)
```

!!! summary "引数"
	- intr_handler_t `handler` handler function to call 
	- void * `handler_arg` argument to be passed to the handler 
	- uint32_t `rtc_intr_mask` combination of RTC_CNTL_*_INT_ENA bits indicating the sources to call the handler for 

!!! note "戻り値"
	esp_err_t



### rtc_isr_deregister()
Deregister the handler previously registered using rtc_isr_register


```c
esp_err_t rtc_isr_deregister(intr_handler_t handler, void *handler_arg)
```

!!! summary "引数"
	- intr_handler_t `handler` handler function to call (as passed to rtc_isr_register) 
	- void * `handler_arg` argument of the handler (as passed to rtc_isr_register) 

!!! note "戻り値"
	esp_err_t 




