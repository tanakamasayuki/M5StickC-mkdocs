# SPI Slave

## 概要

SPI通信のSlave側の機能です。

クラスが準備されておらず、自分で低レベル関数を組み合わせて作る必要があります。Slaveの場合最後の4バイトが受信できないバグがあったりするので、個人的には使わない方が良いと思います。

## 参考サイト
- [ESP32 で SPI スレーブ通信するときの注意点](https://rabbit-note.com/2019/01/20/esp32-arduino-spi-slave/)

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/peripherals/spi_slave.html)
