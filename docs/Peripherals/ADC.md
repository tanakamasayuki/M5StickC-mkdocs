# ADC

## 概要

M5StickCでADCに使えるのはIO0以外の4つです。
IO0はプルアップされているので、GNDに接続した時以外は4095になります。

| PIN            | IO26 | IO36 | IO0 | IO32 | IO33 |
|----------------|------|------|-----|------|------|
| analogRead()   | ○   | ○   | NG  | ○    | ○    |

## サンプルコード
```
#include <M5StickC.h>
 
int PIN = 32;
 
void setup() {
  M5.begin();
 
  pinMode(PIN, ANALOG);
}
 
void loop() {
  Serial.printf( "%04d\n", analogRead( PIN ) );
  delay( 500 );
}
```

戻り値は0(0V)-4095(3.3V)。

## 関数リファレンス

- [Functions/esp32-hal-adc](../../Functions/esp32-hal-adc/)

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/peripherals/adc.html)

## 関連ブログ

- [M5StickCのIOについて調べてみた](https://lang-ship.com/blog/?p=658)
