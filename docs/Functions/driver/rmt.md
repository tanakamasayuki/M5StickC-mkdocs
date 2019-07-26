# rmt

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/rmt.h>
```

上記宣言で利用できます。


## メンバー

























### rmt_set_clk_div()
Set RMT clock divider, channel clock is divided from source clock.


```c
esp_err_t rmt_set_clk_div(rmt_channel_t channel, uint8_t div_cnt)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- uint8_t `div_cnt` RMT counter clock divider

!!! note "戻り値"
	esp_err_t 




### rmt_get_clk_div()
Get RMT clock divider, channel clock is divided from source clock.


```c
esp_err_t rmt_get_clk_div(rmt_channel_t channel, uint8_t *div_cnt)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- uint8_t * `div_cnt` pointer to accept RMT counter divider

!!! note "戻り値"
	esp_err_t 




### rmt_set_rx_idle_thresh()
Set RMT RX idle threshold value


```c
esp_err_t rmt_set_rx_idle_thresh(rmt_channel_t channel, uint16_t thresh)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- uint16_t `thresh` RMT RX idle threshold

!!! note "戻り値"
	esp_err_t



### rmt_get_rx_idle_thresh()
Get RMT idle threshold value.


```c
esp_err_t rmt_get_rx_idle_thresh(rmt_channel_t channel, uint16_t *thresh)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- uint16_t * `thresh` pointer to accept RMT RX idle threshold value

!!! note "戻り値"
	esp_err_t



### rmt_set_mem_block_num()
Set RMT memory block number for RMT channel


```c
esp_err_t rmt_set_mem_block_num(rmt_channel_t channel, uint8_t rmt_mem_num)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- uint8_t `rmt_mem_num` RMT RX memory block number, one block has 64 * 32 bits.

!!! note "戻り値"
	esp_err_t



### rmt_get_mem_block_num()
Get RMT memory block number


```c
esp_err_t rmt_get_mem_block_num(rmt_channel_t channel, uint8_t *rmt_mem_num)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- uint8_t * `rmt_mem_num` Pointer to accept RMT RX memory block number

!!! note "戻り値"
	esp_err_t 




### rmt_set_tx_carrier()
Configure RMT carrier for TX signal.


```c
esp_err_t rmt_set_tx_carrier(rmt_channel_t channel, bool carrier_en, uint16_t high_level, uint16_t low_level, rmt_carrier_level_t carrier_level)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- bool `carrier_en` Whether to enable output carrier. 
	- uint16_t `high_level` High level duration of carrier 
	- uint16_t `low_level` Low level duration of carrier. 
	- rmt_carrier_level_t `carrier_level` Configure the way carrier wave is modulated for channel 0-7.


!!! note "戻り値"
	esp_err_t



### rmt_set_mem_pd()
Set RMT memory in low power mode.


```c
esp_err_t rmt_set_mem_pd(rmt_channel_t channel, bool pd_en)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- bool `pd_en` RMT memory low power enable.

!!! note "戻り値"
	esp_err_t



### rmt_get_mem_pd()
Get RMT memory low power mode.


```c
esp_err_t rmt_get_mem_pd(rmt_channel_t channel, bool *pd_en)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- bool * `pd_en` Pointer to accept RMT memory low power mode.

!!! note "戻り値"
	esp_err_t 




### rmt_tx_start()
Set RMT start sending data from memory.


```c
esp_err_t rmt_tx_start(rmt_channel_t channel, bool tx_idx_rst)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- bool `tx_idx_rst` Set true to reset memory index for TX. Otherwise, transmitter will continue sending from the last index in memory.

!!! note "戻り値"
	esp_err_t 




### rmt_tx_stop()
Set RMT stop sending.


```c
esp_err_t rmt_tx_stop(rmt_channel_t channel)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7)

!!! note "戻り値"
	esp_err_t 




### rmt_rx_start()
Set RMT start receiving data.


