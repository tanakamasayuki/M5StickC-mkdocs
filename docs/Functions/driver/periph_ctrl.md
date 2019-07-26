# periph_ctrl

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/periph_ctrl.h>
```

上記宣言で利用できます。

## メンバー

### periph_module_enable()
enable peripheral module



```c
void periph_module_enable(periph_module_t periph)
```

!!! summary "引数"
	- periph_module_t `periph` : Peripheral module name

!!! note "戻り値"
	void



### periph_module_disable()
disable peripheral module



```c
void periph_module_disable(periph_module_t periph)
```

!!! summary "引数"
	- periph_module_t `periph` : Peripheral module name

!!! note "戻り値"
	void



### periph_module_reset()
reset peripheral module



```c
void periph_module_reset(periph_module_t periph)
```

!!! summary "引数"
	- periph_module_t `periph` : Peripheral module name

!!! note "戻り値"
	void



