# touch_pad

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/touch_pad.h>
```

上記宣言で利用できます。

## メンバー





































### touch_pad_init()
Initialize touch module.




```c
esp_err_t touch_pad_init()
```

!!! note "戻り値"
	esp_err_t



### touch_pad_deinit()
Un-install touch pad driver.




```c
esp_err_t touch_pad_deinit()
```

!!! note "戻り値"
	esp_err_t



### touch_pad_config()
Configure touch pad interrupt threshold.


```c
esp_err_t touch_pad_config(touch_pad_t touch_num, uint16_t threshold)
```

!!! summary "引数"
	- touch_pad_t `touch_num` touch pad index 
	- uint16_t `threshold` interrupt threshold,

!!! note "戻り値"
	esp_err_t



### touch_pad_read()
get touch sensor counter value. Each touch sensor has a counter to count the number of charge/discharge cycles. When the pad is not 'touched', we can get a number of the counter. When the pad is 'touched', the value in counter will get smaller because of the larger equivalent capacitance.


```c
esp_err_t touch_pad_read(touch_pad_t touch_num, uint16_t *touch_value)
```

!!! summary "引数"
	- touch_pad_t `touch_num` touch pad index 
	- uint16_t * `touch_value` pointer to accept touch sensor value

!!! note "戻り値"
	esp_err_t



### touch_pad_read_filtered()
get filtered touch sensor counter value by IIR filter.


```c
esp_err_t touch_pad_read_filtered(touch_pad_t touch_num, uint16_t *touch_value)
```

!!! summary "引数"
	- touch_pad_t `touch_num` touch pad index 
	- uint16_t * `touch_value` pointer to accept touch sensor value

!!! note "戻り値"
	esp_err_t



### touch_pad_read_raw_data()
get raw data (touch sensor counter value) from IIR filter process. Need not request hardware measurements.


```c
esp_err_t touch_pad_read_raw_data(touch_pad_t touch_num, uint16_t *touch_value)
```

!!! summary "引数"
	- touch_pad_t `touch_num` touch pad index 
	- uint16_t * `touch_value` pointer to accept touch sensor value

!!! note "戻り値"
	esp_err_t



### touch_pad_set_filter_read_cb()
Register the callback function that is called after each IIR filter calculation.


```c
esp_err_t touch_pad_set_filter_read_cb(filter_cb_t read_cb)
```

!!! summary "引数"
	- filter_cb_t `read_cb` Pointer to filtered callback function. If the argument passed in is NULL, the callback will stop. 

!!! note "戻り値"
	esp_err_t



### touch_pad_isr_handler_register()
Register touch-pad ISR,


```c
esp_err_t touch_pad_isr_handler_register(void(*fn)(void *), void *arg, int unused, intr_handle_t *handle_unused) __attribute__((deprecated))
```

!!! summary "引数"
	- void(*)(void *) `fn` Pointer to ISR handler 
	- void * `arg` Parameter for ISR 
	- int `unused` Reserved, not used 
	- intr_handle_t * `handle_unused` Reserved, not used 

!!! note "戻り値"
	esp_err_t



### touch_pad_isr_register()
Register touch-pad ISR. The handler will be attached to the same CPU core that this function is running on.


```c
esp_err_t touch_pad_isr_register(intr_handler_t fn, void *arg)
```

!!! summary "引数"
	- intr_handler_t `fn` Pointer to ISR handler 
	- void * `arg` Parameter for ISR 

!!! note "戻り値"
	esp_err_t 




### touch_pad_isr_deregister()
Deregister the handler previously registered using touch_pad_isr_handler_register


```c
esp_err_t touch_pad_isr_deregister(void(*fn)(void *), void *arg)
```

!!! summary "引数"
	- void(*)(void *) `fn` handler function to call (as passed to touch_pad_isr_handler_register) 
	- void * `arg` argument of the handler (as passed to touch_pad_isr_handler_register) 

!!! note "戻り値"
	esp_err_t 




### touch_pad_set_meas_time()
Set touch sensor measurement and sleep time


```c
esp_err_t touch_pad_set_meas_time(uint16_t sleep_cycle, uint16_t meas_cycle)
```

!!! summary "引数"
	- uint16_t `sleep_cycle` The touch sensor will sleep after each measurement. sleep_cycle decide the interval between each measurement. t_sleep = sleep_cycle / (RTC_SLOW_CLK frequency). The approximate frequency value of RTC_SLOW_CLK can be obtained using rtc_clk_slow_freq_get_hz function. 
	- uint16_t `meas_cycle` The duration of the touch sensor measurement. t_meas = meas_cycle / 8M, the maximum measure time is 0xffff / 8M = 8.19 ms 

!!! note "戻り値"
	esp_err_t 




### touch_pad_get_meas_time()
Get touch sensor measurement and sleep time


```c
esp_err_t touch_pad_get_meas_time(uint16_t *sleep_cycle, uint16_t *meas_cycle)
```

!!! summary "引数"
	- uint16_t * `sleep_cycle` Pointer to accept sleep cycle number 
	- uint16_t * `meas_cycle` Pointer to accept measurement cycle count. 

!!! note "戻り値"
	esp_err_t 




### touch_pad_set_voltage()
Set touch sensor reference voltage, if the voltage gap between high and low reference voltage get less, the charging and discharging time would be faster, accordingly, the counter value would be larger. In the case of detecting very slight change of capacitance, we can narrow down the gap so as to increase the sensitivity. On the other hand, narrow voltage gap would also introduce more noise, but we can use a software filter to pre-process the counter value.


```c
esp_err_t touch_pad_set_voltage(touch_high_volt_t refh, touch_low_volt_t refl, touch_volt_atten_t atten)
```

!!! summary "引数"
	- touch_high_volt_t `refh` the value of DREFH 
	- touch_low_volt_t `refl` the value of DREFL 
	- touch_volt_atten_t `atten` the attenuation on DREFH 

!!! note "戻り値"
	esp_err_t 




### touch_pad_get_voltage()
Get touch sensor reference voltage,


```c
esp_err_t touch_pad_get_voltage(touch_high_volt_t *refh, touch_low_volt_t *refl, touch_volt_atten_t *atten)
```

!!! summary "引数"
	- touch_high_volt_t* `refh` pointer to accept DREFH value 
	- touch_low_volt_t* `refl` pointer to accept DREFL value 
	- touch_volt_atten_t* `atten` pointer to accept the attenuation on DREFH 

!!! note "戻り値"
	esp_err_t 




### touch_pad_set_cnt_mode()
Set touch sensor charge/discharge speed for each pad. If the slope is 0, the counter would always be zero. If the slope is 1, the charging and discharging would be slow, accordingly, the counter value would be small. If the slope is set 7, which is the maximum value, the charging and discharging would be fast, accordingly, the counter value would be larger.


```c
esp_err_t touch_pad_set_cnt_mode(touch_pad_t touch_num, touch_cnt_slope_t slope, touch_tie_opt_t opt)
```

!!! summary "引数"
	- touch_pad_t `touch_num` touch pad index 
	- touch_cnt_slope_t `slope` touch pad charge/discharge speed 
	- touch_tie_opt_t `opt` the initial voltage 

!!! note "戻り値"
	esp_err_t 




### touch_pad_get_cnt_mode()
Get touch sensor charge/discharge speed for each pad


```c
esp_err_t touch_pad_get_cnt_mode(touch_pad_t touch_num, touch_cnt_slope_t *slope, touch_tie_opt_t *opt)
```

!!! summary "引数"
	- touch_pad_t `touch_num` touch pad index 
	- touch_cnt_slope_t* `slope` pointer to accept touch pad charge/discharge slope 
	- touch_tie_opt_t* `opt` pointer to accept the initial voltage 

!!! note "戻り値"
	esp_err_t 




### touch_pad_io_init()
Initialize touch pad GPIO


```c
esp_err_t touch_pad_io_init(touch_pad_t touch_num)
```

!!! summary "引数"
	- touch_pad_t `touch_num` touch pad index 

!!! note "戻り値"
	esp_err_t 




### touch_pad_set_fsm_mode()
Set touch sensor FSM mode, the test action can be triggered by the timer, as well as by the software.


```c
esp_err_t touch_pad_set_fsm_mode(touch_fsm_mode_t mode)
```

!!! summary "引数"
	- touch_fsm_mode_t `mode` FSM mode 

!!! note "戻り値"
	esp_err_t 




### touch_pad_get_fsm_mode()
Get touch sensor FSM mode


```c
esp_err_t touch_pad_get_fsm_mode(touch_fsm_mode_t *mode)
```

!!! summary "引数"
	- touch_fsm_mode_t* `mode` pointer to accept FSM mode 

!!! note "戻り値"
	esp_err_t 




### touch_pad_sw_start()
Trigger a touch sensor measurement, only support in SW mode of FSM



```c
esp_err_t touch_pad_sw_start()
```

!!! note "戻り値"
	esp_err_t 




### touch_pad_set_thresh()
Set touch sensor interrupt threshold


```c
esp_err_t touch_pad_set_thresh(touch_pad_t touch_num, uint16_t threshold)
```

!!! summary "引数"
	- touch_pad_t `touch_num` touch pad index 
	- uint16_t `threshold` threshold of touchpad count, refer to touch_pad_set_trigger_mode to see how to set trigger mode. 

!!! note "戻り値"
	esp_err_t 




### touch_pad_get_thresh()
Get touch sensor interrupt threshold


```c
esp_err_t touch_pad_get_thresh(touch_pad_t touch_num, uint16_t *threshold)
```

!!! summary "引数"
	- touch_pad_t `touch_num` touch pad index 
	- uint16_t * `threshold` pointer to accept threshold 

!!! note "戻り値"
	esp_err_t 




### touch_pad_set_trigger_mode()
Set touch sensor interrupt trigger mode. Interrupt can be triggered either when counter result is less than threshold or when counter result is more than threshold.


```c
esp_err_t touch_pad_set_trigger_mode(touch_trigger_mode_t mode)
```

!!! summary "引数"
	- touch_trigger_mode_t `mode` touch sensor interrupt trigger mode 

!!! note "戻り値"
	esp_err_t 




### touch_pad_get_trigger_mode()
Get touch sensor interrupt trigger mode


```c
esp_err_t touch_pad_get_trigger_mode(touch_trigger_mode_t *mode)
```

!!! summary "引数"
	- touch_trigger_mode_t* `mode` pointer to accept touch sensor interrupt trigger mode 

!!! note "戻り値"
	esp_err_t 




### touch_pad_set_trigger_source()
Set touch sensor interrupt trigger source. There are two sets of touch signals. Set1 and set2 can be mapped to several touch signals. Either set will be triggered if at least one of its touch signal is 'touched'. The interrupt can be configured to be generated if set1 is triggered, or only if both sets are triggered.


```c
esp_err_t touch_pad_set_trigger_source(touch_trigger_src_t src)
```

!!! summary "引数"
	- touch_trigger_src_t `src` touch sensor interrupt trigger source 

!!! note "戻り値"
	esp_err_t 




### touch_pad_get_trigger_source()
Get touch sensor interrupt trigger source


```c
esp_err_t touch_pad_get_trigger_source(touch_trigger_src_t *src)
```

!!! summary "引数"
	- touch_trigger_src_t* `src` pointer to accept touch sensor interrupt trigger source 

!!! note "戻り値"
	esp_err_t 




### touch_pad_set_group_mask()
Set touch sensor group mask. Touch pad module has two sets of signals, 'Touched' signal is triggered only if at least one of touch pad in this group is "touched". This function will set the register bits according to the given bitmask.


```c
esp_err_t touch_pad_set_group_mask(uint16_t set1_mask, uint16_t set2_mask, uint16_t en_mask)
```

!!! summary "引数"
	- uint16_t `set1_mask` bitmask of touch sensor signal group1, it's a 10-bit value 
	- uint16_t `set2_mask` bitmask of touch sensor signal group2, it's a 10-bit value 
	- uint16_t `en_mask` bitmask of touch sensor work enable, it's a 10-bit value 

!!! note "戻り値"
	esp_err_t 




### touch_pad_get_group_mask()
Get touch sensor group mask.


```c
esp_err_t touch_pad_get_group_mask(uint16_t *set1_mask, uint16_t *set2_mask, uint16_t *en_mask)
```

!!! summary "引数"
	- uint16_t * `set1_mask` pointer to accept bitmask of touch sensor signal group1, it's a 10-bit value 
	- uint16_t * `set2_mask` pointer to accept bitmask of touch sensor signal group2, it's a 10-bit value 
	- uint16_t * `en_mask` pointer to accept bitmask of touch sensor work enable, it's a 10-bit value 

!!! note "戻り値"
	esp_err_t 




### touch_pad_clear_group_mask()
Clear touch sensor group mask. Touch pad module has two sets of signals, Interrupt is triggered only if at least one of touch pad in this group is "touched". This function will clear the register bits according to the given bitmask.


```c
esp_err_t touch_pad_clear_group_mask(uint16_t set1_mask, uint16_t set2_mask, uint16_t en_mask)
```

!!! summary "引数"
	- uint16_t `set1_mask` bitmask touch sensor signal group1, it's a 10-bit value 
	- uint16_t `set2_mask` bitmask touch sensor signal group2, it's a 10-bit value 
	- uint16_t `en_mask` bitmask of touch sensor work enable, it's a 10-bit value 

!!! note "戻り値"
	esp_err_t 




### touch_pad_clear_status()
To clear the touch status register, usually use this function in touch ISR to clear status.



```c
esp_err_t touch_pad_clear_status()
```

!!! note "戻り値"
	esp_err_t 




### touch_pad_get_status()
Get the touch sensor status, usually used in ISR to decide which pads are 'touched'.



```c
uint32_t touch_pad_get_status()
```

!!! note "戻り値"
	uint32_t 




### touch_pad_intr_enable()
To enable touch pad interrupt



```c
esp_err_t touch_pad_intr_enable()
```

!!! note "戻り値"
	esp_err_t 




### touch_pad_intr_disable()
To disable touch pad interrupt



```c
esp_err_t touch_pad_intr_disable()
```

!!! note "戻り値"
	esp_err_t 




### touch_pad_set_filter_period()
set touch pad filter calibration period, in ms. Need to call touch_pad_filter_start before all touch filter APIs


```c
esp_err_t touch_pad_set_filter_period(uint32_t new_period_ms)
```

!!! summary "引数"
	- uint32_t `new_period_ms` filter period, in ms 

!!! note "戻り値"
	esp_err_t 




### touch_pad_get_filter_period()
get touch pad filter calibration period, in ms Need to call touch_pad_filter_start before all touch filter APIs


```c
esp_err_t touch_pad_get_filter_period(uint32_t *p_period_ms)
```

!!! summary "引数"
	- uint32_t * `p_period_ms` pointer to accept period 

!!! note "戻り値"
	esp_err_t 




### touch_pad_filter_start()
start touch pad filter function This API will start a filter to process the noise in order to prevent false triggering when detecting slight change of capacitance. Need to call touch_pad_filter_start before all touch filter APIs


```c
esp_err_t touch_pad_filter_start(uint32_t filter_period_ms)
```

!!! summary "引数"
	- uint32_t `filter_period_ms` filter calibration period, in ms 

!!! note "戻り値"
	esp_err_t



### touch_pad_filter_stop()
stop touch pad filter function Need to call touch_pad_filter_start before all touch filter APIs



```c
esp_err_t touch_pad_filter_stop()
```

!!! note "戻り値"
	esp_err_t 




### touch_pad_filter_delete()
delete touch pad filter driver and release the memory Need to call touch_pad_filter_start before all touch filter APIs



```c
esp_err_t touch_pad_filter_delete()
```

!!! note "戻り値"
	esp_err_t 




### touch_pad_get_wakeup_status()
Get the touch pad which caused wakeup from sleep


```c
esp_err_t touch_pad_get_wakeup_status(touch_pad_t *pad_num)
```

!!! summary "引数"
	- touch_pad_t* `pad_num` pointer to touch pad which caused wakeup 

!!! note "戻り値"
	esp_err_t 