```c
esp_err_t rmt_rx_start(rmt_channel_t channel, bool rx_idx_rst)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- bool `rx_idx_rst` Set true to reset memory index for receiver. Otherwise, receiver will continue receiving data to the last index in memory.

!!! note "戻り値"
	esp_err_t 




### rmt_rx_stop()
Set RMT stop receiving data.


```c
esp_err_t rmt_rx_stop(rmt_channel_t channel)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7)

!!! note "戻り値"
	esp_err_t 




### rmt_memory_rw_rst()
Reset RMT TX/RX memory index.


```c
esp_err_t rmt_memory_rw_rst(rmt_channel_t channel)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7)

!!! note "戻り値"
	esp_err_t 




### rmt_set_memory_owner()
Set RMT memory owner.


```c
esp_err_t rmt_set_memory_owner(rmt_channel_t channel, rmt_mem_owner_t owner)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- rmt_mem_owner_t `owner` To set when the transmitter or receiver can process the memory of channel.

!!! note "戻り値"
	esp_err_t 




### rmt_get_memory_owner()
Get RMT memory owner.


```c
esp_err_t rmt_get_memory_owner(rmt_channel_t channel, rmt_mem_owner_t *owner)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- rmt_mem_owner_t* `owner` Pointer to get memory owner.

!!! note "戻り値"
	esp_err_t 




### rmt_set_tx_loop_mode()
Set RMT tx loop mode.


```c
esp_err_t rmt_set_tx_loop_mode(rmt_channel_t channel, bool loop_en)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- bool `loop_en` Enable RMT transmitter loop sending mode. If set true, transmitter will continue sending from the first data to the last data in channel 0-7 over and over again in a loop.

!!! note "戻り値"
	esp_err_t 




### rmt_get_tx_loop_mode()
Get RMT tx loop mode.


```c
esp_err_t rmt_get_tx_loop_mode(rmt_channel_t channel, bool *loop_en)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- bool * `loop_en` Pointer to accept RMT transmitter loop sending mode.

!!! note "戻り値"
	esp_err_t 




### rmt_set_rx_filter()
Set RMT RX filter.


```c
esp_err_t rmt_set_rx_filter(rmt_channel_t channel, bool rx_filter_en, uint8_t thresh)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- bool `rx_filter_en` To enable RMT receiver filter. 
	- uint8_t `thresh` Threshold of pulse width for receiver.

!!! note "戻り値"
	esp_err_t



### rmt_set_source_clk()
Set RMT source clock


```c
esp_err_t rmt_set_source_clk(rmt_channel_t channel, rmt_source_clk_t base_clk)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- rmt_source_clk_t `base_clk` To choose source clock for RMT module.

!!! note "戻り値"
	esp_err_t



### rmt_get_source_clk()
Get RMT source clock


```c
esp_err_t rmt_get_source_clk(rmt_channel_t channel, rmt_source_clk_t *src_clk)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- rmt_source_clk_t* `src_clk` Pointer to accept source clock for RMT module.

!!! note "戻り値"
	esp_err_t



### rmt_set_idle_level()
Set RMT idle output level for transmitter


```c
esp_err_t rmt_set_idle_level(rmt_channel_t channel, bool idle_out_en, rmt_idle_level_t level)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- bool `idle_out_en` To enable idle level output. 
	- rmt_idle_level_t `level` To set the output signal's level for channel 0-7 in idle state.

!!! note "戻り値"
	esp_err_t 




### rmt_get_idle_level()
Get RMT idle output level for transmitter


```c
esp_err_t rmt_get_idle_level(rmt_channel_t channel, bool *idle_out_en, rmt_idle_level_t *level)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- bool * `idle_out_en` Pointer to accept value of enable idle. 
	- rmt_idle_level_t* `level` Pointer to accept value of output signal's level in idle state for specified channel.

!!! note "戻り値"
	esp_err_t 




### rmt_get_status()
Get RMT status


