# I2S(Inter-IC Sound)

## 概要

IC間でデジタル音声データを転送する通信です。

M5StickCでは2つまでのI2Sを利用することが可能ですが、内蔵マイクロフォンにて1つ利用しています。

## できること

- 外部DACに音声出力(デジタル)
- 内蔵DAC(IO26)に音声出力(アナログ)
- マイクからの入力(デジタル)

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/peripherals/i2s.html)

