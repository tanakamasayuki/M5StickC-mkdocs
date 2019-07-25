# SPIFFS

内蔵フラッシュ上でのファイルシステム。

- [ESP-WROOM-32 ( ESP32 ) SPIFFS アップローダープラグインの使い方](https://www.mgo-tec.com/blog-entry-spiffs-uploader-plugin-arduino-esp32.html)

スケッチにdataフォルダを作成し、転送ツールであらかじめ転送しておくことで、プログラムの中からファイルとして利用することができます。

プログラムの中に埋め込む形式の場合、プログラムの更新時に毎回転送する必要がありますので、大きなファイルの場合にはSPIFFS上に置いたほうがよいでしょう。

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/storage/spiffs.html)
