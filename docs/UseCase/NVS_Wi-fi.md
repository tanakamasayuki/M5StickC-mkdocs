# Wi-Fiアクセスポイント情報保存、取得

プログラムの中にアクセスポイント情報を記述すると、Wi-Fi環境が変わった場合に大変ですので、NVS(Non-Volatile Storage)領域に保存することで使い回しが可能です。

ただし、NVS領域は暗号化されていませんので、端末の内部を解析することで、保存されている情報が抜き出される可能性があります。

設定専用のアプリを作るか、Webブラウザ経由で設定ページを作ると便利だと思います。

## 保存方法

```
#include <Preferences.h>

Preferences preferences;

void setup() {
  preferences.begin("Wi-Fi", false);
  preferences.putString("ssid", "******");
  preferences.putString("key", "*************");
  preferences.end();
}

void loop() {
}
```

begin()でセクション名を指定して開始し、put系関数で保存します。

## 取得方法

```
#include <Preferences.h>

Preferences preferences;
char wifi_ssid[33];
char wifi_key[65];

void setup() {
  M5.begin();

  // Wi-Fiアクセスポイント情報取得
  preferences.begin("Wi-Fi", true);
  preferences.getString("ssid", wifi_ssid, sizeof(wifi_ssid));
  preferences.getString("key", wifi_key, sizeof(wifi_key));
  preferences.end();
}

void loop() {
}
```

保存とほぼ同じですが、begin()にtrueを指定すると読み込み専用になります。

get系関数を利用して、取得することができます。
