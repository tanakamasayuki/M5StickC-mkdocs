# gpio

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/gpio.h>
```

上記宣言で利用できます。

## メンバー





























### gpio_config()
GPIO common configuration


```c
esp_err_t gpio_config(const gpio_config_t *pGPIOConfig)
```

!!! summary "引数"
	- gpio_config_tconst  * `pGPIOConfig` Pointer to GPIO configure struct

!!! note "戻り値"
	esp_err_t



### gpio_reset_pin()
Reset an gpio to default state (select gpio function, enable pullup and disable input and output).


```c
esp_err_t gpio_reset_pin(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number.

!!! note "戻り値"
	esp_err_t



### gpio_set_intr_type()
GPIO set interrupt trigger type


```c
esp_err_t gpio_set_intr_type(gpio_num_t gpio_num, gpio_int_type_t intr_type)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number. If you want to set the trigger type of e.g. of GPIO16, gpio_num should be GPIO_NUM_16 (16); 
	- gpio_int_type_t `intr_type` Interrupt type, select from gpio_int_type_t

!!! note "戻り値"
	esp_err_t 




### gpio_intr_enable()
Enable GPIO module interrupt signal


```c
esp_err_t gpio_intr_enable(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number. If you want to enable an interrupt on e.g. GPIO16, gpio_num should be GPIO_NUM_16 (16);

!!! note "戻り値"
	esp_err_t



### gpio_intr_disable()
Disable GPIO module interrupt signal


```c
esp_err_t gpio_intr_disable(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number. If you want to disable the interrupt of e.g. GPIO16, gpio_num should be GPIO_NUM_16 (16);

!!! note "戻り値"
	esp_err_t 




### gpio_set_level()
GPIO set output level


```c
esp_err_t gpio_set_level(gpio_num_t gpio_num, uint32_t level)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number. If you want to set the output level of e.g. GPIO16, gpio_num should be GPIO_NUM_16 (16); 
	- uint32_t `level` Output level. 0: low ; 1: high

!!! note "戻り値"
	esp_err_t 




### gpio_get_level()
GPIO get input level


```c
int gpio_get_level(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number. If you want to get the logic level of e.g. pin GPIO16, gpio_num should be GPIO_NUM_16 (16);

!!! note "戻り値"
	int



### gpio_set_direction()
GPIO set direction

Configure GPIO direction,such as output_only,input_only,output_and_input
```c
esp_err_t gpio_set_direction(gpio_num_t gpio_num, gpio_mode_t mode)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` Configure GPIO pins number, it should be GPIO number. If you want to set direction of e.g. GPIO16, gpio_num should be GPIO_NUM_16 (16); 
	- gpio_mode_t `mode` GPIO direction

!!! note "戻り値"
	esp_err_t



### gpio_set_pull_mode()
Configure GPIO pull-up/pull-down resistors

Only pins that support both input & output have integrated pull-up and pull-down resistors. Input-only GPIOs 34-39 do not.
```c
esp_err_t gpio_set_pull_mode(gpio_num_t gpio_num, gpio_pull_mode_t pull)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number. If you want to set pull up or down mode for e.g. GPIO16, gpio_num should be GPIO_NUM_16 (16); 
	- gpio_pull_mode_t `pull` GPIO pull up/down mode.

!!! note "戻り値"
	esp_err_t



### gpio_wakeup_enable()
Enable GPIO wake-up function.


```c
esp_err_t gpio_wakeup_enable(gpio_num_t gpio_num, gpio_int_type_t intr_type)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number.
	- gpio_int_type_t `intr_type` GPIO wake-up type. Only GPIO_INTR_LOW_LEVEL or GPIO_INTR_HIGH_LEVEL can be used.

!!! note "戻り値"
	esp_err_t 




### gpio_wakeup_disable()
Disable GPIO wake-up function.


```c
esp_err_t gpio_wakeup_disable(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number

!!! note "戻り値"
	esp_err_t 




### gpio_isr_register()
Register GPIO interrupt handler, the handler is an ISR. The handler will be attached to the same CPU core that this function is running on.



```c
esp_err_t gpio_isr_register(void(*fn)(void *), void *arg, int intr_alloc_flags, gpio_isr_handle_t *handle)
```

!!! summary "引数"
	- void(*)(void *) `fn` Interrupt handler function. 
	- void * `arg` Parameter for handler function 
	- int `intr_alloc_flags` Flags used to allocate the interrupt. One or multiple (ORred) ESP_INTR_FLAG_* values. See esp_intr_alloc.h for more info. 
	- gpio_isr_handle_t* `handle` Pointer to return handle. If non-NULL, a handle for the interrupt will be returned here.

!!! note "戻り値"
	esp_err_t



### gpio_pullup_en()
Enable pull-up on GPIO.


```c
esp_err_t gpio_pullup_en(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number

!!! note "戻り値"
	esp_err_t 




### gpio_pullup_dis()
Disable pull-up on GPIO.


```c
esp_err_t gpio_pullup_dis(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number

!!! note "戻り値"
	esp_err_t 




### gpio_pulldown_en()
Enable pull-down on GPIO.


```c
esp_err_t gpio_pulldown_en(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number

!!! note "戻り値"
	esp_err_t 




### gpio_pulldown_dis()
Disable pull-down on GPIO.


```c
esp_err_t gpio_pulldown_dis(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number

!!! note "戻り値"
	esp_err_t 




### gpio_install_isr_service()
Install the driver's GPIO ISR handler service, which allows per-pin GPIO interrupt handlers.

This function is incompatible with  - if that function is used, a single global ISR is registered for all GPIO interrupts. If this function is used, the ISR service provides a global GPIO ISR and individual pin handlers are registered via the  function.
```c
esp_err_t gpio_install_isr_service(int intr_alloc_flags)
```

!!! summary "引数"
	- int `intr_alloc_flags` Flags used to allocate the interrupt. One or multiple (ORred) ESP_INTR_FLAG_* values. See esp_intr_alloc.h for more info.

!!! note "戻り値"
	esp_err_t



### gpio_uninstall_isr_service()
Uninstall the driver's GPIO ISR service, freeing related resources.


```c
void gpio_uninstall_isr_service()
```

!!! note "戻り値"
	void



### gpio_isr_handler_add()
Add ISR handler for the corresponding GPIO pin.

This ISR handler will be called from an ISR. So there is a stack size limit (configurable as "ISR stack size" in menuconfig). This limit is smaller compared to a global GPIO interrupt handler due to the additional level of indirection.
```c
esp_err_t gpio_isr_handler_add(gpio_num_t gpio_num, gpio_isr_t isr_handler, void *args)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number 
	- gpio_isr_t `isr_handler` ISR handler function for the corresponding GPIO number. 
	- void * `args` parameter for ISR handler.

!!! note "戻り値"
	esp_err_t



### gpio_isr_handler_remove()
Remove ISR handler for the corresponding GPIO pin.


```c
esp_err_t gpio_isr_handler_remove(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number

!!! note "戻り値"
	esp_err_t 




### gpio_set_drive_capability()
Set GPIO pad drive capability


```c
esp_err_t gpio_set_drive_capability(gpio_num_t gpio_num, gpio_drive_cap_t strength)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number, only support output GPIOs 
	- gpio_drive_cap_t `strength` Drive capability of the pad

!!! note "戻り値"
	esp_err_t 




### gpio_get_drive_capability()
Get GPIO pad drive capability


```c
esp_err_t gpio_get_drive_capability(gpio_num_t gpio_num, gpio_drive_cap_t *strength)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number, only support output GPIOs 
	- gpio_drive_cap_t* `strength` Pointer to accept drive capability of the pad

!!! note "戻り値"
	esp_err_t 




### gpio_hold_en()
Enable gpio pad hold function.

Power down or call gpio_hold_dis will disable this function.
```c
esp_err_t gpio_hold_en(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number, only support output-capable GPIOs

!!! note "戻り値"
	esp_err_t



### gpio_hold_dis()
Disable gpio pad hold function.

When the chip is woken up from Deep-sleep, the gpio will be set to the default mode, so, the gpio will output the default level if this function is called. If you dont't want the level changes, the gpio should be configured to a known state before this function is called. e.g. If you hold gpio18 high during Deep-sleep, after the chip is woken up and  is called, gpio18 will output low level(because gpio18 is input mode by default). If you don't want this behavior, you should configure gpio18 as output mode and set it to hight level before calling .
```c
esp_err_t gpio_hold_dis(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number, only support output-capable GPIOs

!!! note "戻り値"
	esp_err_t



### gpio_deep_sleep_hold_en()
Enable all digital gpio pad hold function during Deep-sleep.

Power down or call gpio_hold_dis will disable this function, otherwise, the digital gpio hold feature works as long as the chip enter Deep-sleep. 
```c
void gpio_deep_sleep_hold_en(void)
```

!!! note "戻り値"
	void



### gpio_deep_sleep_hold_dis()
Disable all digital gpio pad hold function during Deep-sleep.


```c
void gpio_deep_sleep_hold_dis(void)
```

!!! note "戻り値"
	void



### gpio_iomux_in()
Set pad input to a peripheral signal through the IOMUX.


```c
void gpio_iomux_in(uint32_t gpio_num, uint32_t signal_idx)
```

!!! summary "引数"
	- uint32_t `gpio_num` GPIO number of the pad. 
	- uint32_t `signal_idx` Peripheral signal id to input. One of the  signals in . 

!!! note "戻り値"
	void



### gpio_iomux_out()
Set peripheral output to an GPIO pad through the IOMUX.


```c
void gpio_iomux_out(uint8_t gpio_num, int func, bool oen_inv)
```

!!! summary "引数"
	- uint8_t `gpio_num` gpio_num GPIO number of the pad. 
	- int `func` The function number of the peripheral pin to output pin. One of the  of specified pin (X) in . 
	- bool `oen_inv` True if the output enable needs to be inversed, otherwise False. 

!!! note "戻り値"
	void



