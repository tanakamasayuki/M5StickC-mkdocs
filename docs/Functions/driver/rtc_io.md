# rtc_io

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/rtc_io.h>
```

上記宣言で利用できます。

## メンバー





### rtc_gpio_is_valid_gpio()
Determine if the specified GPIO is a valid RTC GPIO.


```c
static bool rtc_gpio_is_valid_gpio(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number 

!!! note "戻り値"
	bool true if GPIO is valid for RTC GPIO use. false otherwise. 



### rtc_gpio_init()
Init a GPIO as RTC GPIO

This function must be called when initializing a pad for an analog function.
```c
esp_err_t rtc_gpio_init(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number (e.g. GPIO_NUM_12)

!!! note "戻り値"
	esp_err_t



### rtc_gpio_deinit()
Init a GPIO as digital GPIO


```c
esp_err_t rtc_gpio_deinit(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number (e.g. GPIO_NUM_12)

!!! note "戻り値"
	esp_err_t 




### rtc_gpio_get_level()
Get the RTC IO input level


```c
uint32_t rtc_gpio_get_level(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number (e.g. GPIO_NUM_12)

!!! note "戻り値"
	uint32_t 




### rtc_gpio_set_level()
Set the RTC IO output level


```c
esp_err_t rtc_gpio_set_level(gpio_num_t gpio_num, uint32_t level)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number (e.g. GPIO_NUM_12) 
	- uint32_t `level` output level

!!! note "戻り値"
	esp_err_t 




### rtc_gpio_set_direction()
RTC GPIO set direction

Configure RTC GPIO direction, such as output only, input only, output and input.
```c
esp_err_t rtc_gpio_set_direction(gpio_num_t gpio_num, rtc_gpio_mode_t mode)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number (e.g. GPIO_NUM_12) 
	- rtc_gpio_mode_t `mode` GPIO direction

!!! note "戻り値"
	esp_err_t



### rtc_gpio_pullup_en()
RTC GPIO pullup enable

This function only works for RTC IOs. In general, call gpio_pullup_en, which will work both for normal GPIOs and RTC IOs.
```c
esp_err_t rtc_gpio_pullup_en(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number (e.g. GPIO_NUM_12)

!!! note "戻り値"
	esp_err_t



### rtc_gpio_pulldown_en()
RTC GPIO pulldown enable

This function only works for RTC IOs. In general, call gpio_pulldown_en, which will work both for normal GPIOs and RTC IOs.
```c
esp_err_t rtc_gpio_pulldown_en(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number (e.g. GPIO_NUM_12)

!!! note "戻り値"
	esp_err_t



### rtc_gpio_pullup_dis()
RTC GPIO pullup disable

This function only works for RTC IOs. In general, call gpio_pullup_dis, which will work both for normal GPIOs and RTC IOs.
```c
esp_err_t rtc_gpio_pullup_dis(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number (e.g. GPIO_NUM_12)

!!! note "戻り値"
	esp_err_t



### rtc_gpio_pulldown_dis()
RTC GPIO pulldown disable

This function only works for RTC IOs. In general, call gpio_pulldown_dis, which will work both for normal GPIOs and RTC IOs.
```c
esp_err_t rtc_gpio_pulldown_dis(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number (e.g. GPIO_NUM_12)

!!! note "戻り値"
	esp_err_t



### rtc_gpio_hold_en()
Enable hold function on an RTC IO pad

Enabling HOLD function will cause the pad to latch current values of input enable, output enable, output value, function, drive strength values. This function is useful when going into light or deep sleep mode to prevent the pin configuration from changing.
```c
esp_err_t rtc_gpio_hold_en(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number (e.g. GPIO_NUM_12) 

!!! note "戻り値"
	esp_err_t



### rtc_gpio_hold_dis()
Disable hold function on an RTC IO pad

Disabling hold function will allow the pad receive the values of input enable, output enable, output value, function, drive strength from RTC_IO peripheral.
```c
esp_err_t rtc_gpio_hold_dis(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number (e.g. GPIO_NUM_12) 

!!! note "戻り値"
	esp_err_t



### rtc_gpio_isolate()
Helper function to disconnect internal circuits from an RTC IO This function disables input, output, pullup, pulldown, and enables hold feature for an RTC IO. Use this function if an RTC IO needs to be disconnected from internal circuits in deep sleep, to minimize leakage current.

In particular, for ESP32-WROVER module, call rtc_gpio_isolate(GPIO_NUM_12) before entering deep sleep, to reduce deep sleep current.
```c
esp_err_t rtc_gpio_isolate(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number (e.g. GPIO_NUM_12). 

!!! note "戻り値"
	esp_err_t



### rtc_gpio_force_hold_dis_all()
Disable force hold signal for all RTC IOs

Each RTC pad has a "force hold" input signal from the RTC controller. If this signal is set, pad latches current values of input enable, function, output enable, and other signals which come from the RTC mux. Force hold signal is enabled before going into deep sleep for pins which are used for EXT1 wakeup. 
```c
void rtc_gpio_force_hold_dis_all()
```

!!! note "戻り値"
	void



### rtc_gpio_set_drive_capability()
Set RTC GPIO pad drive capability


```c
esp_err_t rtc_gpio_set_drive_capability(gpio_num_t gpio_num, gpio_drive_cap_t strength)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number, only support output GPIOs 
	- gpio_drive_cap_t `strength` Drive capability of the pad

!!! note "戻り値"
	esp_err_t 




### rtc_gpio_get_drive_capability()
Get RTC GPIO pad drive capability


```c
esp_err_t rtc_gpio_get_drive_capability(gpio_num_t gpio_num, gpio_drive_cap_t *strength)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number, only support output GPIOs 
	- gpio_drive_cap_t* `strength` Pointer to accept drive capability of the pad

!!! note "戻り値"
	esp_err_t 




### rtc_gpio_wakeup_enable()
Enable wakeup from sleep mode using specific GPIO


```c
esp_err_t rtc_gpio_wakeup_enable(gpio_num_t gpio_num, gpio_int_type_t intr_type)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number 
	- gpio_int_type_t `intr_type` Wakeup on high level (GPIO_INTR_HIGH_LEVEL) or low level (GPIO_INTR_LOW_LEVEL) 

!!! note "戻り値"
	esp_err_t 




### rtc_gpio_wakeup_disable()
Disable wakeup from sleep mode using specific GPIO


```c
esp_err_t rtc_gpio_wakeup_disable(gpio_num_t gpio_num)
```

!!! summary "引数"
	- gpio_num_t `gpio_num` GPIO number 

!!! note "戻り値"
	esp_err_t 




