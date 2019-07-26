# ledc

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/ledc.h>
```

上記宣言で利用できます。

## メンバー



























### ledc_channel_config()
LEDC channel configuration Configure LEDC channel with the given channel/output gpio_num/interrupt/source timer/frequency(Hz)/LEDC duty resolution


```c
esp_err_t ledc_channel_config(const ledc_channel_config_t *ledc_conf)
```

!!! summary "引数"
	- ledc_channel_config_tconst  * `ledc_conf` Pointer of LEDC channel configure struct

!!! note "戻り値"
	esp_err_t 




### ledc_timer_config()
LEDC timer configuration Configure LEDC timer with the given source timer/frequency(Hz)/duty_resolution


```c
esp_err_t ledc_timer_config(const ledc_timer_config_t *timer_conf)
```

!!! summary "引数"
	- ledc_timer_config_tconst  * `timer_conf` Pointer of LEDC timer configure struct

!!! note "戻り値"
	esp_err_t 




### ledc_update_duty()
LEDC update channel parameters


```c
esp_err_t ledc_update_duty(ledc_mode_t speed_mode, ledc_channel_t channel)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode, 
	- ledc_channel_t `channel` LEDC channel (0-7), select from ledc_channel_t

!!! note "戻り値"
	esp_err_t



### ledc_stop()
LEDC stop. Disable LEDC output, and set idle level


```c
esp_err_t ledc_stop(ledc_mode_t speed_mode, ledc_channel_t channel, uint32_t idle_level)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- ledc_channel_t `channel` LEDC channel (0-7), select from ledc_channel_t 
	- uint32_t `idle_level` Set output idle level after LEDC stops.

!!! note "戻り値"
	esp_err_t 




### ledc_set_freq()
LEDC set channel frequency (Hz)


```c
esp_err_t ledc_set_freq(ledc_mode_t speed_mode, ledc_timer_t timer_num, uint32_t freq_hz)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- ledc_timer_t `timer_num` LEDC timer index (0-3), select from ledc_timer_t 
	- uint32_t `freq_hz` Set the LEDC frequency

!!! note "戻り値"
	esp_err_t 




### ledc_get_freq()
LEDC get channel frequency (Hz)


```c
uint32_t ledc_get_freq(ledc_mode_t speed_mode, ledc_timer_t timer_num)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- ledc_timer_t `timer_num` LEDC timer index (0-3), select from ledc_timer_t

!!! note "戻り値"
	uint32_t 




### ledc_set_duty_with_hpoint()
LEDC set duty and hpoint value Only after calling ledc_update_duty will the duty update.


```c
esp_err_t ledc_set_duty_with_hpoint(ledc_mode_t speed_mode, ledc_channel_t channel, uint32_t duty, uint32_t hpoint)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- ledc_channel_t `channel` LEDC channel (0-7), select from ledc_channel_t 
	- uint32_t `duty` Set the LEDC duty, the range of duty setting is [0, (2**duty_resolution)] 
	- uint32_t `hpoint` Set the LEDC hpoint value(max: 0xfffff)

!!! note "戻り値"
	esp_err_t



### ledc_get_hpoint()
LEDC get hpoint value, the counter value when the output is set high level.


```c
int ledc_get_hpoint(ledc_mode_t speed_mode, ledc_channel_t channel)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- ledc_channel_t `channel` LEDC channel (0-7), select from ledc_channel_t 

!!! note "戻り値"
	int 




### ledc_set_duty()
LEDC set duty This function do not change the hpoint value of this channel. if needed, please call ledc_set_duty_with_hpoint. only after calling ledc_update_duty will the duty update.


```c
esp_err_t ledc_set_duty(ledc_mode_t speed_mode, ledc_channel_t channel, uint32_t duty)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- ledc_channel_t `channel` LEDC channel (0-7), select from ledc_channel_t 
	- uint32_t `duty` Set the LEDC duty, the range of duty setting is [0, (2**duty_resolution)]

!!! note "戻り値"
	esp_err_t



### ledc_get_duty()
LEDC get duty


