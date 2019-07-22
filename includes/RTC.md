###  Second

```c
uint8_t RTC::Second
```


###  Minute

```c
uint8_t RTC::Minute
```


###  Hour

```c
uint8_t RTC::Hour
```


###  Week

```c
uint8_t RTC::Week
```


###  Day

```c
uint8_t RTC::Day
```


###  Month

```c
uint8_t RTC::Month
```


###  Year

```c
uint8_t RTC::Year
```


###  DateString

```c
uint8_t RTC::DateString[9]
```


###  TimeString

```c
uint8_t RTC::TimeString[9]
```


###  asc

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



