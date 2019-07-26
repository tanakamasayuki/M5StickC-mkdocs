# uart_select

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/uart_select.h>
```

上記宣言で利用できます。

## メンバー

### uart_set_select_notif_callback()
Set notification callback function for select() events

```c
void uart_set_select_notif_callback(uart_port_t uart_num, uart_select_notif_callback_t uart_select_notif_callback)
```

!!! summary "引数"
	- uart_port_t `uart_num` UART port number 
	- uart_select_notif_callback_t `uart_select_notif_callback` callback function 

### uart_get_selectlock()
Get mutex guarding select() notifications

```c
portMUX_TYPE* uart_get_selectlock()
```

!!! note "戻り値"
	portMUX_TYPE *
