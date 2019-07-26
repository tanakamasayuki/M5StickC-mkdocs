# adc

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/adc.h>
```

上記宣言で利用できます。

## メンバー

































### adc1_pad_get_io_num()
Get the gpio number of a specific ADC1 channel.


```c
esp_err_t adc1_pad_get_io_num(adc1_channel_t channel, gpio_num_t *gpio_num)
```

!!! summary "引数"
	- adc1_channel_t `channel` Channel to get the gpio number
	- gpio_num_t* `gpio_num` output buffer to hold the gpio number

!!! note "戻り値"
	esp_err_t 




### adc1_config_width()
Configure ADC1 capture width, meanwhile enable output invert for ADC1. The configuration is for all channels of ADC1


```c
esp_err_t adc1_config_width(adc_bits_width_t width_bit)
```

!!! summary "引数"
	- adc_bits_width_t `width_bit` Bit capture width for ADC1

!!! note "戻り値"
	esp_err_t 




### adc_set_data_width()
Configure ADC capture width.


```c
esp_err_t adc_set_data_width(adc_unit_t adc_unit, adc_bits_width_t width_bit)
```

!!! summary "引数"
	- adc_unit_t `adc_unit` ADC unit index 
	- adc_bits_width_t `width_bit` Bit capture width for ADC unit. 

!!! note "戻り値"
	esp_err_t 




### adc1_config_channel_atten()
Set the attenuation of a particular channel on ADC1, and configure its associated GPIO pin mux.

For maximum accuracy, use the ADC calibration APIs and measure voltages within these recommended ranges.
```c
esp_err_t adc1_config_channel_atten(adc1_channel_t channel, adc_atten_t atten)
```

!!! summary "引数"
	- adc1_channel_t `channel` ADC1 channel to configure 
	- adc_atten_t `atten` Attenuation level

!!! note "戻り値"
	esp_err_t



### adc1_get_raw()
Take an ADC1 reading from a single channel.


```c
int adc1_get_raw(adc1_channel_t channel)
```

!!! summary "引数"
	- adc1_channel_t `channel` ADC1 channel to read

!!! note "戻り値"
	int



### adc_power_on()
Enable ADC power


```c
void adc_power_on()
```

!!! note "戻り値"
	void



### adc_power_off()
Power off SAR ADC This function will force power down for ADC


```c
void adc_power_off()
```

!!! note "戻り値"
	void



### adc_gpio_init()
Initialize ADC pad


```c
esp_err_t adc_gpio_init(adc_unit_t adc_unit, adc_channel_t channel)
```

!!! summary "引数"
	- adc_unit_t `adc_unit` ADC unit index 
	- adc_channel_t `channel` ADC channel index 

!!! note "戻り値"
	esp_err_t 




### adc_set_data_inv()
Set ADC data invert


```c
esp_err_t adc_set_data_inv(adc_unit_t adc_unit, bool inv_en)
```

!!! summary "引数"
	- adc_unit_t `adc_unit` ADC unit index 
	- bool `inv_en` whether enable data invert 

!!! note "戻り値"
	esp_err_t 




### adc_set_clk_div()
Set ADC source clock


```c
esp_err_t adc_set_clk_div(uint8_t clk_div)
```

!!! summary "引数"
	- uint8_t `clk_div` ADC clock divider, ADC clock is divided from APB clock 

!!! note "戻り値"
	esp_err_t 




### adc_set_i2s_data_source()
Set I2S data source


```c
esp_err_t adc_set_i2s_data_source(adc_i2s_source_t src)
```

!!! summary "引数"
	- adc_i2s_source_t `src` I2S DMA data source, I2S DMA can get data from digital signals or from ADC. 

!!! note "戻り値"
	esp_err_t 




### adc_i2s_mode_init()
Initialize I2S ADC mode


```c
esp_err_t adc_i2s_mode_init(adc_unit_t adc_unit, adc_channel_t channel)
```

!!! summary "引数"
	- adc_unit_t `adc_unit` ADC unit index 
	- adc_channel_t `channel` ADC channel index 

!!! note "戻り値"
	esp_err_t 




### adc1_ulp_enable()
Configure ADC1 to be usable by the ULP

Note that adc1_config_channel_atten, adc1_config_width functions need to be called to configure ADC1 channels, before ADC1 is used by the ULP. 
```c
void adc1_ulp_enable()
```

!!! note "戻り値"
	void



### hall_sensor_read()
Read Hall Sensor






```c
int hall_sensor_read()
```

!!! note "戻り値"
	int



### adc2_pad_get_io_num()
Get the gpio number of a specific ADC2 channel.


```c
esp_err_t adc2_pad_get_io_num(adc2_channel_t channel, gpio_num_t *gpio_num)
```

!!! summary "引数"
	- adc2_channel_t `channel` Channel to get the gpio number
	- gpio_num_t* `gpio_num` output buffer to hold the gpio number

!!! note "戻り値"
	esp_err_t 




### adc2_config_channel_atten()
Configure the ADC2 channel, including setting attenuation.



```c
esp_err_t adc2_config_channel_atten(adc2_channel_t channel, adc_atten_t atten)
```

!!! summary "引数"
	- adc2_channel_t `channel` ADC2 channel to configure 
	- adc_atten_t `atten` Attenuation level

!!! note "戻り値"
	esp_err_t



### adc2_get_raw()
Take an ADC2 reading on a single channel


```c
esp_err_t adc2_get_raw(adc2_channel_t channel, adc_bits_width_t width_bit, int *raw_out)
```

!!! summary "引数"
	- adc2_channel_t `channel` ADC2 channel to read
	- adc_bits_width_t `width_bit` Bit capture width for ADC2
	- int * `raw_out` the variable to hold the output data.

!!! note "戻り値"
	esp_err_t



### adc2_vref_to_gpio()
Output ADC2 reference voltage to gpio 25 or 26 or 27

This function utilizes the testing mux exclusive to ADC 2 to route the reference voltage one of ADC2's channels. Supported gpios are gpios 25, 26, and 27. This refernce voltage can be manually read from the pin and used in the esp_adc_cal component.
```c
esp_err_t adc2_vref_to_gpio(gpio_num_t gpio)
```

!!! summary "引数"
	- gpio_num_t `gpio` GPIO number (gpios 25,26,27 supported)

!!! note "戻り値"
	esp_err_t



