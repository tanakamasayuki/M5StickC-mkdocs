# スリープ

ESP32には通常のアクティブモードの他に、ライトスリープモードと、ディープスリープモードがあります。

esp_sleep_enable_X_wakeup()関数群を利用して、何をトリガーにして復帰するかのウェイクアップソースを指定します。
また、esp_sleep_disable_wakeup_source()関数で指定したトリガーを無効化することもできます。

esp_sleep_pd_config()関数を利用することで、個別に周辺機器等のパワーダウンや、スリープ中での動作設定などが可能です。

## ウェイクアップソース

### タイマー

指定した時間が経過したあとにチップを起動します。
タイマーの精度は高くはないので、厳密な時間管理をしたい場合にはプログラム内部で指定時間まで待つ処理を入れる必要があります。

### タッチセンサー

タッチセンサーの割り込みでチップを起動します。タッチセンサーの値は環境によって異なるので、あらかじめtouchRead()にて、どの値になったらタッチと判定するのかを確認してから設定してください。

ESP_PD_DOMAIN_RTC_PERIPHがESP_PD_OPTION_OFFの場合、電源が供給されていないので利用できません。

### EXT0(RTC_IO)

RTC IOの1つを指定して、指定したロジックレベルになると復帰します。
また、RTCからアクセスが可能なPINである必要があるので、すべてのPINを対象にすることができません。

#### 条件

- HIGH : 指定したIOがHIGHの場合復帰
- LOW : 指定したIOがLOWの場合復帰

このモードではRTC IOモジュールが有効になっているので、内部プルアップまたはプルダウンも利用できます。
プルアップとプルダウンを利用する場合にはpinMode()にてあらかじめ設定しておく必要があります。

ESP_PD_DOMAIN_RTC_PERIPHがESP_PD_OPTION_OFFの場合、電源が供給されていないので利用できません。

### EXT1(RTC_CNTL)

複数のRTC IOを利用して、チップを起動します。
また、RTCからアクセスが可能なPINである必要があるので、すべてのPINを対象にすることができません。

#### 条件

- ESP_EXT1_WAKEUP_ANY_HIGH : 指定したIOのどれか1でもHIGHの場合復帰
- ESP_EXT1_WAKEUP_ALL_LOW : 指定したIOがすべてLOWの場合復帰

このモードではRTCコントローラーにて動くので、通常はRTC IOモジュールが無効になっています。
そのため、内部プルアップまたはプルダウンが利用できません。

利用するためにはESP_PD_DOMAIN_RTC_PERIPHをESP_PD_OPTION_ONかESP_PD_OPTION_AUTOにする必要があります。

### ULP

ULPコアプロセッサーを利用して、チップを起動します。
ULPでは各種センサーや、特定イベント検出時などを自分でプログラムして、復帰させることができます。

ESP_PD_DOMAIN_RTC_PERIPHはESP_PD_OPTION_AUTOが標準で選択されており、ULPが動いている時だけ周辺機器に電源が供給されています。

### GPIO

ライトスリープでのみ利用が可能で、複数のGPIOを利用して、チップを起動します。
EXT0やEXT1と異なり、すべてのGPIOを利用できます。

#### 条件

- HIGH : 指定したIOがHIGHの場合復帰
- LOW : 指定したIOがLOWの場合復帰

### UART

ライトスリープでのみ利用が可能で、UARTの受信を利用して、チップを起動します。
ただし、標準PIN配置のみ対応しており、UART0ではGPIO3、UART1ではGPIO9をRXとして設定する必要があります。

また、受信した信号エッジ数を復帰トリガーとしているので、最初の数文字は取りこぼします。
他の信号線が接続されていない状況以外では積極的に利用することはないと思います。

## ディープスリープ

極力停止できる機能は停止して省電力で動きます。

ディープスリープから復帰した場合には、リセットがかかったときと同じくsetup()から動きます。この時メモリの内容などは消えていますが、スローメモリの内容だけは残っています。

起動したのか、復帰したのかはesp_sleep_get_wakeup_cause()の戻り値を見ることで確認が可能です。

復帰には以下の種類があります。

- タイマー
- タッチセンサー
- EXT0(RTC_IO)
- EXT1(RTC_CNTL)
- ULP

タイマーは指定時間後に復帰するので単純です。タッチセンサーも指定したPADに触れた場合に復帰します。

EXTの2種類はちょっとわかりにくくて、EXT0はプルアップなどが可能で、1つのGPIOをHIGHかLOWのトリガーを指定して復帰できます。簡単な反面1つのGPIOでしか受け付けないのと、プルアップなどで電力を消費してしまいます。

EXI1はプルアップなどが利用できないのですが、複数のGPIOに対してどれかがHIGHになったか、すべてLOWになったかのトリガーで復帰できます。

ULPはコプロセッサーのプログラム内部から復帰できます。ULPからは一部のGPIOやI2Cなどにアクセスが可能ですので、複雑な処理も可能です。

