# Wi-Fi

M5StickCはWi-Fiを内蔵しているので、すぐに通信をすることが可能です。

## Wi-Fi

一般的なWi-Fi機能です。

M5StickC自体がアクセスポイントになり、スマホなどからの接続を受け付けることもできますし、Wi-Fiルーターなどのアクセスポイントに接続することもできます。

### 参考ページ

- [Protocols/ESP-MQTT](../../Protocols/ESP-MQTT)
- [Protocols/HTTPS Server](../../Protocols/HTTPS_Server)
- [Protocols/HTTP Client](../../Protocols/HTTP_Client)
- [Protocols/HTTP Server](../../Protocols/HTTP_Server)
- [Protocols/mDNS](../../Protocols/mDNS)
- [UseCase/RTCの現在日時をNTPサーバーからセット](../../UseCase/RTCSetNTP/)
- [UseCase/RTCの現在日時をWebブラウザからセット](../../UseCase/RTCSetWeb/)

## Smart Config

スマートフォンなどからWi-Fi設定をするためのプロトコルです。

あまり利用されていないので、積極的に利用はしないほうがよいと思います。

- [ESP32のWi-fi設定方法調査](https://lang-ship.com/blog/work/esp32-wi-fi-setting/)
- [ESP-Touch](https://www.espressif.com/en/products/software/esp-touch/overview)
- [(PDF)ESP-TOUCH User Guide](https://www.espressif.com/sites/default/files/documentation/esp-touch_user_guide_en.pdf)

## ESP-NOW

Espressif社のWi-Fiデバイス間で直接通信をするためのプロトコルです。

250バイトまでのデータを簡単に通信することができます。

アクセスポイントが必要ない通信ですので、非常にかんたんに利用することができます。
直接見通せる範囲で簡易的に通信をするのには適していますが、安定した通信をするのであればアクセスポイントに接続した通常のWi-Fi通信の方が安定しやすいと思います。

- [M5StickCでESP-NOW その1](https://lang-ship.com/blog/work/m5stickc-esp-now-1/)
- [M5StickC(ESP32)での無線通信方式の選び方](https://lang-ship.com/blog/work/m5stickc-esp32-radio/)
- [ESP-NOW](https://www.espressif.com/en/products/software/esp-now/overview)
- [(PDF)ESP-NOW User Guide](https://www.espressif.com/sites/default/files/documentation/esp-now_user_guide_en.pdf)

## ESP Mesh

ESPノード自体が相互接続してメッシュネットワークを作成します。

Wi-Fiルーターに接続していない場合や、野外などの広範囲でネットワークを構築する場合には便利な機能です。

ただし扱いは非常の難しいので、Wi-Fiルーターなどのアクセスポイントに接続したほうが汎用的な構成になると思います。

- [ESP Mesh](https://www.espressif.com/en/products/software/esp-mesh/overview)

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/network/esp_wifi.html)
