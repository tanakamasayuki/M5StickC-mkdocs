# esp_sleep



## メンバー













###  deprecated

```c
void deprecated
```


### esp_sleep_disable_wakeup_source()
Disable wakeup source


See docs/sleep-modes.rst for details.
```c
esp_err_t esp_sleep_disable_wakeup_source(esp_sleep_source_t source)
```

!!! summary "引数"
	- esp_sleep_source_t `source` - number of source to disable of type esp_sleep_source_t 

!!! note "戻り値"
	esp_err_t



### esp_sleep_enable_ulp_wakeup()
Enable wakeup by ULP coprocessor




```c
esp_err_t esp_sleep_enable_ulp_wakeup()
```

!!! note "戻り値"
	esp_err_t



### esp_sleep_enable_timer_wakeup()
Enable wakeup by timer


```c
esp_err_t esp_sleep_enable_timer_wakeup(uint64_t time_in_us)
```

!!! summary "引数"
	- uint64_t `time_in_us` time before wakeup, in microseconds 

!!! note "戻り値"
	esp_err_t 




### esp_sleep_enable_touchpad_wakeup()
Enable wakeup by touch sensor





```c
esp_err_t esp_sleep_enable_touchpad_wakeup()
```

!!! note "戻り値"
	esp_err_t



### esp_sleep_get_touchpad_wakeup_status()
Get the touch pad which caused wakeup



```c
touch_pad_t esp_sleep_get_touchpad_wakeup_status()
```

!!! note "戻り値"
	touch_pad_t



### esp_sleep_enable_ext0_wakeup()
Enable wakeup using a pin

This feature can monitor any pin which is an RTC IO. Once the pin transitions into the state given by level argument, the chip will be woken up.
```c
esp_err_t esp_sleep_enable_ext0_wakeup(gpio_num_t gpio_num, int level)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number used as wakeup source. Only GPIOs which are have RTC functionality can be used: 0,2,4,12-15,25-27,32-39. 
	- int `level` input level which will trigger wakeup (0=low, 1=high) 

!!! note "戻り値"
	esp_err_t



### esp_sleep_enable_ext1_wakeup()
Enable wakeup using multiple pins

This feature can monitor any number of pins which are in RTC IOs. Once any of the selected pins goes into the state given by mode argument, the chip will be woken up.
```c
esp_err_t esp_sleep_enable_ext1_wakeup(uint64_t mask, esp_sleep_ext1_wakeup_mode_t mode)
```

!!! summary "引数"
	- uint64_t `mask` bit mask of GPIO numbers which will cause wakeup. Only GPIOs which are have RTC functionality can be used in this bit map: 0,2,4,12-15,25-27,32-39. 
	- esp_sleep_ext1_wakeup_mode_t `mode` select logic function used to determine wakeup condition:


!!! note "戻り値"
	esp_err_t



### esp_sleep_enable_gpio_wakeup()
Enable wakeup from light sleep using GPIOs




```c
esp_err_t esp_sleep_enable_gpio_wakeup()
```

!!! note "戻り値"
	esp_err_t



### esp_sleep_enable_uart_wakeup()
Enable wakeup from light sleep using UART

Wakeup from light sleep takes some time, so not every character sent to the UART can be received by the application.
```c
esp_err_t esp_sleep_enable_uart_wakeup(int uart_num)
```

!!! summary "引数"
	- int `uart_num` UART port to wake up from 

!!! note "戻り値"
	esp_err_t



### esp_sleep_get_ext1_wakeup_status()
Get the bit mask of GPIOs which caused wakeup (ext1)



```c
uint64_t esp_sleep_get_ext1_wakeup_status()
```

!!! note "戻り値"
	uint64_t



### esp_sleep_pd_config()
Set power down mode for an RTC power domain in sleep mode

If not set set using this API, all power domains default to ESP_PD_OPTION_AUTO.
```c
esp_err_t esp_sleep_pd_config(esp_sleep_pd_domain_t domain, esp_sleep_pd_option_t option)
```

!!! summary "引数"
	- esp_sleep_pd_domain_t `domain` power domain to configure 
	- esp_sleep_pd_option_t `option` power down option (ESP_PD_OPTION_OFF, ESP_PD_OPTION_ON, or ESP_PD_OPTION_AUTO) 

!!! note "戻り値"
	esp_err_t



### esp_deep_sleep_start()
Enter deep sleep with the configured wakeup options

This function does not return. 
```c
void esp_deep_sleep_start() __attribute__((noreturn))
```

!!! note "戻り値"
	void



### esp_light_sleep_start()
Enter light sleep with the configured wakeup options



```c
esp_err_t esp_light_sleep_start()
```

!!! note "戻り値"
	esp_err_t 




### esp_deep_sleep()
Enter deep-sleep mode

This function does not return.
```c
void esp_deep_sleep(uint64_t time_in_us) __attribute__((noreturn))
```

!!! summary "引数"
	- uint64_t `time_in_us` deep-sleep time, unit: microsecond 

!!! note "戻り値"
	void



### system_deep_sleep()
Enter deep-sleep mode

Function has been renamed to esp_deep_sleep. This name is deprecated and will be removed in a future version.
```c
void system_deep_sleep(uint64_t time_in_us) __attribute__((noreturn
```

!!! summary "引数"
	- uint64_t `time_in_us` deep-sleep time, unit: microsecond 

!!! note "戻り値"
	void



### esp_sleep_get_wakeup_cause()
Get the wakeup source which caused wakeup from sleep



```c
esp_sleep_wakeup_cause_t esp_sleep_get_wakeup_cause()
```

!!! note "戻り値"
	esp_sleep_wakeup_cause_t cause of wake up from last sleep (deep sleep or light sleep) 



### esp_wake_deep_sleep()
Default stub to run on wake from deep sleep.

See docs/deep-sleep-stub.rst for details. 
```c
void esp_wake_deep_sleep(void)
```

!!! note "戻り値"
	void



### esp_set_deep_sleep_wake_stub()
Install a new stub at runtime to run on wake from deep sleep

However, it is possible to call this function to substitute a different deep sleep stub. Any function used as a deep sleep stub must be marked RTC_IRAM_ATTR, and must obey the same rules given for . 
```c
void esp_set_deep_sleep_wake_stub(esp_deep_sleep_wake_stub_fn_t new_stub)
```

!!! summary "引数"
	- esp_deep_sleep_wake_stub_fn_t `new_stub` 

!!! note "戻り値"
	void



### esp_get_deep_sleep_wake_stub()
Get current wake from deep sleep stub



```c
esp_deep_sleep_wake_stub_fn_t esp_get_deep_sleep_wake_stub(void)
```

!!! note "戻り値"
	esp_deep_sleep_wake_stub_fn_t Return current wake from deep sleep stub, or NULL if no stub is installed. 



### esp_default_wake_deep_sleep()
The default esp-idf-provided  stub.

See docs/deep-sleep-stub.rst for details. 
```c
void esp_default_wake_deep_sleep(void)
```

!!! note "戻り値"
	void



### esp_deep_sleep_disable_rom_logging()
Disable logging from the ROM code after deep sleep.

Using LSB of RTC_STORE4. 
```c
void esp_deep_sleep_disable_rom_logging(void)
```

!!! note "戻り値"
	void



