# timer

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/timer.h>
```

上記宣言で利用できます。


## メンバー



















### timer_get_counter_value()
Read the counter value of hardware timer.


```c
esp_err_t timer_get_counter_value(timer_group_t group_num, timer_idx_t timer_num, uint64_t *timer_val)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1] 
	- uint64_t * `timer_val` Pointer to accept timer counter value.

!!! note "戻り値"
	esp_err_t 




### timer_get_counter_time_sec()
Read the counter value of hardware timer, in unit of a given scale.


```c
esp_err_t timer_get_counter_time_sec(timer_group_t group_num, timer_idx_t timer_num, double *time)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1] 
	- double * `time` Pointer, type of double*, to accept timer counter value, in seconds.

!!! note "戻り値"
	esp_err_t 




### timer_set_counter_value()
Set counter value to hardware timer.


```c
esp_err_t timer_set_counter_value(timer_group_t group_num, timer_idx_t timer_num, uint64_t load_val)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1] 
	- uint64_t `load_val` Counter value to write to the hardware timer.

!!! note "戻り値"
	esp_err_t 




### timer_start()
Start the counter of hardware timer.


```c
esp_err_t timer_start(timer_group_t group_num, timer_idx_t timer_num)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group number, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1]

!!! note "戻り値"
	esp_err_t 




### timer_pause()
Pause the counter of hardware timer.


```c
esp_err_t timer_pause(timer_group_t group_num, timer_idx_t timer_num)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group number, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1]

!!! note "戻り値"
	esp_err_t 




### timer_set_counter_mode()
Set counting mode for hardware timer.


```c
esp_err_t timer_set_counter_mode(timer_group_t group_num, timer_idx_t timer_num, timer_count_dir_t counter_dir)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group number, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1] 
	- timer_count_dir_t `counter_dir` Counting direction of timer, count-up or count-down

!!! note "戻り値"
	esp_err_t 




### timer_set_auto_reload()
Enable or disable counter reload function when alarm event occurs.


```c
esp_err_t timer_set_auto_reload(timer_group_t group_num, timer_idx_t timer_num, timer_autoreload_t reload)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group number, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1] 
	- timer_autoreload_t `reload` Counter reload mode.

!!! note "戻り値"
	esp_err_t 




### timer_set_divider()
Set hardware timer source clock divider. Timer groups clock are divider from APB clock.


```c
esp_err_t timer_set_divider(timer_group_t group_num, timer_idx_t timer_num, uint32_t divider)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group number, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1] 
	- uint32_t `divider` Timer clock divider value. The divider's range is from from 2 to 65536.

!!! note "戻り値"
	esp_err_t 




### timer_set_alarm_value()
Set timer alarm value.


```c
esp_err_t timer_set_alarm_value(timer_group_t group_num, timer_idx_t timer_num, uint64_t alarm_value)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1] 
	- uint64_t `alarm_value` A 64-bit value to set the alarm value.

!!! note "戻り値"
	esp_err_t 




### timer_get_alarm_value()
Get timer alarm value.


```c
esp_err_t timer_get_alarm_value(timer_group_t group_num, timer_idx_t timer_num, uint64_t *alarm_value)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1] 
	- uint64_t * `alarm_value` Pointer of A 64-bit value to accept the alarm value.

!!! note "戻り値"
	esp_err_t 




### timer_set_alarm()
Enable or disable generation of timer alarm events.


```c
esp_err_t timer_set_alarm(timer_group_t group_num, timer_idx_t timer_num, timer_alarm_t alarm_en)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1] 
	- timer_alarm_t `alarm_en` To enable or disable timer alarm function.

!!! note "戻り値"
	esp_err_t 




### timer_isr_register()
Register Timer interrupt handler, the handler is an ISR. The handler will be attached to the same CPU core that this function is running on.


```c
esp_err_t timer_isr_register(timer_group_t group_num, timer_idx_t timer_num, void(*fn)(void *), void *arg, int intr_alloc_flags, timer_isr_handle_t *handle)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group number 
	- timer_idx_t `timer_num` Timer index of timer group 
	- void(*)(void *) `fn` Interrupt handler function. 
	- void * `arg` Parameter for handler function 
	- int `intr_alloc_flags` Flags used to allocate the interrupt. One or multiple (ORred) ESP_INTR_FLAG_* values. See esp_intr_alloc.h for more info. 
	- timer_isr_handle_t* `handle` Pointer to return handle. If non-NULL, a handle for the interrupt will be returned here.

!!! note "戻り値"
	esp_err_t



### timer_init()
Initializes and configure the timer.


```c
esp_err_t timer_init(timer_group_t group_num, timer_idx_t timer_num, const timer_config_t *config)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group number, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1] 
	- timer_config_tconst  * `config` Pointer to timer initialization parameters.

!!! note "戻り値"
	esp_err_t 




### timer_get_config()
Get timer configure value.


```c
esp_err_t timer_get_config(timer_group_t group_num, timer_idx_t timer_num, timer_config_t *config)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group number, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index, 0 for hw_timer[0] & 1 for hw_timer[1] 
	- timer_config_t* `config` Pointer of struct to accept timer parameters.

!!! note "戻り値"
	esp_err_t 




### timer_group_intr_enable()
Enable timer group interrupt, by enable mask


```c
esp_err_t timer_group_intr_enable(timer_group_t group_num, uint32_t en_mask)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group number, 0 for TIMERG0 or 1 for TIMERG1 
	- uint32_t `en_mask` Timer interrupt enable mask. Use TIMG_T0_INT_ENA_M to enable t0 interrupt Use TIMG_T1_INT_ENA_M to enable t1 interrupt

!!! note "戻り値"
	esp_err_t 




### timer_group_intr_disable()
Disable timer group interrupt, by disable mask


```c
esp_err_t timer_group_intr_disable(timer_group_t group_num, uint32_t disable_mask)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group number, 0 for TIMERG0 or 1 for TIMERG1 
	- uint32_t `disable_mask` Timer interrupt disable mask. Use TIMG_T0_INT_ENA_M to disable t0 interrupt Use TIMG_T1_INT_ENA_M to disable t1 interrupt

!!! note "戻り値"
	esp_err_t 




### timer_enable_intr()
Enable timer interrupt


```c
esp_err_t timer_enable_intr(timer_group_t group_num, timer_idx_t timer_num)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group number, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index.

!!! note "戻り値"
	esp_err_t 




### timer_disable_intr()
Disable timer interrupt


```c
esp_err_t timer_disable_intr(timer_group_t group_num, timer_idx_t timer_num)
```

!!! summary "引数"
	- timer_group_t `group_num` Timer group number, 0 for TIMERG0 or 1 for TIMERG1 
	- timer_idx_t `timer_num` Timer index.

!!! note "戻り値"
	esp_err_t 




