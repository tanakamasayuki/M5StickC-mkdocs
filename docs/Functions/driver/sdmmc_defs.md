# sdmmc_defs

内部関数です。通常は使いません。

## 利用方法
```
#include <driver/sdmmc_defs.h>
```

上記宣言で利用できます。

## メンバー









































































































































































































































































































































































































































































































































































































### MMC_RSP_BITS()
Extract up to 32 sequential bits from an array of 32-bit words

start=0 len=4 -> result=0x00000007 start=0 len=12 -> result=0x00000567 start=28 len=8 -> result=0x000000f0 start=59 len=5 -> result=0x00000011
```c
static uint32_t MMC_RSP_BITS(uint32_t *src, int start, int len)
```

!!! summary "引数"
	- uint32_t * `src` array of words to extract bits from 
	- int `start` index of the first bit to extract 
	- int `len` number of bits to extract, 1 to 32 

!!! note "戻り値"
	uint32_t



