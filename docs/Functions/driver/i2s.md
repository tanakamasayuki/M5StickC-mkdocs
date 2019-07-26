# i2s

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/i2s.h>
```

上記宣言で利用できます。

## メンバー

























### i2s_set_pin()
Set I2S pin number




```c
esp_err_t i2s_set_pin(i2s_port_t i2s_num, const i2s_pin_config_t *pin)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0 or I2S_NUM_1
	- i2s_pin_config_tconst  * `pin` I2S Pin structure, or NULL to set 2-channel 8-bit internal DAC pin configuration (GPIO25 & GPIO26)

!!! note "戻り値"
	esp_err_t



### i2s_set_dac_mode()
Set I2S dac mode, I2S built-in DAC is disabled by default


```c
esp_err_t i2s_set_dac_mode(i2s_dac_mode_t dac_mode)
```

!!! summary "引数"
	- i2s_dac_mode_t `dac_mode` DAC mode configurations - see i2s_dac_mode_t

!!! note "戻り値"
	esp_err_t



### i2s_driver_install()
Install and start I2S driver.



```c
esp_err_t i2s_driver_install(i2s_port_t i2s_num, const i2s_config_t *i2s_config, int queue_size, void *i2s_queue)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0, I2S_NUM_1
	- i2s_config_tconst  * `i2s_config` I2S configurations - see  struct
	- int `queue_size` I2S event queue size/depth.
	- void * `i2s_queue` I2S event queue handle, if set NULL, driver will not use an event queue.

!!! note "戻り値"
	esp_err_t



### i2s_driver_uninstall()
Uninstall I2S driver.


```c
esp_err_t i2s_driver_uninstall(i2s_port_t i2s_num)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0, I2S_NUM_1

!!! note "戻り値"
	esp_err_t 




### i2s_write_bytes()
Write data to I2S DMA transmit buffer.



```c
int i2s_write_bytes(i2s_port_t i2s_num, const void *src, size_t size, TickType_t ticks_to_wait) __attribute__((deprecated))
```

!!! summary "引数"
	- i2s_port_t `i2s_num` 
	- const void * `src` 
	- size_t `size` 
	- TickType_t `ticks_to_wait` 

!!! note "戻り値"
	int



### i2s_write()
Write data to I2S DMA transmit buffer.


