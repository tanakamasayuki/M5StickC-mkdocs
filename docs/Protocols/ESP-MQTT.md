# ESP-MQTT

MQTTはTCP/IPを利用したメッセージ送信プロトコルです。

ブローカーと呼ばれるMQサーバーと通信を行い、軽量なデータを送受信することができます。

センサーデータをアップロードするだけであればHTTPアクセスでもよいのですが、MQTTの方が通信量が少なく済みます。

## 無料で使えるブローカーサービス

- [shiftr.io](https://shiftr.io/)
- [Beebotte](https://beebotte.com/)
- [Heroku+CloudMQTT](https://jp.heroku.com/)
- [CloudMQTT](https://www.cloudmqtt.com/)

## 関連ブログ
- [M5StickCにENV HAT(気温、湿度、気圧)をサーバーにアップする その5(Beebotte+MQTT編)](https://lang-ship.com/blog/work/m5stickc-env-hat-5/)

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/protocols/mqtt.html)