```c
uint32_t ledc_get_duty(ledc_mode_t speed_mode, ledc_channel_t channel)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- ledc_channel_t `channel` LEDC channel (0-7), select from ledc_channel_t

!!! note "戻り値"
	uint32_t 




### ledc_set_fade()
LEDC set gradient Set LEDC gradient, After the function calls the ledc_update_duty function, the function can take effect.


```c
esp_err_t ledc_set_fade(ledc_mode_t speed_mode, ledc_channel_t channel, uint32_t duty, ledc_duty_direction_t fade_direction, uint32_t step_num, uint32_t duty_cyle_num, uint32_t duty_scale)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- ledc_channel_t `channel` LEDC channel (0-7), select from ledc_channel_t 
	- uint32_t `duty` Set the start of the gradient duty, the range of duty setting is [0, (2**duty_resolution)] 
	- ledc_duty_direction_t `fade_direction` Set the direction of the gradient 
	- uint32_t `step_num` Set the number of the gradient 
	- uint32_t `duty_cyle_num` Set how many LEDC tick each time the gradient lasts 
	- uint32_t `duty_scale` Set gradient change amplitude

!!! note "戻り値"
	esp_err_t



### ledc_isr_register()
Register LEDC interrupt handler, the handler is an ISR. The handler will be attached to the same CPU core that this function is running on.


```c
esp_err_t ledc_isr_register(void(*fn)(void *), void *arg, int intr_alloc_flags, ledc_isr_handle_t *handle)
```

!!! summary "引数"
	- void(*)(void *) `fn` Interrupt handler function. 
	- void * `arg` Parameter for handler function 
	- int `intr_alloc_flags` Flags used to allocate the interrupt. One or multiple (ORred) ESP_INTR_FLAG_* values. See esp_intr_alloc.h for more info. 
	- ledc_isr_handle_t* `handle` Pointer to return handle. If non-NULL, a handle for the interrupt will be returned here.

!!! note "戻り値"
	esp_err_t 




### ledc_timer_set()
Configure LEDC settings


```c
esp_err_t ledc_timer_set(ledc_mode_t speed_mode, ledc_timer_t timer_sel, uint32_t clock_divider, uint32_t duty_resolution, ledc_clk_src_t clk_src)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- ledc_timer_t `timer_sel` Timer index (0-3), there are 4 timers in LEDC module 
	- uint32_t `clock_divider` Timer clock divide value, the timer clock is divided from the selected clock source 
	- uint32_t `duty_resolution` Resolution of duty setting in number of bits. The range of duty values is [0, (2**duty_resolution)] 
	- ledc_clk_src_t `clk_src` Select LEDC source clock.

!!! note "戻り値"
	esp_err_t 




### ledc_timer_rst()
Reset LEDC timer


```c
esp_err_t ledc_timer_rst(ledc_mode_t speed_mode, uint32_t timer_sel)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- uint32_t `timer_sel` LEDC timer index (0-3), select from ledc_timer_t

!!! note "戻り値"
	esp_err_t 




### ledc_timer_pause()
Pause LEDC timer counter


```c
esp_err_t ledc_timer_pause(ledc_mode_t speed_mode, uint32_t timer_sel)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- uint32_t `timer_sel` LEDC timer index (0-3), select from ledc_timer_t

!!! note "戻り値"
	esp_err_t 




### ledc_timer_resume()
Resume LEDC timer


```c
esp_err_t ledc_timer_resume(ledc_mode_t speed_mode, uint32_t timer_sel)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- uint32_t `timer_sel` LEDC timer index (0-3), select from ledc_timer_t

!!! note "戻り値"
	esp_err_t 




### ledc_bind_channel_timer()
Bind LEDC channel with the selected timer


```c
esp_err_t ledc_bind_channel_timer(ledc_mode_t speed_mode, uint32_t channel, uint32_t timer_idx)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- uint32_t `channel` LEDC channel index (0-7), select from ledc_channel_t 
	- uint32_t `timer_idx` LEDC timer index (0-3), select from ledc_timer_t

!!! note "戻り値"
	esp_err_t 




### ledc_set_fade_with_step()
Set LEDC fade function.


```c
esp_err_t ledc_set_fade_with_step(ledc_mode_t speed_mode, ledc_channel_t channel, uint32_t target_duty, uint32_t scale, uint32_t cycle_num)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode, 
	- ledc_channel_t `channel` LEDC channel index (0-7), select from ledc_channel_t 
	- uint32_t `target_duty` Target duty of fading [0, (2**duty_resolution) - 1] 
	- uint32_t `scale` Controls the increase or decrease step scale. 
	- uint32_t `cycle_num` increase or decrease the duty every cycle_num cycles

