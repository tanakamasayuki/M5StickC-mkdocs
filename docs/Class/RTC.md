# リアルタイムクロック(RTC)

## 概要

内蔵されている時計機能の管理クラスです。

時間合わせをしない限り正しい時間がセットされていないので、利用する前にかならず時間をセットしてください。

## データシート
- RTC [BM8563](http://www.belling.com.cn/media/file_object/bel_product/BM8563/datasheet/BM8563_V1.1_cn.pdf)

## メンバー

{! Class/M5StickC/RTC.md !}

## サンプルスケッチ

### 日時設定
```
#include <M5StickC.h>

void setup() {
  M5.begin();

  RTC_DateTypeDef DateStruct;
  DateStruct.WeekDay = 3;
  DateStruct.Month = 3;
  DateStruct.Date = 22;
  DateStruct.Year = 2019;
  M5.Rtc.SetData(&DateStruct);

  RTC_TimeTypeDef TimeStruct;
  TimeStruct.Hours   = 18;
  TimeStruct.Minutes = 56;
  TimeStruct.Seconds = 10;
  M5.Rtc.SetTime(&TimeStruct);
}

void loop() {
}
```

### 日時取得
```
#include <M5StickC.h>

void setup() {
  M5.begin();
  M5.Lcd.setRotation(3);

  M5.Rtc.GetBm8563Time();
  M5.Lcd.printf("%04d/%02d/%02d %02d:%02d:%02d",
    M5.Rtc.Year,
    M5.Rtc.Month,
    M5.Rtc.Day,
    M5.Rtc.Hour,
    M5.Rtc.Minute,
    M5.Rtc.Second
  );  
}

void loop() {
}
```

## 利用例

- [RTCの現在日時をNTPサーバーからセット](../../UseCase/RTCSetNTP/)
- [RTCの現在日時をWebブラウザからセット](../../UseCase/RTCSetWeb/)

