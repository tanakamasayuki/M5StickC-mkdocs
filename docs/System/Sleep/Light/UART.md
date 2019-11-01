# UART

シリアル受信にて復帰します。
しかしながらM5StickCではピンアサインの関係で利用できません。

## 利用前提

UARTで受信トリガーにできるのは標準PIN配置のUARTだけで、UART0ではGPIO3、UART1ではGPIO9をRXとして設定する必要があります。

受信した信号エッジ数を復帰トリガーとしているので、最初の数文字は取りこぼします。他の信号線が接続されていない状況以外では積極的に利用することはないと思います。
