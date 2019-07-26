# mcpwm

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/mcpwm.h>
```

上記宣言で利用できます。

## メンバー

































### mcpwm_gpio_init()
This function initializes each gpio signal for MCPWM


```c
esp_err_t mcpwm_gpio_init(mcpwm_unit_t mcpwm_num, mcpwm_io_signals_t io_signal, int gpio_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_io_signals_t `io_signal` set MCPWM signals, each MCPWM unit has 6 output(MCPWMXA, MCPWMXB) and 9 input(SYNC_X, FAULT_X, CAP_X) 'X' is timer_num(0-2) 
	- int `gpio_num` set this to configure gpio for MCPWM, if you want to use gpio16, gpio_num = 16

!!! note "戻り値"
	esp_err_t



### mcpwm_set_pin()
Initialize MCPWM gpio structure


```c
esp_err_t mcpwm_set_pin(mcpwm_unit_t mcpwm_num, const mcpwm_pin_config_t *mcpwm_pin)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_pin_config_tconst  * `mcpwm_pin` MCPWM pin structure

!!! note "戻り値"
	esp_err_t



### mcpwm_init()
Initialize MCPWM parameters


```c
esp_err_t mcpwm_init(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, const mcpwm_config_t *mcpwm_conf)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_config_tconst  * `mcpwm_conf` configure structure 

!!! note "戻り値"
	esp_err_t 




### mcpwm_set_frequency()
Set frequency(in Hz) of MCPWM timer


```c
esp_err_t mcpwm_set_frequency(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, uint32_t frequency)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- uint32_t `frequency` set the frequency in Hz of each timer

!!! note "戻り値"
	esp_err_t 




### mcpwm_set_duty()
Set duty cycle of each operator(MCPWMXA/MCPWMXB)


```c
esp_err_t mcpwm_set_duty(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, mcpwm_operator_t op_num, float duty)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_operator_t `op_num` set the operator(MCPWMXA/MCPWMXB), 'X' is timer number selected 
	- float `duty` set duty cycle in %(i.e for 62.3% duty cycle, duty = 62.3) of each operator

!!! note "戻り値"
	esp_err_t 




### mcpwm_set_duty_in_us()
Set duty cycle of each operator(MCPWMXA/MCPWMXB) in us


```c
esp_err_t mcpwm_set_duty_in_us(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, mcpwm_operator_t op_num, uint32_t duty)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_operator_t `op_num` set the operator(MCPWMXA/MCPWMXB), 'x' is timer number selected 
	- uint32_t `duty` set duty value in microseconds of each operator

!!! note "戻り値"
	esp_err_t 




### mcpwm_set_duty_type()
Set duty either active high or active low(out of phase/inverted)


```c
esp_err_t mcpwm_set_duty_type(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, mcpwm_operator_t op_num, mcpwm_duty_type_t duty_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_operator_t `op_num` set the operator(MCPWMXA/MCPWMXB), 'x' is timer number selected 
	- mcpwm_duty_type_t `duty_num` set active low or active high duty type

!!! note "戻り値"
	esp_err_t



### mcpwm_get_frequency()
Get frequency of timer


```c
uint32_t mcpwm_get_frequency(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers

!!! note "戻り値"
	uint32_t 




### mcpwm_get_duty()
Get duty cycle of each operator


```c
float mcpwm_get_duty(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, mcpwm_operator_t op_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_operator_t `op_num` set the operator(MCPWMXA/MCPWMXB), 'x' is timer number selected

!!! note "戻り値"
	float 




### mcpwm_set_signal_high()
Use this function to set MCPWM signal high


```c
esp_err_t mcpwm_set_signal_high(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, mcpwm_operator_t op_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_operator_t `op_num` set the operator(MCPWMXA/MCPWMXB), 'x' is timer number selected

!!! note "戻り値"
	esp_err_t 




### mcpwm_set_signal_low()
Use this function to set MCPWM signal low


```c
esp_err_t mcpwm_set_signal_low(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, mcpwm_operator_t op_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_operator_t `op_num` set the operator(MCPWMXA/MCPWMXB), 'x' is timer number selected

!!! note "戻り値"
	esp_err_t 




### mcpwm_start()
Start MCPWM signal on timer 'x'


```c
esp_err_t mcpwm_start(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers

!!! note "戻り値"
	esp_err_t 




### mcpwm_stop()
Start MCPWM signal on timer 'x'


```c
esp_err_t mcpwm_stop(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers

!!! note "戻り値"
	esp_err_t 




### mcpwm_carrier_init()
Initialize carrier configuration


```c
esp_err_t mcpwm_carrier_init(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, const mcpwm_carrier_config_t *carrier_conf)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_carrier_config_tconst  * `carrier_conf` configure structure 

!!! note "戻り値"
	esp_err_t 




### mcpwm_carrier_enable()
Enable MCPWM carrier submodule, for respective timer


```c
esp_err_t mcpwm_carrier_enable(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers

!!! note "戻り値"
	esp_err_t 




### mcpwm_carrier_disable()
Disable MCPWM carrier submodule, for respective timer


```c
esp_err_t mcpwm_carrier_disable(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers

!!! note "戻り値"
	esp_err_t 




### mcpwm_carrier_set_period()
Set period of carrier


```c
esp_err_t mcpwm_carrier_set_period(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, uint8_t carrier_period)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- uint8_t `carrier_period` set the carrier period of each timer, carrier period = (carrier_period + 1)*800ns (carrier_period <= 15)

!!! note "戻り値"
	esp_err_t 




### mcpwm_carrier_set_duty_cycle()
Set duty_cycle of carrier


```c
esp_err_t mcpwm_carrier_set_duty_cycle(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, uint8_t carrier_duty)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- uint8_t `carrier_duty` set duty_cycle of carrier , carrier duty cycle = carrier_duty*12.5% (chop_duty <= 7)

!!! note "戻り値"
	esp_err_t 




### mcpwm_carrier_oneshot_mode_enable()
Enable and set width of first pulse in carrier oneshot mode


```c
esp_err_t mcpwm_carrier_oneshot_mode_enable(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, uint8_t pulse_width)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- uint8_t `pulse_width` set pulse width of first pulse in oneshot mode, width = (carrier period)*(pulse_width +1) (pulse_width <= 15)

!!! note "戻り値"
	esp_err_t 




### mcpwm_carrier_oneshot_mode_disable()
Disable oneshot mode, width of first pulse = carrier period


```c
esp_err_t mcpwm_carrier_oneshot_mode_disable(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers

!!! note "戻り値"
	esp_err_t 




### mcpwm_carrier_output_invert()
Enable or disable carrier output inversion


```c
esp_err_t mcpwm_carrier_output_invert(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, mcpwm_carrier_out_ivt_t carrier_ivt_mode)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_carrier_out_ivt_t `carrier_ivt_mode` enable or disable carrier output inversion

!!! note "戻り値"
	esp_err_t 




### mcpwm_deadtime_enable()
Enable and initialize deadtime for each MCPWM timer


```c
esp_err_t mcpwm_deadtime_enable(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, mcpwm_deadtime_type_t dt_mode, uint32_t red, uint32_t fed)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_deadtime_type_t `dt_mode` set deadtime mode 
	- uint32_t `red` set rising edge delay = red*100ns 
	- uint32_t `fed` set rising edge delay = fed*100ns

!!! note "戻り値"
	esp_err_t 




### mcpwm_deadtime_disable()
Disable deadtime on MCPWM timer


```c
esp_err_t mcpwm_deadtime_disable(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers

!!! note "戻り値"
	esp_err_t 




### mcpwm_fault_init()
Initialize fault submodule, currently low level triggering is not supported


```c
esp_err_t mcpwm_fault_init(mcpwm_unit_t mcpwm_num, mcpwm_fault_input_level_t intput_level, mcpwm_fault_signal_t fault_sig)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_fault_input_level_t `intput_level` set fault signal level, which will cause fault to occur 
	- mcpwm_fault_signal_t `fault_sig` set the fault pin, which needs to be enabled

!!! note "戻り値"
	esp_err_t 




### mcpwm_fault_set_oneshot_mode()
Set oneshot mode on fault detection, once fault occur in oneshot mode reset is required to resume MCPWM signals


```c
esp_err_t mcpwm_fault_set_oneshot_mode(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, mcpwm_fault_signal_t fault_sig, mcpwm_action_on_pwmxa_t action_on_pwmxa, mcpwm_action_on_pwmxb_t action_on_pwmxb)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_fault_signal_t `fault_sig` set the fault pin, which needs to be enabled for oneshot mode 
	- mcpwm_action_on_pwmxa_t `action_on_pwmxa` action to be taken on MCPWMXA when fault occurs, either no change or high or low or toggle 
	- mcpwm_action_on_pwmxb_t `action_on_pwmxb` action to be taken on MCPWMXB when fault occurs, either no change or high or low or toggle

!!! note "戻り値"
	esp_err_t



### mcpwm_fault_set_cyc_mode()
Set cycle-by-cycle mode on fault detection, once fault occur in cyc mode MCPWM signal resumes as soon as fault signal becomes inactive


```c
esp_err_t mcpwm_fault_set_cyc_mode(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, mcpwm_fault_signal_t fault_sig, mcpwm_action_on_pwmxa_t action_on_pwmxa, mcpwm_action_on_pwmxb_t action_on_pwmxb)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_fault_signal_t `fault_sig` set the fault pin, which needs to be enabled for cyc mode 
	- mcpwm_action_on_pwmxa_t `action_on_pwmxa` action to be taken on MCPWMXA when fault occurs, either no change or high or low or toggle 
	- mcpwm_action_on_pwmxb_t `action_on_pwmxb` action to be taken on MCPWMXB when fault occurs, either no change or high or low or toggle

!!! note "戻り値"
	esp_err_t



### mcpwm_fault_deinit()
Disable fault signal


```c
esp_err_t mcpwm_fault_deinit(mcpwm_unit_t mcpwm_num, mcpwm_fault_signal_t fault_sig)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_fault_signal_t `fault_sig` fault pin, which needs to be disabled

!!! note "戻り値"
	esp_err_t 




### mcpwm_capture_enable()
Initialize capture submodule


```c
esp_err_t mcpwm_capture_enable(mcpwm_unit_t mcpwm_num, mcpwm_capture_signal_t cap_sig, mcpwm_capture_on_edge_t cap_edge, uint32_t num_of_pulse)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_capture_signal_t `cap_sig` capture pin, which needs to be enabled 
	- mcpwm_capture_on_edge_t `cap_edge` set capture edge, BIT(0) - negative edge, BIT(1) - positive edge 
	- uint32_t `num_of_pulse` count time between rising/falling edge between 2 *(pulses mentioned), counter uses APB_CLK

!!! note "戻り値"
	esp_err_t 




### mcpwm_capture_disable()
Disable capture signal


```c
esp_err_t mcpwm_capture_disable(mcpwm_unit_t mcpwm_num, mcpwm_capture_signal_t cap_sig)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_capture_signal_t `cap_sig` capture pin, which needs to be disabled

!!! note "戻り値"
	esp_err_t 




### mcpwm_capture_signal_get_value()
Get capture value


```c
uint32_t mcpwm_capture_signal_get_value(mcpwm_unit_t mcpwm_num, mcpwm_capture_signal_t cap_sig)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_capture_signal_t `cap_sig` capture pin on which value is to be measured

!!! note "戻り値"
	uint32_t Captured value 



### mcpwm_capture_signal_get_edge()
Get edge of capture signal


```c
uint32_t mcpwm_capture_signal_get_edge(mcpwm_unit_t mcpwm_num, mcpwm_capture_signal_t cap_sig)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_capture_signal_t `cap_sig` capture pin of whose edge is to be determined

!!! note "戻り値"
	uint32_t Capture signal edge: 1 - positive edge, 2 - negtive edge 



### mcpwm_sync_enable()
Initialize sync submodule


```c
esp_err_t mcpwm_sync_enable(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num, mcpwm_sync_signal_t sync_sig, uint32_t phase_val)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers 
	- mcpwm_sync_signal_t `sync_sig` set the synchronization pin, which needs to be enabled 
	- uint32_t `phase_val` phase value in 1/1000 (for 86.7%, phase_val = 867) which timer moves to on sync signal

!!! note "戻り値"
	esp_err_t 




### mcpwm_sync_disable()
Disable sync submodule on given timer


```c
esp_err_t mcpwm_sync_disable(mcpwm_unit_t mcpwm_num, mcpwm_timer_t timer_num)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- mcpwm_timer_t `timer_num` set timer number(0-2) of MCPWM, each MCPWM unit has 3 timers

!!! note "戻り値"
	esp_err_t 




### mcpwm_isr_register()
Register MCPWM interrupt handler, the handler is an ISR. the handler will be attached to the same CPU core that this function is running on.


```c
esp_err_t mcpwm_isr_register(mcpwm_unit_t mcpwm_num, void(*fn)(void *), void *arg, int intr_alloc_flags, intr_handle_t *handle)
```

!!! summary "引数"
	- mcpwm_unit_t `mcpwm_num` set MCPWM unit(0-1) 
	- void(*)(void *) `fn` interrupt handler function. 
	- void * `arg` parameter for handler function 
	- int `intr_alloc_flags` flags used to allocate the interrupt. One or multiple (ORred) ESP_INTR_FLAG_* values. see esp_intr_alloc.h for more info. 
	- intr_handle_t * `handle` pointer to return handle. If non-NULL, a handle for the interrupt will be returned here.

!!! note "戻り値"
	esp_err_t 




