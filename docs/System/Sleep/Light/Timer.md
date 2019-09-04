# Timer

指定時間後に復帰します。

## サンプルスケッチ[[GitHub](https://github.com/tanakamasayuki/M5StickC-examples/blob/master/Sleep/LightSleepTimerWakeUp/LightSleepTimerWakeUp.ino)]

```c
int bootCount = 0; // ライトスリープは通常の変数で良い

void setup() {
  // シリアル初期化
  Serial.begin(115200);

  // シリアル初期化待ち
  delay(1000);

  // 1000000us = 1sのタイマー設定
  esp_sleep_enable_timer_wakeup(1000000);
}

void loop() {
  // 起動回数カウントアップ
  bootCount++;
  Serial.printf("起動回数: %d ", bootCount);

  // 起動方法取得
  esp_sleep_wakeup_cause_t wakeup_reason;
  wakeup_reason = esp_sleep_get_wakeup_cause();
  switch(wakeup_reason){
    case ESP_SLEEP_WAKEUP_EXT0      : Serial.printf("外部割り込み(RTC_IO)で起動\n"); break;
    case ESP_SLEEP_WAKEUP_EXT1      : Serial.printf("外部割り込み(RTC_CNTL)で起動 IO=%llX\n", esp_sleep_get_ext1_wakeup_status()); break;
    case ESP_SLEEP_WAKEUP_TIMER     : Serial.printf("タイマー割り込みで起動\n"); break;
    case ESP_SLEEP_WAKEUP_TOUCHPAD  : Serial.printf("タッチ割り込みで起動 PAD=%d\n", esp_sleep_get_touchpad_wakeup_status()); break;
    case ESP_SLEEP_WAKEUP_ULP       : Serial.printf("ULPプログラムで起動\n"); break;
    case ESP_SLEEP_WAKEUP_GPIO      : Serial.printf("ライトスリープからGPIO割り込みで起動\n"); break;
    case ESP_SLEEP_WAKEUP_UART      : Serial.printf("ライトスリープからUART割り込みで起動\n"); break;
    default                         : Serial.printf("スリープ以外からの起動\n"); break;
  }

  // シリアルをすべて出力する
  Serial.flush();

  // ライトスリープ
  esp_light_sleep_start();
}
```