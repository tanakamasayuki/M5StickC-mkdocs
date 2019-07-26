# pcnt

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/pcnt.h>
```

上記宣言で利用できます。

## メンバー















### pcnt_unit_config()
Configure Pulse Counter unit


```c
esp_err_t pcnt_unit_config(const pcnt_config_t *pcnt_config)
```

!!! summary "引数"
	- pcnt_config_tconst  * `pcnt_config` Pointer of Pulse Counter unit configure parameter

!!! note "戻り値"
	esp_err_t



### pcnt_get_counter_value()
Get pulse counter value


```c
esp_err_t pcnt_get_counter_value(pcnt_unit_t pcnt_unit, int16_t *count)
```

!!! summary "引数"
	- pcnt_unit_t `pcnt_unit` Pulse Counter unit number 
	- int16_t * `count` Pointer to accept counter value

!!! note "戻り値"
	esp_err_t 



### pcnt_counter_pause()
Pause PCNT counter of PCNT unit


```c
esp_err_t pcnt_counter_pause(pcnt_unit_t pcnt_unit)
```

!!! summary "引数"
	- pcnt_unit_t `pcnt_unit` PCNT unit number

!!! note "戻り値"
	esp_err_t 




### pcnt_counter_resume()
Resume counting for PCNT counter


```c
esp_err_t pcnt_counter_resume(pcnt_unit_t pcnt_unit)
```

!!! summary "引数"
	- pcnt_unit_t `pcnt_unit` PCNT unit number, select from pcnt_unit_t

!!! note "戻り値"
	esp_err_t 




### pcnt_counter_clear()
Clear and reset PCNT counter value to zero


```c
esp_err_t pcnt_counter_clear(pcnt_unit_t pcnt_unit)
```

!!! summary "引数"
	- pcnt_unit_t `pcnt_unit` PCNT unit number, select from pcnt_unit_t

!!! note "戻り値"
	esp_err_t 




### pcnt_intr_enable()
Enable PCNT interrupt for PCNT unit


```c
esp_err_t pcnt_intr_enable(pcnt_unit_t pcnt_unit)
```

!!! summary "引数"
	- pcnt_unit_t `pcnt_unit` PCNT unit number

!!! note "戻り値"
	esp_err_t



### pcnt_intr_disable()
Disable PCNT interrupt for PCNT unit


```c
esp_err_t pcnt_intr_disable(pcnt_unit_t pcnt_unit)
```

!!! summary "引数"
	- pcnt_unit_t `pcnt_unit` PCNT unit number

!!! note "戻り値"
	esp_err_t 




### pcnt_event_enable()
Enable PCNT event of PCNT unit


```c
esp_err_t pcnt_event_enable(pcnt_unit_t unit, pcnt_evt_type_t evt_type)
```

!!! summary "引数"
	- pcnt_unit_t `unit` PCNT unit number 
	- pcnt_evt_type_t `evt_type` Watch point event type. All enabled events share the same interrupt (one interrupt per pulse counter unit). 

!!! note "戻り値"
	esp_err_t 




### pcnt_event_disable()
Disable PCNT event of PCNT unit


```c
esp_err_t pcnt_event_disable(pcnt_unit_t unit, pcnt_evt_type_t evt_type)
```

!!! summary "引数"
	- pcnt_unit_t `unit` PCNT unit number 
	- pcnt_evt_type_t `evt_type` Watch point event type. All enabled events share the same interrupt (one interrupt per pulse counter unit). 

!!! note "戻り値"
	esp_err_t 




### pcnt_set_event_value()
Set PCNT event value of PCNT unit


```c
esp_err_t pcnt_set_event_value(pcnt_unit_t unit, pcnt_evt_type_t evt_type, int16_t value)
```

!!! summary "引数"
	- pcnt_unit_t `unit` PCNT unit number 
	- pcnt_evt_type_t `evt_type` Watch point event type. All enabled events share the same interrupt (one interrupt per pulse counter unit).
	- int16_t `value` Counter value for PCNT event

!!! note "戻り値"
	esp_err_t 




### pcnt_get_event_value()
Get PCNT event value of PCNT unit


```c
esp_err_t pcnt_get_event_value(pcnt_unit_t unit, pcnt_evt_type_t evt_type, int16_t *value)
```

!!! summary "引数"
	- pcnt_unit_t `unit` PCNT unit number 
	- pcnt_evt_type_t `evt_type` Watch point event type. All enabled events share the same interrupt (one interrupt per pulse counter unit). 
	- int16_t * `value` Pointer to accept counter value for PCNT event

!!! note "戻り値"
	esp_err_t 




### pcnt_isr_register()
Register PCNT interrupt handler, the handler is an ISR. The handler will be attached to the same CPU core that this function is running on. Please do not use pcnt_isr_service_install if this function was called.


```c
esp_err_t pcnt_isr_register(void(*fn)(void *), void *arg, int intr_alloc_flags, pcnt_isr_handle_t *handle)
```

!!! summary "引数"
	- void(*)(void *) `fn` Interrupt handler function. 
	- void * `arg` Parameter for handler function 
	- int `intr_alloc_flags` Flags used to allocate the interrupt. One or multiple (ORred) ESP_INTR_FLAG_* values. See esp_intr_alloc.h for more info. 
	- pcnt_isr_handle_t* `handle` Pointer to return handle. If non-NULL, a handle for the interrupt will be returned here. Calling esp_intr_free to unregister this ISR service if needed, but only if the handle is not NULL.

!!! note "戻り値"
	esp_err_t 




### pcnt_set_pin()
Configure PCNT pulse signal input pin and control input pin


```c
esp_err_t pcnt_set_pin(pcnt_unit_t unit, pcnt_channel_t channel, int pulse_io, int ctrl_io)
```

!!! summary "引数"
	- pcnt_unit_t `unit` PCNT unit number 
	- pcnt_channel_t `channel` PCNT channel number 
	- int `pulse_io` Pulse signal input GPIO 
	- int `ctrl_io` Control signal input GPIO

!!! note "戻り値"
	esp_err_t



### pcnt_filter_enable()
Enable PCNT input filter


```c
esp_err_t pcnt_filter_enable(pcnt_unit_t unit)
```

!!! summary "引数"
	- pcnt_unit_t `unit` PCNT unit number

!!! note "戻り値"
	esp_err_t 




### pcnt_filter_disable()
Disable PCNT input filter


```c
esp_err_t pcnt_filter_disable(pcnt_unit_t unit)
```

!!! summary "引数"
	- pcnt_unit_t `unit` PCNT unit number

!!! note "戻り値"
	esp_err_t 




### pcnt_set_filter_value()
Set PCNT filter value


```c
esp_err_t pcnt_set_filter_value(pcnt_unit_t unit, uint16_t filter_val)
```

!!! summary "引数"
	- pcnt_unit_t `unit` PCNT unit number 
	- uint16_t `filter_val` PCNT signal filter value, counter in APB_CLK cycles. Any pulses lasting shorter than this will be ignored when the filter is enabled. 

!!! note "戻り値"
	esp_err_t



### pcnt_get_filter_value()
Get PCNT filter value


```c
esp_err_t pcnt_get_filter_value(pcnt_unit_t unit, uint16_t *filter_val)
```

!!! summary "引数"
	- pcnt_unit_t `unit` PCNT unit number 
	- uint16_t * `filter_val` Pointer to accept PCNT filter value.

!!! note "戻り値"
	esp_err_t 




### pcnt_set_mode()
Set PCNT counter mode


```c
esp_err_t pcnt_set_mode(pcnt_unit_t unit, pcnt_channel_t channel, pcnt_count_mode_t pos_mode, pcnt_count_mode_t neg_mode, pcnt_ctrl_mode_t hctrl_mode, pcnt_ctrl_mode_t lctrl_mode)
```

!!! summary "引数"
	- pcnt_unit_t `unit` PCNT unit number 
	- pcnt_channel_t `channel` PCNT channel number 
	- pcnt_count_mode_t `pos_mode` Counter mode when detecting positive edge 
	- pcnt_count_mode_t `neg_mode` Counter mode when detecting negative edge 
	- pcnt_ctrl_mode_t `hctrl_mode` Counter mode when control signal is high level 
	- pcnt_ctrl_mode_t `lctrl_mode` Counter mode when control signal is low level

!!! note "戻り値"
	esp_err_t 




### pcnt_isr_handler_add()
Add ISR handler for specified unit.

This ISR handler will be called from an ISR. So there is a stack size limit (configurable as "ISR stack size" in menuconfig). This limit is smaller compared to a global PCNT interrupt handler due to the additional level of indirection.
```c
esp_err_t pcnt_isr_handler_add(pcnt_unit_t unit, void(*isr_handler)(void *), void *args)
```

!!! summary "引数"
	- pcnt_unit_t `unit` PCNT unit number 
	- void(*)(void *) `isr_handler` Interrupt handler function. 
	- void * `args` Parameter for handler function

!!! note "戻り値"
	esp_err_t



### pcnt_isr_service_install()
Install PCNT ISR service.


```c
esp_err_t pcnt_isr_service_install(int intr_alloc_flags)
```

!!! summary "引数"
	- int `intr_alloc_flags` Flags used to allocate the interrupt. One or multiple (ORred) ESP_INTR_FLAG_* values. See esp_intr_alloc.h for more info.

!!! note "戻り値"
	esp_err_t



### pcnt_isr_service_uninstall()
Uninstall PCNT ISR service, freeing related resources.


```c
void pcnt_isr_service_uninstall(void)
```

!!! note "戻り値"
	void



### pcnt_isr_handler_remove()
Delete ISR handler for specified unit.


```c
esp_err_t pcnt_isr_handler_remove(pcnt_unit_t unit)
```

!!! summary "引数"
	- pcnt_unit_t `unit` PCNT unit number

!!! note "戻り値"
	esp_err_t 




