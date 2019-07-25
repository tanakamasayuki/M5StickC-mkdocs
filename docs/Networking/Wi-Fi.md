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

- [ESP-Touch](https://www.espressif.com/en/products/software/esp-touch/overview)
- [(PDF)ESP-TOUCH User Guide](https://www.espressif.com/sites/default/files/documentation/esp-touch_user_guide_en.pdf)

## ESP-NOW

Espressif社のWi-Fiデバイス間で直接通信をするためのプロトコルです。

250バイトまでのデータを簡単に通信することができます。

特殊な場合を除いて、Wi-Fiルーターなどのアクセスポイントに接続したほうが汎用的な構成になると思います。

- [ESP-NOW](https://www.espressif.com/en/products/software/esp-now/overview)
- [(PDF)ESP-NOW User Guide](https://www.espressif.com/sites/default/files/documentation/esp-now_user_guide_en.pdf)

## ESP Mesh

ESPノード自体が相互接続してメッシュネットワークを作成します。

Wi-Fiルーターに接続していない場合や、野外などの広範囲でネットワークを構築する場合には便利な機能です。

ただし扱いは非常の難しいので、Wi-Fiルーターなどのアクセスポイントに接続したほうが汎用的な構成になると思います。

- [ESP Mesh](https://www.espressif.com/en/products/software/esp-mesh/overview)

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/network/esp_wifi.html)
