# adc2_wifi_internal

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/adc2_wifi_internal.h>
```

上記宣言で利用できます。

## メンバー

### adc2_wifi_acquire()
For WIFI module to claim the usage of ADC2.



```c
esp_err_t adc2_wifi_acquire()
```

!!! note "戻り値"
	esp_err_t



### adc2_wifi_release()
For WIFI module to let other tasks use the ADC2 when WIFI is not work.



```c
esp_err_t adc2_wifi_release()
```

!!! note "戻り値"
	esp_err_t



