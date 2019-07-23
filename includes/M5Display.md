### コンストラクタ M5Display()
初期化作業
```c
M5Display::M5Display()
```



### 開始 begin()
SPIの開始と画面クリア
```c
void M5Display::begin()
```



### (未実装)スリープ sleep()
未実装
```c
void M5Display::sleep()
```



### (未実装)液晶の明るさ設定 setBrightness()
未実装。M5.Axp.ScreenBreath()を利用してください
```c
void M5Display::setBrightness(uint8_t brightness)
```

!!! summary "引数"
	- uint8_t `brightness` (未実装)明るさ



### Bitmap描画(const 16bit) drawBitmap()
Bitmap画像を描画する
```c
void M5Display::drawBitmap(int16_t x0, int16_t y0, int16_t w, int16_t h, const uint16_t *data)
```

!!! summary "引数"
	- int16_t `x0` 開始X座標
	- int16_t `y0` 開始Y座標
	- int16_t `w` 横幅
	- int16_t `h` 縦幅
	- const uint16_t * `data` データ



### Bitmap描画(const 8bit) drawBitmap()
Bitmap画像を描画する
```c
void M5Display::drawBitmap(int16_t x0, int16_t y0, int16_t w, int16_t h, const uint8_t *data)
```

!!! summary "引数"
	- int16_t `x0` 開始X座標
	- int16_t `y0` 開始Y座標
	- int16_t `w` 横幅
	- int16_t `h` 縦幅
	- const uint8_t * `data` データ



### Bitmap描画(16bit) drawBitmap()
Bitmap画像を描画する
```c
void M5Display::drawBitmap(int16_t x0, int16_t y0, int16_t w, int16_t h, uint16_t *data)
```

!!! summary "引数"
	- int16_t `x0` 開始X座標
	- int16_t `y0` 開始Y座標
	- int16_t `w` 横幅
	- int16_t `h` 縦幅
	- uint16_t * `data` データ



### Bitmap描画(8bit) drawBitmap()
Bitmap画像を描画する
```c
void M5Display::drawBitmap(int16_t x0, int16_t y0, int16_t w, int16_t h, uint8_t *data)
```

!!! summary "引数"
	- int16_t `x0` 開始X座標
	- int16_t `y0` 開始Y座標
	- int16_t `w` 横幅
	- int16_t `h` 縦幅
	- uint8_t * `data` データ



### Bitmap描画(16bit+透過色) drawBitmap()
Bitmap画像を描画する
```c
void M5Display::drawBitmap(int16_t x0, int16_t y0, int16_t w, int16_t h, const uint16_t *data, uint16_t transparent)
```

!!! summary "引数"
	- int16_t `x0` 開始X座標
	- int16_t `y0` 開始Y座標
	- int16_t `w` 横幅
	- int16_t `h` 縦幅
	- const uint16_t * `data` データ
	- uint16_t `transparent` 透過色



### 中国語フォントロード loadHzk16()
中国語フォントをロードする
```c
void M5Display::loadHzk16(Hzk16Types hzkTypes=InternalHzk16, const char *HZK16Path="/HZK16", const char *ASC16Path="/ASC16")
```

!!! summary "引数"
	- Hzk16Types `hzkTypes` 
	- const char * `HZK16Path` 
	- const char * `ASC16Path` 



### テキスト折返し設定 setTextWrap()
テキスト描画の折返し設定
```c
void M5Display::setTextWrap(boolean wrap)
```

!!! summary "引数"
	- boolean `wrap` 1:折返しをする, 0:折り返さない



### 中国語フォント描画 writeHzk()
中国語フォントを描画する
```c
void M5Display::writeHzk(char *c)
```

!!! summary "引数"
	- char * `c` 文字



### ハイライト設定 highlight()
テキスト描画のハイライトを設定する
```c
void M5Display::highlight(bool isHighlight)
```

!!! summary "引数"
	- bool `isHighlight` 1:ハイライトする, 0:ハイライトしない



### ハイライトカラー設定 setHighlightColor()
テキスト描画のハイライトカラーを設定する
```c
void M5Display::setHighlightColor(uint16_t color)
```

!!! summary "引数"
	- uint16_t `color` ハイライトカラー



### QRコード描画(char) qrcode()
QRコードを生成して描画する。詳細は[QRコード](../QRCode/)を参照してください。
```c
void M5Display::qrcode(const char *string, uint16_t x=5, uint16_t y=45, uint8_t width=70, uint8_t version=7)
```

!!! summary "引数"
	- const char * `string` 文字列
	- uint16_t `x` X座標
	- uint16_t `y` Y座標
	- uint8_t `width` 横幅
	- uint8_t `version` バージョン



### QRコード描画(String) qrcode()
QRコードを生成して描画する。詳細は[QRコード](../QRCode/)を参照してください。
```c
void M5Display::qrcode(const String &string, uint16_t x=5, uint16_t y=45, uint8_t width=70, uint8_t version=7)
```

!!! summary "引数"
	- const String & `string` 文字列
	- uint16_t `x` X座標
	- uint16_t `y` Y座標
	- uint8_t `width` 横幅
	- uint8_t `version` バージョン



