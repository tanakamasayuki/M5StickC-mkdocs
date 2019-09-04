# 外部接続端子

## 概要

外部接続可能な端子について、状況別の確認をしてみました。
電源オフでは3V3出力な無く、電源オン時にはAXP192の初期化の有無では変化はありません。

スリープした場合、一般的なESP32と同じくモードによってHIGH出力がオープンになりますが、それ以外には影響はありません。
AXP192のスリープは影響は消えますが、I2C接続されているAXP192やRTCにはアクセス可能なままです。

| 条件                        | GPIO0 | GPIO26 | GPIO36 | GPIO32 | GPIO33 | BAT | 3V3 | 5V | Grove5V |
|-----------------------------|-------|--------|--------|--------|--------|-----|-----|----|---------|
| 電源オフ                    | -     | -      | -      | -      | -      | ON  | <font color="Red">OFF</font> | ON | ON      |
| 電源オン 初期化無し         | <font color="Red">HIGH</font>  | -      | -      | -      | -      | ON  | ON  | ON | ON      |
| M5.begin();                 | <font color="Red">HIGH</font>  | -      | -      | -      | -      | ON  | ON  | ON | ON      |
| INPUT初期化のみ             | <font color="Red">HIGH</font>  | -      | -      | -      | -      | ON  | ON  | ON | ON      |
| INPUT_PULLUP初期化のみ      | <font color="Red">HIGH</font>  | HIGH   | -      | HIGH   | HIGH   | ON  | ON  | ON | ON      |
| INPUT_PULLDOWN初期化のみ    | <font color="Red">HIGH</font>  | LOW    | -      | LOW    | LOW    | ON  | ON  | ON | ON      |
| ANALOG初期化のみ            | <font color="Red">HIGH</font>  | -      | -      | -      | -      | ON  | ON  | ON | ON      |
| OUTPUT初期化のみ            | <font color="Magenta">LOW※</font>  | LOW    | <font color="Red">----</font>      | LOW    | LOW    | ON  | ON  | ON | ON      |
| OUTPUT LOW                  | <font color="Magenta">LOW※</font>  | LOW    | <font color="Red">----</font>      | LOW    | LOW    | ON  | ON  | ON | ON      |
| OUTPUT HIGH                 | HIGH  | HIGH   | -      | HIGH   | HIGH   | ON  | ON  | ON | ON      |
| OUTPUT_OPEN_DRAIN初期化のみ | <font color="Magenta">LOW※</font>  | LOW    | -      | LOW    | LOW    | ON  | ON  | ON | ON      |
| OUTPUT_OPEN_DRAIN LOW       | <font color="Magenta">LOW※</font>  | LOW    | -      | LOW    | LOW    | ON  | ON  | ON | ON      |
| OUTPUT_OPEN_DRAIN HIGH      | <font color="Red">HIGH</font>  | -      | -      | -      | -      | ON  | ON  | ON | ON      |
| ESP32 Timer DeepSleep       | <font color="Red">HIGH</font>  | -      | -      | -      | -      | ON  | ON  | ON | ON      |
| ESP32 Timer LightSleep      | <font color="Red">HIGH</font>  | -      | -      | -      | -      | ON  | ON  | ON | ON      |
| AXP192 Sleep                | HIGH  | HIGH   | -      | HIGH   | HIGH   | ON  | ON  | ON | ON      |

LOW※は150mV程度の電圧出力あり。

## 端子別備考

### BAT端子
内蔵バッテリーの出力端子で、 3Vから4V程度が常に出力されています。

### 3V3端子
3.3Vが出力される端子で、この端子のみ電源OFFだと出力されません。

### 5V端子
5Vが出力される端子で、常に出力されています。

### GROVE 5V端子
Grove端子側の5V端子で、常に出力されています。ただ、GPIO32とGPIO33の入力は3.3Vまでなので、接続する装置によってはこの電源の5Vの入力がそのまま入る可能性があります。とはいえ、実際のところ5Vの入力を入れても壊れることはないようですが、正式には5V入力を許容していませんので注意して利用してください。

### GPIO0
基本的に3.3Vでプルアップされている端子で、電源オフ時とLOWの出力時以外はHIGHになっています。ただLOWのときにもGNDレベルではなく150mV程度の電圧が出力されていました。

また、この端子をLOWに落としている時は、起動に失敗しますので接続には注意してください。

### GPIO26
非常にシンプルな端子で、素直に動きます。また、M5StickCではDAC出力に唯一使える端子でもあります。

### GPIO36
入力専用端子で出力はできません。また、プルアップとプルダウンも利用できませんので注意しましょう。

### GPIO32, 33
Grove側の端子で、素直に動きます。Groveの電源が5Vですが、この端子の入力は3.3Vまでなので注意しましょう。
