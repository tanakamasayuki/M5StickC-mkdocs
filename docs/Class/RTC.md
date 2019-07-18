# リアルタイムクロック(RTC)

## 概要

内蔵されている時計機能の管理クラスです。

時間合わせをしない限り正しい時間がセットされていないので、利用する前にかならず時間をセットしてください。

## データシート
- RTC [BM8563](http://www.belling.com.cn/media/file_object/bel_product/BM8563/datasheet/BM8563_V1.1_cn.pdf)

## 関数リファレンス

### 日時取得 GetData(), GetTime()

日時を取得します。GetData()とGetTime()はペアで呼び出します。

!!! note "定義"
	void RTC::GetData	(	RTC_DateTypeDef * 	RTC_DateStruct	)

!!! note "定義"
	void RTC::GetTime	(	RTC_TimeTypeDef * 	RTC_TimeStruct	)

```
#include <M5StickC.h>

RTC_TimeTypeDef RTC_TimeStruct;
RTC_DateTypeDef RTC_DateStruct;
static const char *wd[7] = {"Sun", "Mon", "Tue", "Wed", "Thr", "Fri", "Sat"};

void setup() {
  M5.begin();
  M5.Lcd.setRotation(3);
}

void loop() {
  M5.Rtc.GetTime(&RTC_TimeStruct);
  M5.Rtc.GetData(&RTC_DateStruct);
  M5.Lcd.setCursor(0, 30);
  M5.Lcd.printf("Data: %04d/%02d/%02d\n", RTC_DateStruct.Year, RTC_DateStruct.Month, RTC_DateStruct.Date);
  M5.Lcd.printf("Week: %s\n", wd[RTC_DateStruct.WeekDay]);
  M5.Lcd.printf("Time: %02d : %02d : %02d\n", RTC_TimeStruct.Hours, RTC_TimeStruct.Minutes, RTC_TimeStruct.Seconds);
  delay(500);
}
```

### 日時設定 SetData(), SetTime()

日時を設定します。SetData()とSetTime()はペアで呼び出します。

!!! note "定義"
	void RTC::SetData	(	RTC_DateTypeDef * 	RTC_DateStruct	)

!!! note "定義"
	void RTC::SetTime	(	RTC_TimeTypeDef * 	RTC_TimeStruct	)

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

### (非推奨)日時取得 GetBm8563Time()

日時を取得して、公開変数を更新します。

現状非推奨です。0.0.7では時間しか更新されず、日付は取得できません。

!!! note "定義"
	void RTC::GetBm8563Time( void )

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