復帰のトリガーは複数設定し、タイマーをかけつつ、タッチセンサーでも復帰することなども可能です。

## ライトスリープ

一時的にチップの処理をとめて、省電力するモードです。ディープスリープはリセットされたように、setup()から実行し直されますが、ライトスリープはスリープした場所から再開されます。

一般的にディープスリープはよく使われていますが、ライトスリープはあまり使われていないようです。ただ、トリガーまで省電力で待機するなどを簡単に実現できます。

復帰の種類は以下の7種類あります。

- タイマー
- タッチセンサー
- EXT0(RTC_IO)
- EXT1(RTC_CNTL)
- ULP
- GPIO
- UART

上5つはディープスリープと同じ方法です。GPIOはほぼEXT0と同じ機能ですが、複数のGPIOを対象にすることができます。UARTはシリアルの受信をトリガーに復帰することができます。

## 無線について

Wi-FiとBluetoothを利用している場合にはスリープに入ると電源が切れます。
ただしスリープに入る前にesp_bluedroid_disable()、esp_bt_controller_disable()、esp_wifi_stop()等で明示的に通信を無効化してください。

Wi-Fi接続を維持したい場合には、自動ライトスリープ機能を使うことで実現できます。

## スリープ設定

esp_sleep_pd_config()によって、以下の設定が可能です。
個別に使わないものをOFFに設定することで、より省電力で使うことができます。

```c
// 有効化
esp_sleep_pd_config(ESP_PD_DOMAIN_RTC_PERIPH, ESP_PD_OPTION_ON);

// 無効化
esp_sleep_pd_config(ESP_PD_DOMAIN_RTC_PERIPH, ESP_PD_OPTION_OFF);
```

設定値としてESP_PD_OPTION_AUTOがありますが、デフォルトで指定されているので、明示的に指定する必要はありません。

|        |PERIPH| SLOW | FAST | XTAL|MAX|
|--------|------|------|------|-----|---|
| **初期値** | AUTO | AUTO | AUTO | <font color="Blue">OFF</font> | X |
| **TIMER**  | <font color="Blue">OFF</font>  | <font color="Red">ON</font>   | <font color="Red">ON</font>   | <font color="Blue">OFF</font> | X |
| **TOUCH**  | <font color="Blue">OFF</font>  | <font color="Red">ON</font>   | <font color="Red">ON</font>   | <font color="Blue">OFF</font> | X |
| **EXT0**   | <font color="Red">ON</font>   | <font color="Red">ON</font>   | <font color="Red">ON</font>   | <font color="Blue">OFF</font> | X |
| **EXT1**   | <font color="Blue">OFF</font>  | <font color="Red">ON</font>   | <font color="Red">ON</font>   | <font color="Blue">OFF</font> | X |
| **ULP**    | <font color="Blue">OFF</font>  | <font color="Red">ON</font>   | <font color="Red">ON</font>   | <font color="Blue">OFF</font> | X |
| **GPIO**   | <font color="Red">ON</font>   | <font color="Red">ON</font>   | <font color="Red">ON</font>   | <font color="Blue">OFF</font> | X |
| **UART**   | <font color="Blue">OFF</font>  | <font color="Red">ON</font>   | <font color="Red">ON</font>   | <font color="Blue">OFF</font> | X |

上記がウェイクアップソース別の初期値です。
設定値はONが優先なので、EXT0とTIMERを利用した場合、ESP_PD_DOMAIN_RTC_PERIPHはONになります。

### ESP_PD_DOMAIN_RTC_PERIPH

周辺機器への電源供給を制御します。digitalWrite()などで、HIGHの出力を継続する場合などはONにする必要があります。
EXT0とGPIOを利用する場合にはONになりますが、それ以外の復帰をする場合にはOFFになります。

ただし、OFFにしてもULPが動いている間は一時的にONになり、ULPが停止するとOFFに戻ります。

同じくタッチセンサーを利用している場合にも、タッチタイマーが定期的に動いており、タッチ情報を取得しているごく短い時間だけONになり、すぐにOFFに戻ります。

### ESP_PD_DOMAIN_RTC_SLOW_MEM

ULPやディープスリープから復帰した場合に保持しておくメモリ領域への電源供給を制御します。
OFFにするとRTC_DATA_ATTR指定された変数や、RTC_SLOW_MEM[]変数の値がおかしくなります。

またULPを指定した場合にOFFにするとULP自体が動きません。

### ESP_PD_DOMAIN_RTC_FAST_MEM

ブートに関係するメモリですが、フラッシュメモリの初期化が遅い場合などに遅延を入れるコードなどが入っているようです。
OFFにしても、他に影響を与えない場合もありますが、環境によってはフラッシュメモリのエラーが発生して起動が失敗します。

### ESP_PD_DOMAIN_XTAL

水晶振動子への電源供給を制御します。通常OFFで動いており、どんな場合にONにするのかがわかりませんでした。

### ESP_PD_DOMAIN_MAX

enumの最大値を取得するためだけの設定値ですので、指定するとエラーが出ます。