!!! note "戻り値"
	esp_err_t



### ledc_set_fade_with_time()
Set LEDC fade function, with a limited time.


```c
esp_err_t ledc_set_fade_with_time(ledc_mode_t speed_mode, ledc_channel_t channel, uint32_t target_duty, int max_fade_time_ms)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode, 
	- ledc_channel_t `channel` LEDC channel index (0-7), select from ledc_channel_t 
	- uint32_t `target_duty` Target duty of fading.( 0 - (2 ** duty_resolution - 1))) 
	- int `max_fade_time_ms` The maximum time of the fading ( ms ).

!!! note "戻り値"
	esp_err_t



### ledc_fade_func_install()
Install LEDC fade function. This function will occupy interrupt of LEDC module.


```c
esp_err_t ledc_fade_func_install(int intr_alloc_flags)
```

!!! summary "引数"
	- int `intr_alloc_flags` Flags used to allocate the interrupt. One or multiple (ORred) ESP_INTR_FLAG_* values. See esp_intr_alloc.h for more info.

!!! note "戻り値"
	esp_err_t 




### ledc_fade_func_uninstall()
Uninstall LEDC fade function.


```c
void ledc_fade_func_uninstall()
```

!!! note "戻り値"
	void



### ledc_fade_start()
Start LEDC fading.


```c
esp_err_t ledc_fade_start(ledc_mode_t speed_mode, ledc_channel_t channel, ledc_fade_mode_t fade_mode)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- ledc_channel_t `channel` LEDC channel number 
	- ledc_fade_mode_t `fade_mode` Whether to block until fading done.

!!! note "戻り値"
	esp_err_t



### ledc_set_duty_and_update()
A thread-safe API to set duty for LEDC channel and return when duty updated.


```c
esp_err_t ledc_set_duty_and_update(ledc_mode_t speed_mode, ledc_channel_t channel, uint32_t duty, uint32_t hpoint)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode 
	- ledc_channel_t `channel` LEDC channel (0-7), select from ledc_channel_t 
	- uint32_t `duty` Set the LEDC duty, the range of duty setting is [0, (2**duty_resolution)] 
	- uint32_t `hpoint` Set the LEDC hpoint value(max: 0xfffff) 

!!! note "戻り値"
	esp_err_t



### ledc_set_fade_time_and_start()
A thread-safe API to set and start LEDC fade function, with a limited time.


```c
esp_err_t ledc_set_fade_time_and_start(ledc_mode_t speed_mode, ledc_channel_t channel, uint32_t target_duty, uint32_t max_fade_time_ms, ledc_fade_mode_t fade_mode)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode, 
	- ledc_channel_t `channel` LEDC channel index (0-7), select from ledc_channel_t 
	- uint32_t `target_duty` Target duty of fading.( 0 - (2 ** duty_resolution - 1))) 
	- uint32_t `max_fade_time_ms` The maximum time of the fading ( ms ). 
	- ledc_fade_mode_t `fade_mode` choose blocking or non-blocking mode 

!!! note "戻り値"
	esp_err_t



### ledc_set_fade_step_and_start()
A thread-safe API to set and start LEDC fade function.


```c
esp_err_t ledc_set_fade_step_and_start(ledc_mode_t speed_mode, ledc_channel_t channel, uint32_t target_duty, uint32_t scale, uint32_t cycle_num, ledc_fade_mode_t fade_mode)
```

!!! summary "引数"
	- ledc_mode_t `speed_mode` Select the LEDC speed_mode, high-speed mode and low-speed mode, 
	- ledc_channel_t `channel` LEDC channel index (0-7), select from ledc_channel_t 
	- uint32_t `target_duty` Target duty of fading [0, (2**duty_resolution) - 1] 
	- uint32_t `scale` Controls the increase or decrease step scale. 
	- uint32_t `cycle_num` increase or decrease the duty every cycle_num cycles 
	- ledc_fade_mode_t `fade_mode` choose blocking or non-blocking mode 

!!! note "戻り値"
	esp_err_t



