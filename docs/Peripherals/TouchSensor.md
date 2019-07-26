# タッチセンサー

## 概要

静電容量式のタッチセンサーを利用する機能です。

利用できるのは2つのPINのみですが、PINアサインが逆になっているので注意してください。IO32に接続しているセンサーの値を取得するには33を指定する必要があります。

| PIN            | IO26 | IO36 | IO0 | IO32 | IO33 |
|----------------|------|------|-----|------|------|
| touchRead()    | NG   | NG   | NG  | 33   | 32   |

## サンプルプログラム
```
#include <M5StickC.h>
 
int PIN = 32;
boolean touched = false;
int threshold = 16;
 
void gotTouch() {
  touched = true;
}
 
void setup() {
  M5.begin();
 
  pinMode( PIN, INPUT);
  touchAttachInterrupt(PIN, gotTouch, threshold);
}
 
void loop() {
  if (touched) {
    Serial.println("touch!");
    touched = false;
  }
  Serial.printf("%4d\n", touchRead(PIN) );
  delay(500);
}
```

touchRead()は触ると数値が小さくなるので、触らないときの数字と、触って下がったときの数字の中間か、やや低い値をthresholdに設定してください。

## 関数リファレンス

- [Functions/esp32-hal-touch](../../Functions/esp32-hal-touch/)

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/peripherals/touch_pad.html)

## 関連ブログ

- [M5StickCのIOについて調べてみた](https://lang-ship.com/blog/?p=658)
