# GPIO(その他汎用機能)

## 概要

その他の汎用IO系をここにまとめます。

| PIN            | IO26 | IO36 | IO0 | IO32 | IO33 |
|----------------|------|------|-----|------|------|
| digitalRead()  | ○    | ○    | ○   | ○    | ○    |
| analogRead()   | NG   | NG   | NG  | ○    | ○    |
| touchRead()    | NG   | NG   | NG  | 33   | 32   |
| dacWrite()     | ○    | NG   | NG  | NG   | NG   |
| digitalWrite() | ○    | NG   | ○   | ○    | ○    |
| ledcWrite()    | ○    | NG   | ○   | ○    | ○    |


## 機能

### digitalRead() デジタル入力 0(1.65V未満) or 1(1.65V以上)
```
#include <M5StickC.h>
 
int PIN = 32;
 
void setup() {
  M5.begin();
 
  pinMode( PIN, INPUT);
}
 
void loop() {
  Serial.printf("%04d\n", digitalRead(PIN) );
  delay(500);
}
```

PINの入力がHIGHかLOWかを出力します。

### analogRead() アナログ入力 0(0V)-4095(3.3V)
```
#include <M5StickC.h>
 
int PIN = 32;
 
void setup() {
  M5.begin();
 
  pinMode( PIN, INPUT);
}
 
void loop() {
  Serial.printf("%04d\n", analogRead(PIN) );
  delay(500);
}
```

PINの電圧を取得することができます。

### digitalWrite() デジタル出力 LOW(0V) or HIGH(3.3V)
```
#include <M5StickC.h>
 
int PIN = 32;
 
void setup() {
  M5.begin();
 
  pinMode(PIN, OUTPUT);
}
 
void loop() {
  digitalWrite(PIN, HIGH);
  delay(500);
  digitalWrite(PIN, LOW);
  delay(500);
}
```

PINをHIGHかLOWに設定します。

## 関数リファレンス

- [/Functions/esp32-hal-gpio](../../Functions/esp32-hal-gpio/)

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/peripherals/gpio.html)

## 関連ブログ

- [M5StickCのIOについて調べてみた](https://lang-ship.com/blog/?p=658)
