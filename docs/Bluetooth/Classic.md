# Bluetooth Classic

Bluetooth Serial以外はより新しいBLEを利用したほうが多くの場合、好ましいです。

## 対応プロファイル

### BT GAP(Generic Access Profile)

すべてのプロファイルの基礎として動く、プロファイルでデバイスの接続、認証、暗号化などを行う。

### BT A2DP(Advanced Audio Distribution Profile)

ステレオのオーディオデータをストリーミング配信するためのプロファイル。

### BT AVRC(Audio/Video Remote Control Profile)

リモコンとしてデバイスを操作するプロファイル。

### BT SPP

仮想シリアルポートを作成するプロファイル。

### BT HFP Define

携帯電話の発着信や通話を行うプロファイル。

## Bluetooth Serialのサンプル [[Github](https://github.com/tanakamasayuki/M5StickC-examples/blob/master/BluetoothSerial/BluetoothSerial.ino)]
```
#include <M5StickC.h>
#include <BluetoothSerial.h>

BluetoothSerial SerialBT;
uint64_t chipid;
char chipname[256];

void setup() {
  chipid = ESP.getEfuseMac();
  sprintf( chipname, "M5StickC_%04X", (uint16_t)(chipid >> 32));
  M5.begin();
  M5.Lcd.setRotation(3);
  M5.Lcd.fillScreen(BLACK);
  M5.Lcd.printf("Bluetooth: %s\n", chipname);
  M5.Lcd.printf("Ver: %s %s\n", __DATE__, __TIME__);
  M5.Lcd.println();
  M5.Lcd.printf("Val:");

  SerialBT.begin(chipname);
}

void loop() {
  int val = analogRead(33);

  Serial.println(val);
  SerialBT.println(val);
  M5.Lcd.setCursor(8*4, 8*3);
  M5.Lcd.printf("%4d", val);
  delay(500);
}
```

BluetoothSerialを宣言してSerialBT.println()などで通常のシリアルと同じ様に利用することができます。
通信速度の設定が不要で、それなりに高速で欠落のすくない通信が可能ですので便利に使えます。

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/bluetooth/classic_bt.html)

## 利用例

- [リアルタイムデータロガー](../../UseCase/DataLogRealtime/)
