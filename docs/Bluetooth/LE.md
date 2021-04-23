# Bluetooth LE

Bluetooth LEを使って、通信をすることができます。

## Bluetooth LEの概要

### ServerとClinetの区分

Bluetoothキーボードとパソコンの関係でいうと、BluetoothキーボードがServerで、パソコン側がClinetになります。

キーボードなどのBluetoothデバイスに、各端末側が接続に行くイメージです。

M5StickCはServerにも、Clinetにもなることが可能です。

### プロファイル

Bluetooth LEは複数のプロファイルがありますが、ESP32だとサポートしているプロファイルしか取得することができません。

わかりやすいもので、iOSがサポートしているBluetoothのバッテリー残量などは取得ができません。

[ESP32 Frequently Asked Questions](https://www.espressif.com/sites/default/files/documentation/ESP32_FAQs__EN.pdf)

では、以下のプロファイルをサポートしていると記述がありました。

基本プロファイルのGATT/SMP/GAPは完全サポートで、その他にBLE HID (receiving side), BLE SPP-Like, Battery, DIS, Blu-Fi (Bluetooth Network Configurationtransmitting side)などが実装されているとかかれていますが、Arduino IDE上から使えるとは限りません。

## 関連ブログ
- [M5StickC(ESP32)にWindows10からBLE-MIDIでリアルタイム数値送信をしてみる](https://lang-ship.com/blog/work/m5stickc-esp32-ble-midi/)
- [M5StickCでBluetooth keyboardを実装してプレゼン用リモコンを作る](https://lang-ship.com/blog/work/m5stickc-bluetooth-keyboard/)
- [M5StickC(ESP32)でダイソーのBluetoothシャッターを操作(1.0.4対応版)](https://lang-ship.com/blog/work/m5stickc-esp32-bluetooth-shutter-1-0-4/)
- [ESP32 1.0.3のBLEUUIDについて](https://lang-ship.com/blog/?p=933)
- [M5StickC(ESP32)でダイソーのBluetoothシャッターを操作(1.0.3対応版)](https://lang-ship.com/blog/?p=929)
- [M5StickC(ESP32)でダイソーのBluetoothシャッターを操作](https://lang-ship.com/blog/?p=704)
- [M5StickCでBLEデバイスを検索する](https://lang-ship.com/blog/?p=691)

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/bluetooth/bt_le.html)
