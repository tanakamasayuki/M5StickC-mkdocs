# SPI Master

## 概要

SPI通信のMaster側の機能です。SPIは3線＋αの信号線を利用した比較的高速の通信方式。概ねM単位での転送速度です。

M5StickCは上側に外部接続用のピンソケットと、下側にGrove端子がついています。
入力専用のIO36を除き、外部接続可能な4PINはどんな組み合わせでもSPIで通信が可能です。
ただし、上下両方に接続する必要があるので、非常に接続が面倒です。

## 端子名

| Arduino | Master側 | Slave側 | 別名      | 用途                                             |
|---------|----------|---------|-----------|--------------------------------------------------|
| SCK     | SCK      | SCK     | SCLK, SCL | データ送信のクロックをマスターが送信する         |
| MISO    | SDI      | SDO     | DC, D/C   | マスターの受信、スレーブの送信をする             |
| MOSI    | SDO      | SDI     | SDA       | マスターの送信、スレーブの受信をする             |
| SS      | SS       | CS      |           | 特定スレーブのCSを0Vにすることで通信先を選択する |

基本は3線で通信を行い、複数の通信先(スレーブ)がいる場合には、マスター側が複数のSS用PINを操作して、通信先のCSを0Vにすることで通信先を選択します。

相手先が1つだけの場合には、配線の段階でCSをGNDに接続することで常に選択されている状態となります。

名称は接続先のデバイスによって命名が様々なのと、SPI以外の通信線も接続する必要があるデバイスもあるので注意してください。

## SPIサポート

M5StickCでは最大4系統のSPI通信をサポートしています。

- SPI0 : 内部Flashへの接続に利用済み
- SPI1 : 内部Flashへの接続に利用済み
- HSPI : 未使用
- VSPI : 内蔵画面への接続に利用済み

M5StickCで追加で利用できるSPIは1系統のみになります。ただし、そもそも4線しか使えるピンが無いので外部に2系統使うことはできません。

複数のSPIデバイスを接続したい場合にはSCKとMISO、MOSIは平行にそのまま接続可能ですが、SSの選択を工夫する必要があります。2デバイスであればNOTなどで反転した信号を2デバイス目のCSに接続することで制御可能かもしれません。

3デバイス以上の場合には1-Wireの[DS2408](https://www.maximintegrated.com/jp/products/ibutton/memory-products/DS2408.html)などを使えば制御可能かもしれませんが、おすすめしません。

## 接続例
- [ST7735S+ISP液晶](../../Device/SPI/Display/ST7735S/)

## クラスリファレンス
- [Class/ESP32/SPIClass](../../Class/ESP32/SPIClass/)

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/peripherals/spi_master.html)

## 関連ブログ
- [M5StickCでSPI通信をする](https://lang-ship.com/blog/?p=683)