```c
esp_err_t rmt_get_status(rmt_channel_t channel, uint32_t *status)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0-7) 
	- uint32_t * `status` Pointer to accept channel status.

!!! note "戻り値"
	esp_err_t 




### rmt_set_intr_enable_mask()
Set mask value to RMT interrupt enable register.


```c
void rmt_set_intr_enable_mask(uint32_t mask)
```

!!! summary "引数"
	- uint32_t `mask` Bit mask to set to the register 

!!! note "戻り値"
	void



### rmt_clr_intr_enable_mask()
Clear mask value to RMT interrupt enable register.


```c
void rmt_clr_intr_enable_mask(uint32_t mask)
```

!!! summary "引数"
	- uint32_t `mask` Bit mask to clear the register 

!!! note "戻り値"
	void



### rmt_set_rx_intr_en()
Set RMT RX interrupt enable


```c
esp_err_t rmt_set_rx_intr_en(rmt_channel_t channel, bool en)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7) 
	- bool `en` enable or disable RX interrupt.

!!! note "戻り値"
	esp_err_t 




### rmt_set_err_intr_en()
Set RMT RX error interrupt enable


```c
esp_err_t rmt_set_err_intr_en(rmt_channel_t channel, bool en)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7) 
	- bool `en` enable or disable RX err interrupt.

!!! note "戻り値"
	esp_err_t 




### rmt_set_tx_intr_en()
Set RMT TX interrupt enable


```c
esp_err_t rmt_set_tx_intr_en(rmt_channel_t channel, bool en)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7) 
	- bool `en` enable or disable TX interrupt.

!!! note "戻り値"
	esp_err_t 




### rmt_set_tx_thr_intr_en()
Set RMT TX threshold event interrupt enable

An interrupt will be triggered when the number of transmitted items reaches the threshold value
```c
esp_err_t rmt_set_tx_thr_intr_en(rmt_channel_t channel, bool en, uint16_t evt_thresh)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7) 
	- bool `en` enable or disable TX event interrupt. 
	- uint16_t `evt_thresh` RMT event interrupt threshold value

!!! note "戻り値"
	esp_err_t



### rmt_set_pin()
Set RMT pin


```c
esp_err_t rmt_set_pin(rmt_channel_t channel, rmt_mode_t mode, gpio_num_t gpio_num)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7) 
	- rmt_mode_t `mode` TX or RX mode for RMT 
	- gpio_num_t `gpio_num` GPIO number to transmit or receive the signal.

!!! note "戻り値"
	esp_err_t 




### rmt_config()
Configure RMT parameters


```c
esp_err_t rmt_config(const rmt_config_t *rmt_param)
```

!!! summary "引数"
	- rmt_config_tconst  * `rmt_param` RMT parameter struct

!!! note "戻り値"
	esp_err_t 




### rmt_isr_register()
Register RMT interrupt handler, the handler is an ISR.


```c
esp_err_t rmt_isr_register(void(*fn)(void *), void *arg, int intr_alloc_flags, rmt_isr_handle_t *handle)
```

!!! summary "引数"
	- void(*)(void *) `fn` Interrupt handler function. 
	- void * `arg` Parameter for the handler function 
	- int `intr_alloc_flags` Flags used to allocate the interrupt. One or multiple (ORred) ESP_INTR_FLAG_* values. See esp_intr_alloc.h for more info. 
	- rmt_isr_handle_t* `handle` If non-zero, a handle to later clean up the ISR gets stored here.

!!! note "戻り値"
	esp_err_t



### rmt_isr_deregister()
Deregister previously registered RMT interrupt handler


```c
esp_err_t rmt_isr_deregister(rmt_isr_handle_t handle)
```

!!! summary "引数"
	- rmt_isr_handle_t `handle` Handle obtained from rmt_isr_register

!!! note "戻り値"
	esp_err_t 




### rmt_fill_tx_items()
Fill memory data of channel with given RMT items.


