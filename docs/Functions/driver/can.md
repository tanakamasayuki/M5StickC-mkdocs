# can

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/can.h>
```

上記宣言で利用できます。

## メンバー





### can_driver_install()
Install CAN driver

This function installs the CAN driver using three configuration structures. The required memory is allocated and the CAN driver is placed in the stopped state after running this function.
```c
esp_err_t can_driver_install(const can_general_config_t *g_config, const can_timing_config_t *t_config, const can_filter_config_t *f_config)
```

!!! summary "引数"
	- can_general_config_tconst  * `g_config` General configuration structure 
	- can_timing_config_tconst  * `t_config` Timing configuration structure 
	- can_filter_config_tconst  * `f_config` Filter configuration structure

!!! note "戻り値"
	esp_err_t



### can_driver_uninstall()
Uninstall the CAN driver




```c
esp_err_t can_driver_uninstall()
```

!!! note "戻り値"
	esp_err_t



### can_start()
Start the CAN driver



```c
esp_err_t can_start()
```

!!! note "戻り値"
	esp_err_t



### can_stop()
Stop the CAN driver




```c
esp_err_t can_stop()
```

!!! note "戻り値"
	esp_err_t



### can_transmit()
Transmit a CAN message

This function queues a CAN message for transmission. Transmission will start immediately if no other messages are queued for transmission. If the TX queue is full, this function will block until more space becomes available or until it timesout. If the TX queue is disabled (TX queue length = 0 in configuration), this function will return immediately if another message is undergoing transmission. This function can only be called when the CAN driver is in the running state and cannot be called under Listen Only Mode.
```c
esp_err_t can_transmit(const can_message_t *message, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- can_message_tconst  * `message` Message to transmit 
	- TickType_t `ticks_to_wait` Number of FreeRTOS ticks to block on the TX queue

!!! note "戻り値"
	esp_err_t



### can_receive()
Receive a CAN message

This function receives a message from the RX queue. The flags field of the message structure will indicate the type of message received. This function will block if there are no messages in the RX queue
```c
esp_err_t can_receive(can_message_t *message, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- can_message_t* `message` Received message 
	- TickType_t `ticks_to_wait` Number of FreeRTOS ticks to block on RX queue

!!! note "戻り値"
	esp_err_t



### can_read_alerts()
Read CAN driver alerts

This function will read the alerts raised by the CAN driver. If no alert has been when this function is called, this function will block until an alert occurs or until it timeouts.
```c
esp_err_t can_read_alerts(uint32_t *alerts, TickType_t ticks_to_wait)
```

!!! summary "引数"
	- uint32_t * `alerts` Bit field of raised alerts (see documentation for alert flags) 
	- TickType_t `ticks_to_wait` Number of FreeRTOS ticks to block for alert

!!! note "戻り値"
	esp_err_t



### can_reconfigure_alerts()
Reconfigure which alerts are enabled

This function reconfigures which alerts are enabled. If there are alerts which have not been read whilst reconfiguring, this function can read those alerts.
```c
esp_err_t can_reconfigure_alerts(uint32_t alerts_enabled, uint32_t *current_alerts)
```

!!! summary "引数"
	- uint32_t `alerts_enabled` Bit field of alerts to enable (see documentation for alert flags) 
	- uint32_t * `current_alerts` Bit field of currently raised alerts. Set to NULL if unused

!!! note "戻り値"
	esp_err_t



### can_initiate_recovery()
Start the bus recovery process




```c
esp_err_t can_initiate_recovery()
```

!!! note "戻り値"
	esp_err_t



### can_get_status_info()
Get current status information of the CAN driver


```c
esp_err_t can_get_status_info(can_status_info_t *status_info)
```

!!! summary "引数"
	- can_status_info_t* `status_info` Status information

!!! note "戻り値"
	esp_err_t 