```c
esp_err_t i2s_write(i2s_port_t i2s_num, const void *src, size_t size, size_t *bytes_written, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0, I2S_NUM_1
	- const void * `src` Source address to write from
	- size_t `size` Size of data in bytes
	- size_t * `bytes_written` Number of bytes written, if timeout, the result will be less than the size passed in.
	- TickType_t `ticks_to_wait` TX buffer wait timeout in RTOS ticks. If this many ticks pass without space becoming available in the DMA transmit buffer, then the function will return (note that if the data is written to the DMA buffer in pieces, the overall operation may still take longer than this timeout.) Pass portMAX_DELAY for no timeout.

!!! note "戻り値"
	esp_err_t 




### i2s_write_expand()
Write data to I2S DMA transmit buffer while expanding the number of bits per sample. For example, expanding 16-bit PCM to 32-bit PCM.



```c
esp_err_t i2s_write_expand(i2s_port_t i2s_num, const void *src, size_t size, size_t src_bits, size_t aim_bits, size_t *bytes_written, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0, I2S_NUM_1
	- const void * `src` Source address to write from
	- size_t `size` Size of data in bytes
	- size_t `src_bits` Source audio bit
	- size_t `aim_bits` Bit wanted, no more than 32, and must be greater than src_bits
	- size_t * `bytes_written` Number of bytes written, if timeout, the result will be less than the size passed in.
	- TickType_t `ticks_to_wait` TX buffer wait timeout in RTOS ticks. If this many ticks pass without space becoming available in the DMA transmit buffer, then the function will return (note that if the data is written to the DMA buffer in pieces, the overall operation may still take longer than this timeout.) Pass portMAX_DELAY for no timeout.

!!! note "戻り値"
	esp_err_t



### i2s_read_bytes()
Read data from I2S DMA receive buffer



```c
int i2s_read_bytes(i2s_port_t i2s_num, void *dest, size_t size, TickType_t ticks_to_wait) __attribute__((deprecated))
```

!!! summary "引数"
	- i2s_port_t `i2s_num` 
	- void * `dest` 
	- size_t `size` 
	- TickType_t `ticks_to_wait` 

!!! note "戻り値"
	int



### i2s_read()
Read data from I2S DMA receive buffer


```c
esp_err_t i2s_read(i2s_port_t i2s_num, void *dest, size_t size, size_t *bytes_read, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0, I2S_NUM_1
	- void * `dest` Destination address to read into
	- size_t `size` Size of data in bytes
	- size_t * `bytes_read` Number of bytes read, if timeout, bytes read will be less than the size passed in.
	- TickType_t `ticks_to_wait` RX buffer wait timeout in RTOS ticks. If this many ticks pass without bytes becoming available in the DMA receive buffer, then the function will return (note that if data is read from the DMA buffer in pieces, the overall operation may still take longer than this timeout.) Pass portMAX_DELAY for no timeout.

!!! note "戻り値"
	esp_err_t



### i2s_push_sample()
Write a single sample to the I2S DMA TX buffer.

This function is deprecated. Use 'i2s_write' instead. This definition will be removed in a future release.
```c
int i2s_push_sample(i2s_port_t i2s_num, const void *sample, TickType_t ticks_to_wait) __attribute__((deprecated))
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0, I2S_NUM_1
	- const void * `sample` Buffer to read data. Size of buffer (in bytes) = bits_per_sample / 8.
	- TickType_t `ticks_to_wait` Timeout in RTOS ticks. If a sample is not available in the DMA buffer within this period, no data is read and function returns zero.

!!! note "戻り値"
	int



### i2s_pop_sample()
Read a single sample from the I2S DMA RX buffer.

This function is deprecated. Use 'i2s_read' instead. This definition will be removed in a future release.
```c
int i2s_pop_sample(i2s_port_t i2s_num, void *sample, TickType_t ticks_to_wait) __attribute__((deprecated))
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0, I2S_NUM_1
	- void * `sample` Buffer to write data. Size of buffer (in bytes) = bits_per_sample / 8.
	- TickType_t `ticks_to_wait` Timeout in RTOS ticks. If a sample is not available in the DMA buffer within this period, no data is read and function returns zero.

!!! note "戻り値"
	int



### i2s_set_sample_rates()
Set sample rate used for I2S RX and TX.


```c
esp_err_t i2s_set_sample_rates(i2s_port_t i2s_num, uint32_t rate)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0, I2S_NUM_1
	- uint32_t `rate` I2S sample rate (ex: 8000, 44100...)

!!! note "戻り値"
	esp_err_t



### i2s_stop()
Stop I2S driver

Disables I2S TX/RX, until  is called.
```c
esp_err_t i2s_stop(i2s_port_t i2s_num)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0, I2S_NUM_1

!!! note "戻り値"
	esp_err_t



### i2s_start()
Start I2S driver

It is not necessary to call this function after  (it is started automatically), however it is necessary to call it after .
```c
esp_err_t i2s_start(i2s_port_t i2s_num)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0, I2S_NUM_1

!!! note "戻り値"
	esp_err_t



### i2s_zero_dma_buffer()
Zero the contents of the TX DMA buffer.

Pushes zero-byte samples into the TX DMA buffer, until it is full.
```c
esp_err_t i2s_zero_dma_buffer(i2s_port_t i2s_num)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0, I2S_NUM_1

!!! note "戻り値"
	esp_err_t



### i2s_set_clk()
Set clock & bit width used for I2S RX and TX.

Similar to , but also sets bit width.
```c
esp_err_t i2s_set_clk(i2s_port_t i2s_num, uint32_t rate, i2s_bits_per_sample_t bits, i2s_channel_t ch)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` I2S_NUM_0, I2S_NUM_1
	- uint32_t `rate` I2S sample rate (ex: 8000, 44100...)
	- i2s_bits_per_sample_t `bits` I2S bit width (I2S_BITS_PER_SAMPLE_16BIT, I2S_BITS_PER_SAMPLE_24BIT, I2S_BITS_PER_SAMPLE_32BIT)
	- i2s_channel_t `ch` I2S channel, (I2S_CHANNEL_MONO, I2S_CHANNEL_STEREO)

!!! note "戻り値"
	esp_err_t



### i2s_set_adc_mode()
Set built-in ADC mode for I2S DMA, this function will initialize ADC pad, and set ADC parameters.


```c
esp_err_t i2s_set_adc_mode(adc_unit_t adc_unit, adc1_channel_t adc_channel)
```

!!! summary "引数"
	- adc_unit_t `adc_unit` SAR ADC unit index 
	- adc1_channel_t `adc_channel` ADC channel index 

!!! note "戻り値"
	esp_err_t 




### i2s_adc_enable()
Start to use I2S built-in ADC mode


```c
esp_err_t i2s_adc_enable(i2s_port_t i2s_num)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` i2s port index 

!!! note "戻り値"
	esp_err_t



### i2s_adc_disable()
Stop to use I2S built-in ADC mode


```c
esp_err_t i2s_adc_disable(i2s_port_t i2s_num)
```

!!! summary "引数"
	- i2s_port_t `i2s_num` i2s port index 

!!! note "戻り値"
	esp_err_t



