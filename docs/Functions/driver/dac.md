# dac

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/dac.h>
```

上記宣言で利用できます。

## メンバー



### dac_pad_get_io_num()
Get the gpio number of a specific DAC channel.


```c
esp_err_t dac_pad_get_io_num(dac_channel_t channel, gpio_num_t *gpio_num)
```

!!! summary "引数"
	- dac_channel_t `channel` Channel to get the gpio number
	- gpio_num_t* `gpio_num` output buffer to hold the gpio number

!!! note "戻り値"
	esp_err_t 




### dac_output_voltage()
Set DAC output voltage.

DAC output is 8-bit. Maximum (255) corresponds to VDD.
```c
esp_err_t dac_output_voltage(dac_channel_t channel, uint8_t dac_value)
```

!!! summary "引数"
	- dac_channel_t `channel` DAC channel 
	- uint8_t `dac_value` DAC output value

!!! note "戻り値"
	esp_err_t



### dac_output_enable()
DAC pad output enable


```c
esp_err_t dac_output_enable(dac_channel_t channel)
```

!!! summary "引数"
	- dac_channel_t `channel` DAC channel 

!!! note "戻り値"
	esp_err_t



### dac_output_disable()
DAC pad output disable


```c
esp_err_t dac_output_disable(dac_channel_t channel)
```

!!! summary "引数"
	- dac_channel_t `channel` DAC channel 

!!! note "戻り値"
	esp_err_t



### dac_i2s_enable()
Enable DAC output data from I2S


```c
esp_err_t dac_i2s_enable()
```

!!! note "戻り値"
	esp_err_t



### dac_i2s_disable()
Disable DAC output data from I2S


```c
esp_err_t dac_i2s_disable()
```

!!! note "戻り値"
	esp_err_t



