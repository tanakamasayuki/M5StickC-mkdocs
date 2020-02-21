# I2C

## 概要

2本の信号線を利用した比較的低速の通信方式。概ね100Kから400K程度の転送速度です。

M5StickCは上側に外部接続用のピンソケットと、下側にGrove端子がついています。
入力専用のIO36を除き、外部接続可能な4PINはどんな組み合わせでもI2Cで通信が可能です。

IO26とIO0のような組み合わせも可能でしたが、通常はピンソケットのIO0とIO26、Grove端子のIO32とIO33の組み合わせで使うと思います。

M5StickCは内部で1つのI2C通信を行っているため、あと1つのI2C通信をすることが可能です。

またArduino環境ではI2Cのマスター動作しかライブラリが用意されていません。マイコンなどと接続する場合にはUARTなど他の通信プロトコルを検討してください。

## 内蔵ピンアサイン

- Wire1 SDA:IO21, SCL:IO22

上記が内部で宣言されて、電源管理やRTC接続で利用されています。

## おすすめピンアサイン

- ピンソケット SDA:IO0, SCL:IO26
- Grove端子 SDA:IO32, SCL:IO33

GroveのI2C端子が上記のアサインなので、逆に使うと混乱します。
ピンソケット側はどちらでも構わないのですが、OfficialのI2Cを使ったHATがこのピンアサインだったので、こちらを使ったほうが無難だと思います。

## サンプルプログラム
```
#include <M5StickC.h>

void setup() {
  M5.begin();

  Wire.begin(32, 33);
}

void loop() {
  byte error, address;
  int nDevices;

  Serial.println("Scanning... Wire");

  nDevices = 0;
  for (address = 1; address < 127; address++ )
  {
    Wire.beginTransmission(address);
    error = Wire.endTransmission();

    if (error == 0)
    {
      Serial.print("I2C device found at address 0x");
      if (address < 16)
        Serial.print("0");
      Serial.print(address, HEX);
      Serial.println("  !");

      nDevices++;
    }
    else if (error == 4)
    {
      Serial.print("Unknown error at address 0x");
      if (address < 16)
        Serial.print("0");
      Serial.println(address, HEX);
    }
  }
  if (nDevices == 0)
    Serial.println("No I2C devices found\n");
  else
    Serial.println("done\n");

  delay(5000);
}
```

上記のコードはI2Cのアドレス検索をするサンプルです。I2Cを接続した場合には利用できるかスキャンしてからの方が、問題の切り分けがしやすいです。

## 2系統同時に使う方法(ピンソケット＋Grove接続I2C)
```
void setup() {
  M5.begin();
 
  Wire.begin(32, 33);
  Wire1.begin(0, 26);
}
```

内部のI2C通信を使わないのであれば、同時に利用が可能です。

Wireが1系統目のI2C通信で、Wire1が2系統目のI2C通信です。通常Wire1は電源管理などの内部接続用I2Cとして使われています。

M5.begin()で電源管理の初期化をしてしまえば、あとは接続していなくても問題ないかと思いますので、Wire1.begin()で別のピンにアサインしなおします。

## 3系統同時に使う方法(ピンソケット＋Grove＋内部接続I2C)
```
#include <M5StickC.h>
 
void setup() {
  M5.begin();
 
  Wire.begin(32, 33);
}
 
void loop() {
  byte error, address;
  int nDevices;
 
  Serial.println("Scanning... Wire");
 
  nDevices = 0;
  for (address = 1; address < 127; address++ )
  {
    Wire.beginTransmission(address);
    error = Wire.endTransmission();
 
    if (error == 0)
    {
      Serial.print("I2C device found at address 0x");
      if (address < 16)
        Serial.print("0");
      Serial.print(address, HEX);
      Serial.println("  !");
 
      nDevices++;
    }
    else if (error == 4)
    {
      Serial.print("Unknown error at address 0x");
      if (address < 16)
        Serial.print("0");
      Serial.println(address, HEX);
    }
  }
  if (nDevices == 0)
    Serial.println("No I2C devices found\n");
  else
    Serial.println("done\n");
 
  Serial.println("Scanning... Wire1");
  Wire1.begin(0, 26);
 
  nDevices = 0;
  for (address = 1; address < 127; address++ )
  {
    Wire1.beginTransmission(address);
    error = Wire1.endTransmission();
 
    if (error == 0)
    {
      Serial.print("I2C device found at address 0x");
      if (address < 16)
        Serial.print("0");
      Serial.print(address, HEX);
      Serial.println("  !");
 
      nDevices++;
    }
    else if (error == 4)
    {
      Serial.print("Unknown error at address 0x");
      if (address < 16)
        Serial.print("0");
      Serial.println(address, HEX);
    }
  }
  if (nDevices == 0)
    Serial.println("No I2C devices found\n");
  else
    Serial.println("done\n");
 
  Serial.println("Scanning... Wire1-2");
  Wire1.begin(21, 22);
 
  nDevices = 0;
  for (address = 1; address < 127; address++ )
  {
    Wire1.beginTransmission(address);
    error = Wire1.endTransmission();
 
    if (error == 0)
    {
      Serial.print("I2C device found at address 0x");
      if (address < 16)
        Serial.print("0");
      Serial.print(address, HEX);
      Serial.println("  !");
 
      nDevices++;
    }
    else if (error == 4)
    {
      Serial.print("Unknown error at address 0x");
      if (address < 16)
        Serial.print("0");
      Serial.println(address, HEX);
    }
  }
  if (nDevices == 0)
    Serial.println("No I2C devices found\n");
  else
    Serial.println("done\n");
 
  delay(5000);
}
```

I2Cのアドレススキャナで検証しましたが、使う前にbegin()でアドレス指定をすれば使えそうです。

ただ、複数使うのはトラブルになりそうなので、可能であればピンソケットかGroveのどちらか1系統だけを使ったほうが安全だと思います。

## クラスリファレンス
- [Class/ESP32/TwoWire](../../Class/ESP32/TwoWire/)

## リファレンス
- [espressif](https://docs.espressif.com/projects/esp-idf/en/latest/api-reference/peripherals/i2c.html)

## 公式サンプルコード
- Git Hub [M5StickC/examples/Hat/ENV](https://github.com/m5stack/M5StickC/blob/master/examples/Hat/ENV)
- Git Hub [M5StickC/examples/Hat/MLX90640](https://github.com/m5stack/M5StickC/tree/master/examples/Hat/MLX90640)
- Git Hub [M5StickC/examples/Hat/NCIR_Hat](https://github.com/m5stack/M5StickC/blob/master/examples/Hat/NCIR_HAT)


## 関連ブログ

- [M5StickCのIOについて調べてみた](https://lang-ship.com/blog/?p=658)
- [M5StickCでI2C通信をする](https://lang-ship.com/blog/?p=674)