```c
esp_err_t rmt_fill_tx_items(rmt_channel_t channel, const rmt_item32_t *item, uint16_t item_num, uint16_t mem_offset)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7) 
	- const rmt_item32_t * `item` Pointer of items. 
	- uint16_t `item_num` RMT sending items number. 
	- uint16_t `mem_offset` Index offset of memory.

!!! note "戻り値"
	esp_err_t 




### rmt_driver_install()
Initialize RMT driver


```c
esp_err_t rmt_driver_install(rmt_channel_t channel, size_t rx_buf_size, int intr_alloc_flags)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7) 
	- size_t `rx_buf_size` Size of RMT RX ringbuffer. Can be 0 if the RX ringbuffer is not used. 
	- int `intr_alloc_flags` Flags for the RMT driver interrupt handler. Pass 0 for default flags. See esp_intr_alloc.h for details. If ESP_INTR_FLAG_IRAM is used, please do not use the memory allocated from psram when calling rmt_write_items.

!!! note "戻り値"
	esp_err_t 




### rmt_driver_uninstall()
Uninstall RMT driver.


```c
esp_err_t rmt_driver_uninstall(rmt_channel_t channel)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7)

!!! note "戻り値"
	esp_err_t 




### rmt_write_items()
RMT send waveform from rmt_item array.


```c
esp_err_t rmt_write_items(rmt_channel_t channel, const rmt_item32_t *rmt_item, int item_num, bool wait_tx_done)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7) 
	- const rmt_item32_t * `rmt_item` head point of RMT items array. If ESP_INTR_FLAG_IRAM is used, please do not use the memory allocated from psram when calling rmt_write_items. 
	- int `item_num` RMT data item number. 
	- bool `wait_tx_done` 


!!! note "戻り値"
	esp_err_t



### rmt_wait_tx_done()
Wait RMT TX finished.


```c
esp_err_t rmt_wait_tx_done(rmt_channel_t channel, TickType_t wait_time)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7) 
	- TickType_t `wait_time` Maximum time in ticks to wait for transmission to be complete. If set 0, return immediately with ESP_ERR_TIMEOUT if TX is busy (polling).

!!! note "戻り値"
	esp_err_t 




### rmt_get_ringbuf_handle()
Get ringbuffer from RMT.


```c
esp_err_t rmt_get_ringbuf_handle(rmt_channel_t channel, RingbufHandle_t *buf_handle)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7) 
	- RingbufHandle_t * `buf_handle` Pointer to buffer handle to accept RX ringbuffer handle.

!!! note "戻り値"
	esp_err_t



### rmt_translator_init()
Init rmt translator and register user callback. The callback will convert the raw data that needs to be sent to rmt format. If a channel is initialized more than once, tha user callback will be replaced by the later.


```c
esp_err_t rmt_translator_init(rmt_channel_t channel, sample_to_rmt_t fn)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7). 
	- sample_to_rmt_t `fn` Point to the data conversion function.

!!! note "戻り値"
	esp_err_t 




### rmt_write_sample()
Translate uint8_t type of data into rmt format and send it out. Requires rmt_translator_init to init the translator first.


```c
esp_err_t rmt_write_sample(rmt_channel_t channel, const uint8_t *src, size_t src_size, bool wait_tx_done)
```

!!! summary "引数"
	- rmt_channel_t `channel` RMT channel (0 - 7). 
	- const uint8_t * `src` Pointer to the raw data. 
	- size_t `src_size` The size of the raw data. 
	- bool `wait_tx_done` Set true to wait all data send done.

!!! note "戻り値"
	esp_err_t 




### rmt_register_tx_end_callback()
Registers a callback that will be called when transmission ends.


```c
rmt_tx_end_callback_t rmt_register_tx_end_callback(rmt_tx_end_fn_t function, void *arg)
```

!!! summary "引数"
	- rmt_tx_end_fn_t `function` Function to be called from the default interrupt handler or NULL. 
	- void * `arg` Argument which will be provided to the callback when it is called.

!!! note "戻り値"
	rmt_tx_end_callback_t



