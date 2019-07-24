# アナログ出力(DAC)

アナログ出力が可能です。

## 利用例

- [Peripherals/DAC](../../Peripherals/DAC/)

## メンバー

### アナログ出力 dacWrite()
指定したピンから指定電圧を出力します。

```c
void dacWrite(uint8_t pin, uint8_t value)
```

!!! summary "引数"
	- uint8_t `pin` 指定するピン(M5StickCでは26のみ)
	- uint8_t `value` 出力値(0-255:3.3V)

