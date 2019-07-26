# sigmadelta

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/sigmadelta.h>
```

上記宣言で利用できます。

## メンバー



### sigmadelta_config()
Configure Sigma-delta channel


```c
esp_err_t sigmadelta_config(const sigmadelta_config_t *config)
```

!!! summary "引数"
	- sigmadelta_config_tconst  * `config` Pointer of Sigma-delta channel configuration struct

!!! note "戻り値"
	esp_err_t 




### sigmadelta_set_duty()
Set Sigma-delta channel duty.


```c
esp_err_t sigmadelta_set_duty(sigmadelta_channel_t channel, int8_t duty)
```

!!! summary "引数"
	- sigmadelta_channel_t `channel` Sigma-delta channel number 
	- int8_t `duty` Sigma-delta duty of one channel, the value ranges from -128 to 127, recommended range is -90 ~ 90. The waveform is more like a random one in this range.

!!! note "戻り値"
	esp_err_t



### sigmadelta_set_prescale()
Set Sigma-delta channel's clock pre-scale value. The source clock is APP_CLK, 80MHz. The clock frequency of the sigma-delta channel is APP_CLK / pre_scale


```c
esp_err_t sigmadelta_set_prescale(sigmadelta_channel_t channel, uint8_t prescale)
```

!!! summary "引数"
	- sigmadelta_channel_t `channel` Sigma-delta channel number 
	- uint8_t `prescale` The divider of source clock, ranges from 0 to 255

!!! note "戻り値"
	esp_err_t 




### sigmadelta_set_pin()
Set Sigma-delta signal output pin


```c
esp_err_t sigmadelta_set_pin(sigmadelta_channel_t channel, gpio_num_t gpio_num)
```

!!! summary "引数"
	- sigmadelta_channel_t `channel` Sigma-delta channel number 
	- gpio_num_t `gpio_num` GPIO number of output pin.

!!! note "戻り値"
	esp_err_t 




