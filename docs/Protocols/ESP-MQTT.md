# ESP-MQTT

MQTTはTCP/IPを利用したメッセージ送信プロトコルです。

ブローカーと呼ばれるMQサーバーと通信を行い、軽量なデータを送受信することができます。

センサーデータをアップロードするだけであればHTTPアクセスでもよいのですが、MQTTの方が通信量が少なく済みます。

## 無料で使えるブローカーサービス

- [Beebotte](https://beebotte.com/)
- [Heroku+CloudMQTT](https://jp.heroku.com/)
- [CloudMQTT](https://www.cloudmqtt.com/)

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/protocols/mqtt.html)
