# リアルタイムクロック(RTC)

## 概要

内蔵されている時計機能の管理クラスです。

時間合わせをしない限り正しい時間がセットされていないので、利用する前にかならず時間をセットしてください。

## データシート
- RTC [BM8563](http://www.belling.com.cn/media/file_object/bel_product/BM8563/datasheet/BM8563_V1.1_cn.pdf)

## メンバー

### 秒 Second
関数で更新されます
```c
uint8_t RTC::Second
```


### 分 Minute
関数で更新されます
```c
uint8_t RTC::Minute
```


### 時間 Hour
関数で更新されます
```c
uint8_t RTC::Hour
```


### 曜日(0:日, 1:月, 2:火, 3:水, 4:木, 5:金, 6:土) Week
現状更新されないので利用できません
```c
uint8_t RTC::Week
```


### 日 Day
現状更新されないので利用できません
```c
uint8_t RTC::Day
```


### 月 Month
現状更新されないので利用できません
```c
uint8_t RTC::Month
```


### 年 Year
現状更新されないので利用できません
```c
uint8_t RTC::Year
```


### 年月日文字列 DateString
現状更新されないので利用できません
```c
uint8_t RTC::DateString[9]
```


### 時間文字列 TimeString
現状更新されないので利用できません
```c
uint8_t RTC::TimeString[9]
```


### 日時データ asc
関数で更新されます
```c
uint8_t RTC::asc[14]
```


### コンストラクタ RTC()
I2Cの初期化
```c
RTC::RTC()
```



### (非推奨)日時取得 GetBm8563Time()
現状非推奨です。0.0.7では時間しか更新されず、日付は取得できません。
```c
void RTC::GetBm8563Time(void)
```



### 時間を設定 SetTime()
とSetTime()はペアで呼び出します。
```c
void RTC::SetTime(RTC_TimeTypeDef *RTC_TimeStruct)
```

!!! summary "引数"
	- RTC_TimeTypeDef* `RTC_TimeStruct` 時間用構造体



### 日付を設定 SetData()
とSetTime()はペアで呼び出します。
```c
void RTC::SetData(RTC_DateTypeDef *RTC_DataStruct)
```

!!! summary "引数"
	- RTC_DateTypeDef* `RTC_DataStruct` 日付用構造体



### 時間を取得 GetTime()
とGetTime()はペアで呼び出します。
```c
void RTC::GetTime(RTC_TimeTypeDef *RTC_TimeStruct)
```

!!! summary "引数"
	- RTC_TimeTypeDef* `RTC_TimeStruct` 時間用構造体



### 日付を取得 GetData()
とGetTime()はペアで呼び出します。
```c
void RTC::GetData(RTC_DateTypeDef *RTC_DataStruct)
```

!!! summary "引数"
	- RTC_DateTypeDef* `RTC_DataStruct` 日付用構造体




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

