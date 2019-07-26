# 画面管理(M5Display)

## 概要

画面制御クラスです。非常にメンバーが多いので、概要を別ページにまとめました。

- [M5Displayクラスの使い方](../../Tips/M5Display/)

## データシート

- TFTスクリーン [ST7735S](https://github.com/m5stack/M5-Schematic/blob/master/Core/ST7735S_v1.1.pdf)


## メンバー

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



### カーソルX座標 cursor_x
カーソルのX座標
```c
int32_t TFT_eSPI::cursor_x
```


### カーソルY座標 cursor_y
カーソルのY座標
```c
int32_t TFT_eSPI::cursor_y
```


### パティング量 padX
パティングの量
```c
int32_t TFT_eSPI::padX
```


### テキスト描画色 textcolor
テキスト描画の色
```c
uint32_t TFT_eSPI::textcolor
```


### テキスト背景色 textbgcolor
テキスト背景の色
```c
uint32_t TFT_eSPI::textbgcolor
```


### Bitmap描画色 bitmap_fg
Bitmap描画の色
```c
uint32_t TFT_eSPI::bitmap_fg
```


### Bitmap背景色 bitmap_bg
Bitmap背景の色
```c
uint32_t TFT_eSPI::bitmap_bg
```


### テキストフォント textfont
テキストのフォント
```c
uint8_t TFT_eSPI::textfont
```


### テキストサイズ textsize
テキストのサイズ
```c
uint8_t TFT_eSPI::textsize
```


### テキスト描画座標 textdatum
テキスト描画座標(0-8)
```c
uint8_t TFT_eSPI::textdatum
```


### 描画方向 rotation
描画する方向(0-3)
```c
uint8_t TFT_eSPI::rotation
```


### ピボットX座標 _xpivot
ピボットのX座標
```c
int16_t TFT_eSPI::_xpivot
```


### ピボットY座標 _ypivot
ピボットのY座標
```c
int16_t TFT_eSPI::_ypivot
```


### UTF8デコーダー状態 decoderState
UTF8デコーダーの状態
```c
uint8_t TFT_eSPI::decoderState
```


### UTF8デコーダーバッファ decoderBuffer
UTF8デコーダーのバッファ
```c
uint16_t TFT_eSPI::decoderBuffer
```


### コンストラクタ TFT_eSPI()
各種初期化
```c
TFT_eSPI::TFT_eSPI(int16_t _W=TFT_WIDTH, int16_t _H=TFT_HEIGHT)
```

!!! summary "引数"
	- int16_t `_W` TFTの横幅
	- int16_t `_H` TFTの縦幅



### 初期化 init()
SPIなどの初期化を行う
```c
void TFT_eSPI::init(uint8_t tc=TAB_COLOUR)
```

!!! summary "引数"
	- uint8_t `tc` setRotation関数とsetupで使うタブの色



### 開始 begin()
内部でinit関数を呼んでいる
```c
void TFT_eSPI::begin(uint8_t tc=TAB_COLOUR)
```

!!! summary "引数"
	- uint8_t `tc` setRotation関数とsetupで使うタブの色



### 点描画 drawPixel()
点を描画する
```c
void TFT_eSPI::drawPixel(int32_t x, int32_t y, uint32_t color)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- uint32_t `color` 色



### 文字描画 drawChar()
1文字描画する
```c
void TFT_eSPI::drawChar(int32_t x, int32_t y, uint16_t c, uint32_t color, uint32_t bg, uint8_t size)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- uint16_t `c` 文字
	- uint32_t `color` 色
	- uint32_t `bg` 背景色
	- uint8_t `size` サイズ



### 線描画 drawLine()
線を描画する
```c
void TFT_eSPI::drawLine(int32_t x0, int32_t y0, int32_t x1, int32_t y1, uint32_t color)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `x1` 終了X座標
	- int32_t `y1` 終了Y座標
	- uint32_t `color` 色



### 垂直線描画 drawFastVLine()
(x, y)から高さhの線を描画
```c
void TFT_eSPI::drawFastVLine(int32_t x, int32_t y, int32_t h, uint32_t color)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- int32_t `h` 高さ
	- uint32_t `color` 色



### 水平線描画 drawFastHLine()
(x, y)から幅wの線を描画
```c
void TFT_eSPI::drawFastHLine(int32_t x, int32_t y, int32_t w, uint32_t color)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- int32_t `w` 幅
	- uint32_t `color` 色



### 塗りつぶし四角形描画 fillRect()
塗りつぶしの四角形を描画
```c
void TFT_eSPI::fillRect(int32_t x, int32_t y, int32_t w, int32_t h, uint32_t color)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- uint32_t `color` 色



### 文字描画(Unicode＋font) drawChar()
文字を描画する
```c
int16_t TFT_eSPI::drawChar(uint16_t uniCode, int32_t x, int32_t y, uint8_t font)
```

!!! summary "引数"
	- uint16_t `uniCode` 文字コード
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- uint8_t `font` フォント

!!! note "戻り値"
	描画した横幅


### 文字描画(Unicode) drawChar()
文字を描画する
```c
int16_t TFT_eSPI::drawChar(uint16_t uniCode, int32_t x, int32_t y)
```

!!! summary "引数"
	- uint16_t `uniCode` 文字コード
	- int32_t `x` X座標
	- int32_t `y` Y座標

!!! note "戻り値"
	描画した横幅


### 画面の縦幅取得 height()
画面の縦幅を取得する
```c
int16_t TFT_eSPI::height(void)
```

!!! note "戻り値"
	画面の縦幅


### 画面の横幅取得 width()
画面の横幅を取得する
```c
int16_t TFT_eSPI::width(void)
```

!!! note "戻り値"
	画面の横幅


### ウインドウ設定 setWindow()
ピクセルストリームの受け取り領域を設定する
```c
void TFT_eSPI::setWindow(int32_t xs, int32_t ys, int32_t xe, int32_t ye)
```

!!! summary "引数"
	- int32_t `xs` 開始X座標
	- int32_t `ys` 開始Y座標
	- int32_t `xe` 終了X座標
	- int32_t `ye` 終了Y座標



### 色転送(1) pushColor()
色を転送する
```c
void TFT_eSPI::pushColor(uint16_t color)
```

!!! summary "引数"
	- uint16_t `color` 色



### 色転送(複数) pushColor()
色を転送する
```c
void TFT_eSPI::pushColor(uint16_t color, uint32_t len)
```

!!! summary "引数"
	- uint16_t `color` 色
	- uint32_t `len` 長さ



### 色転送(複数+Swap) pushColors()
色を複数転送する
```c
void TFT_eSPI::pushColors(uint16_t *data, uint32_t len, bool swap=true)
```

!!! summary "引数"
	- uint16_t * `data` データ
	- uint32_t `len` 長さ
	- bool `swap` 色のバイトオーダー変換をするか



### 色転送(配列) pushColors()
色を配列から転送する
```c
void TFT_eSPI::pushColors(uint8_t *data, uint32_t len)
```

!!! summary "引数"
	- uint8_t * `data` データ
	- uint32_t `len` 長さ



### 画面塗りつぶし fillScreen()
画面を塗りつぶす
```c
void TFT_eSPI::fillScreen(uint32_t color)
```

!!! summary "引数"
	- uint32_t `color` 色



### 四角描画 drawRect()
四角を描画
```c
void TFT_eSPI::drawRect(int32_t x, int32_t y, int32_t w, int32_t h, uint32_t color)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- uint32_t `color` 色



### 角丸四角描画 drawRoundRect()
角の丸い四角を描画
```c
void TFT_eSPI::drawRoundRect(int32_t x0, int32_t y0, int32_t w, int32_t h, int32_t radius, uint32_t color)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- int32_t `radius` 角の半径
	- uint32_t `color` 色



### 塗りつぶし角丸四角描画 fillRoundRect()
塗りつぶした角丸四角を描画
```c
void TFT_eSPI::fillRoundRect(int32_t x0, int32_t y0, int32_t w, int32_t h, int32_t radius, uint32_t color)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- int32_t `radius` 角の半径
	- uint32_t `color` 色



### 描画方向設定 setRotation()
描画の方向を設定
```c
void TFT_eSPI::setRotation(uint8_t r)
```

!!! summary "引数"
	- uint8_t `r` 描画方向(0-3)



### 反転表示 invertDisplay()
反転して表示
```c
void TFT_eSPI::invertDisplay(boolean i)
```

!!! summary "引数"
	- boolean `i` 反転 0:通常, 1:反転



### 円描画 drawCircle()
円を描画
```c
void TFT_eSPI::drawCircle(int32_t x0, int32_t y0, int32_t r, uint32_t color)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `r` 半径
	- uint32_t `color` 色



### 円一部描画 drawCircleHelper()
円の一部を描画
```c
void TFT_eSPI::drawCircleHelper(int32_t x0, int32_t y0, int32_t r, uint8_t cornername, uint32_t color)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `r` 半径
	- uint8_t `cornername` 描画する円のエリアビット指定(1:左上, 2:右上, 4:右下, 8:左下)
	- uint32_t `color` 色



### 塗りつぶし円描画 fillCircle()
塗りつぶしの円を描画
```c
void TFT_eSPI::fillCircle(int32_t x0, int32_t y0, int32_t r, uint32_t color)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `r` 半径
	- uint32_t `color` 色



### 塗りつぶし円一部描画 fillCircleHelper()
塗りつぶした円を一部の描画
```c
void TFT_eSPI::fillCircleHelper(int32_t x0, int32_t y0, int32_t r, uint8_t cornername, int32_t delta, uint32_t color)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `r` 半径
	- uint8_t `cornername` 描画する円のエリアビット指定(1:左半分, 2:右半分)
	- int32_t `delta` 中央に追加され伸びる高さ
	- uint32_t `color` 色



### 楕円描画 drawEllipse()
楕円を描画する
```c
void TFT_eSPI::drawEllipse(int16_t x0, int16_t y0, int32_t rx, int32_t ry, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 開始X座標
	- int16_t `y0` 開始Y座標
	- int32_t `rx` 横幅の半径
	- int32_t `ry` 縦幅の半径
	- uint16_t `color` 色



### 塗りつぶし楕円描画 fillEllipse()
塗りつぶしの楕円を描画
```c
void TFT_eSPI::fillEllipse(int16_t x0, int16_t y0, int32_t rx, int32_t ry, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 開始X座標
	- int16_t `y0` 開始Y座標
	- int32_t `rx` 横幅の半径
	- int32_t `ry` 縦幅の半径
	- uint16_t `color` 色



### 三角描画 drawTriangle()
三角を描画
```c
void TFT_eSPI::drawTriangle(int32_t x0, int32_t y0, int32_t x1, int32_t y1, int32_t x2, int32_t y2, uint32_t color)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `x1` 中間X座標
	- int32_t `y1` 中間Y座標
	- int32_t `x2` 終了X座標
	- int32_t `y2` 終了Y座標
	- uint32_t `color` 色



### 塗りつぶし三角描画 fillTriangle()
塗りつぶしの三角を描画
```c
void TFT_eSPI::fillTriangle(int32_t x0, int32_t y0, int32_t x1, int32_t y1, int32_t x2, int32_t y2, uint32_t color)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `x1` 中間X座標
	- int32_t `y1` 中間Y座標
	- int32_t `x2` 終了X座標
	- int32_t `y2` 終了Y座標
	- uint32_t `color` 色



### Bitmap描画 drawBitmap()
Bitmapを描画
```c
void TFT_eSPI::drawBitmap(int16_t x, int16_t y, const uint8_t *bitmap, int16_t w, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` X座標
	- int16_t `y` Y座標
	- const uint8_t * `bitmap` ビットマップ
	- int16_t `w` 横幅
	- int16_t `h` 縦幅
	- uint16_t `color` 色



### XBitmap描画 drawXBitmap()
XBitmapを描画
```c
void TFT_eSPI::drawXBitmap(int16_t x, int16_t y, const uint8_t *bitmap, int16_t w, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` X座標
	- int16_t `y` Y座標
	- const uint8_t * `bitmap` ビットマップ
	- int16_t `w` 横幅
	- int16_t `h` 縦幅
	- uint16_t `color` 色



### XBitmap描画(背景色指定) drawXBitmap()
XBitmapを描画
```c
void TFT_eSPI::drawXBitmap(int16_t x, int16_t y, const uint8_t *bitmap, int16_t w, int16_t h, uint16_t fgcolor, uint16_t bgcolor)
```

!!! summary "引数"
	- int16_t `x` X座標
	- int16_t `y` Y座標
	- const uint8_t * `bitmap` ビットマップ
	- int16_t `w` 横幅
	- int16_t `h` 縦幅
	- uint16_t `fgcolor` 描画色
	- uint16_t `bgcolor` 背景色



### Bitmap描画色指定 setBitmapColor()
Bitmapの描画色を指定
```c
void TFT_eSPI::setBitmapColor(uint16_t fgcolor, uint16_t bgcolor)
```

!!! summary "引数"
	- uint16_t `fgcolor` 描画色
	- uint16_t `bgcolor` 背景色



### ピボット指定 setPivot()
ピボットを指定
```c
void TFT_eSPI::setPivot(int16_t x, int16_t y)
```

!!! summary "引数"
	- int16_t `x` ピボットX座標
	- int16_t `y` ピボットY座標



### カーソル指定 setCursor()
カーソルを指定
```c
void TFT_eSPI::setCursor(int16_t x, int16_t y)
```

!!! summary "引数"
	- int16_t `x` カーソルX座標
	- int16_t `y` カーソルY座標



### カーソル指定(+フォント) setCursor()
カーソルを指定
```c
void TFT_eSPI::setCursor(int16_t x, int16_t y, uint8_t font)
```

!!! summary "引数"
	- int16_t `x` カーソルX座標
	- int16_t `y` カーソルY座標
	- uint8_t `font` フォント



### テキスト描画色設定 setTextColor()
テキスト描画色を設定
```c
void TFT_eSPI::setTextColor(uint16_t color)
```

!!! summary "引数"
	- uint16_t `color` 色



### テキスト描画色設定(+背景色) setTextColor()
テキスト描画色を設定
```c
void TFT_eSPI::setTextColor(uint16_t fgcolor, uint16_t bgcolor)
```

!!! summary "引数"
	- uint16_t `fgcolor` 描画色
	- uint16_t `bgcolor` 背景色



### テキストサイズ設定 setTextSize()
テキストサイズを設定
```c
void TFT_eSPI::setTextSize(uint8_t size)
```

!!! summary "引数"
	- uint8_t `size` サイズ



### テキスト折返し設定 setTextWrap()
テキスト折返しを設定
```c
void TFT_eSPI::setTextWrap(boolean wrapX, boolean wrapY=false)
```

!!! summary "引数"
	- boolean `wrapX` X座標での折返し 0:しない, 1:する
	- boolean `wrapY` Y座標での折返し 0:しない, 1:する



### テキスト描画座標設定 setTextDatum()
テキスト描画座標を設定
```c
void TFT_eSPI::setTextDatum(uint8_t datum)
```

!!! summary "引数"
	- uint8_t `datum` テキスト描画座標(0-8)



### テキストパティング設定 setTextPadding()
テキストパティングを設定
```c
void TFT_eSPI::setTextPadding(uint16_t x_width)
```

!!! summary "引数"
	- uint16_t `x_width` パティング量



### GFXfont設定 setFreeFont()
GFXfontを設定
```c
void TFT_eSPI::setFreeFont(const GFXfont *f=NULL)
```

!!! summary "引数"
	- const GFXfont * `f` GFXfont



### テキストフォント設定 setTextFont()
テキストフォントを設定
```c
void TFT_eSPI::setTextFont(uint8_t font)
```

!!! summary "引数"
	- uint8_t `font` フォント



### SPI書き込み spiwrite()
SPIに1文字書き込み
```c
void TFT_eSPI::spiwrite(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` 文字



### コマンド送信 writecommand()
コマンドを送信
```c
void TFT_eSPI::writecommand(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` 文字



### データ送信 writedata()
データを送信
```c
void TFT_eSPI::writedata(uint8_t d)
```

!!! summary "引数"
	- uint8_t `d` 



### コマンド複数送信 commandList()
コマンドを複数送信
```c
void TFT_eSPI::commandList(const uint8_t *addr)
```

!!! summary "引数"
	- const uint8_t * `addr` アドレス



### コマンド受信(8bit) readcommand8()
コマンドを受信
```c
uint8_t TFT_eSPI::readcommand8(uint8_t cmd_function, uint8_t index=0)
```

!!! summary "引数"
	- uint8_t `cmd_function` コマンド関数
	- uint8_t `index` インデックス

!!! note "戻り値"
	受信結果


### コマンド受信(16bit) readcommand16()
コマンドを受信
```c
uint16_t TFT_eSPI::readcommand16(uint8_t cmd_function, uint8_t index=0)
```

!!! summary "引数"
	- uint8_t `cmd_function` コマンド関数
	- uint8_t `index` インデックス

!!! note "戻り値"
	受信結果


### コマンド受信(32bit) readcommand32()
コマンドを受信
```c
uint32_t TFT_eSPI::readcommand32(uint8_t cmd_function, uint8_t index=0)
```

!!! summary "引数"
	- uint8_t `cmd_function` コマンド関数
	- uint8_t `index` インデックス

!!! note "戻り値"
	受信結果


### 点読み込み readPixel()
点を読み込む
```c
uint16_t TFT_eSPI::readPixel(int32_t x0, int32_t y0)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標

!!! note "戻り値"
	点


### 矩形読み込み readRect()
矩形を読み込む
```c
void TFT_eSPI::readRect(int32_t x0, int32_t y0, int32_t w, int32_t h, uint16_t *data)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- uint16_t * `data` データ



### 矩形送信 pushRect()
矩形を送信
```c
void TFT_eSPI::pushRect(int32_t x0, int32_t y0, int32_t w, int32_t h, uint16_t *data)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- uint16_t * `data` データ



### 画像送信 pushImage()
画像を送信
```c
void TFT_eSPI::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, uint16_t *data)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- uint16_t * `data` データ



### 画像送信(透過色) pushImage()
画像を送信
```c
void TFT_eSPI::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, uint16_t *data, uint16_t transparent)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- uint16_t * `data` データ
	- uint16_t `transparent` 透過色



### 画像送信(PROGMEM+透過色) pushImage()
画像を送信
```c
void TFT_eSPI::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, const uint16_t *data, uint16_t transparent)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- const uint16_t * `data` データ
	- uint16_t `transparent` 透過色



### 画像送信(PROGMEM) pushImage()
画像を送信
```c
void TFT_eSPI::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, const uint16_t *data)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- const uint16_t * `data` データ



### 画像送信(8bit色) pushImage()
画像を送信
```c
void TFT_eSPI::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, uint8_t *data, bool bpp8=true)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- uint8_t * `data` データ
	- bool `bpp8` 8bit色



### 画像送信(8bit色+透過色) pushImage()
画像を送信
```c
void TFT_eSPI::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, uint8_t *data, uint8_t transparent, bool bpp8=true)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- uint8_t * `data` データ
	- uint8_t `transparent` 透過色
	- bool `bpp8` 8bit色



### スワップ設定 setSwapBytes()
スワップを設定
```c
void TFT_eSPI::setSwapBytes(bool swap)
```

!!! summary "引数"
	- bool `swap` 色のバイトオーダー変換をするか



### スワップ取得 getSwapBytes()
スワップを取得
```c
bool TFT_eSPI::getSwapBytes(void)
```

!!! note "戻り値"
	swap


### 矩形読み込み(RGB) readRectRGB()
矩形を読み込み
```c
void TFT_eSPI::readRectRGB(int32_t x0, int32_t y0, int32_t w, int32_t h, uint8_t *data)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- uint8_t * `data` データ



### 描画方向取得 getRotation()
描画方向の取得
```c
uint8_t TFT_eSPI::getRotation(void)
```

!!! note "戻り値"
	描画方向(0-3)


### テキスト描画座標取得 getTextDatum()
テキスト描画座標の取得
```c
uint8_t TFT_eSPI::getTextDatum(void)
```

!!! note "戻り値"
	テキスト描画座標(0-8)


### 色変換(16bitから8bit) color16to8()
色の変換
```c
uint8_t TFT_eSPI::color16to8(uint16_t color565)
```

!!! summary "引数"
	- uint16_t `color565` 16bit色

!!! note "戻り値"
	8bit色


### カーソルX座標取得 getCursorX()
カーソルX座標の取得
```c
int16_t TFT_eSPI::getCursorX(void)
```

!!! note "戻り値"
	カーソルX座標


### カーソルY座標取得 getCursorY()
カーソルY座標の取得
```c
int16_t TFT_eSPI::getCursorY(void)
```

!!! note "戻り値"
	カーソルY座標


### ピボットX座標取得 getPivotX()
ピボットX座標の取得
```c
int16_t TFT_eSPI::getPivotX(void)
```

!!! note "戻り値"
	ピボットX座標


### ピボットY座標取得 getPivotY()
ピボットY座標の取得
```c
int16_t TFT_eSPI::getPivotY(void)
```

!!! note "戻り値"
	ピボットY座標


### フォント読み込み状態取得 fontsLoaded()
フォント読み込み状態の取得
```c
uint16_t TFT_eSPI::fontsLoaded(void)
```

!!! note "戻り値"
	フォント読み込み状態


### 色変換(32bitから16ビット) color565()
色の変換
```c
uint16_t TFT_eSPI::color565(uint8_t red, uint8_t green, uint8_t blue)
```

!!! summary "引数"
	- uint8_t `red` 赤(0-255)
	- uint8_t `green` 緑(0-255)
	- uint8_t `blue` 青(0-255)

!!! note "戻り値"
	16bit色


### 色変換(8bitから16ビット) color8to16()
色の変換
```c
uint16_t TFT_eSPI::color8to16(uint8_t color332)
```

!!! summary "引数"
	- uint8_t `color332` 8bit色

!!! note "戻り値"
	16bit色


### 数字描画(+font) drawNumber()
数字の描画
```c
int16_t TFT_eSPI::drawNumber(long long_num, int32_t poX, int32_t poY, uint8_t font)
```

!!! summary "引数"
	- long `long_num` 数字
	- int32_t `poX` X座標
	- int32_t `poY` Y座標
	- uint8_t `font` フォント

!!! note "戻り値"
	描画横幅


### 数字描画 drawNumber()
数字の描画
```c
int16_t TFT_eSPI::drawNumber(long long_num, int32_t poX, int32_t poY)
```

!!! summary "引数"
	- long `long_num` 数字
	- int32_t `poX` X座標
	- int32_t `poY` Y座標

!!! note "戻り値"
	描画横幅


### 浮動小数点描画(+font) drawFloat()
浮動小数点の描画
```c
int16_t TFT_eSPI::drawFloat(float floatNumber, uint8_t decimal, int32_t poX, int32_t poY, uint8_t font)
```

!!! summary "引数"
	- float `floatNumber` 
	- uint8_t `decimal` 
	- int32_t `poX` X座標
	- int32_t `poY` Y座標
	- uint8_t `font` フォント

!!! note "戻り値"
	描画横幅


### 浮動小数点描画 drawFloat()
浮動小数点の描画
```c
int16_t TFT_eSPI::drawFloat(float floatNumber, uint8_t decimal, int32_t poX, int32_t poY)
```

!!! summary "引数"
	- float `floatNumber` 
	- uint8_t `decimal` 
	- int32_t `poX` X座標
	- int32_t `poY` Y座標

!!! note "戻り値"
	描画横幅


### 文字列描画(+font) drawString()
文字列の描画
```c
int16_t TFT_eSPI::drawString(const char *string, int32_t poX, int32_t poY, uint8_t font)
```

!!! summary "引数"
	- const char * `string` 文字列
	- int32_t `poX` X座標
	- int32_t `poY` Y座標
	- uint8_t `font` フォント

!!! note "戻り値"
	描画横幅


### 文字列描画 drawString()
文字列の描画
```c
int16_t TFT_eSPI::drawString(const char *string, int32_t poX, int32_t poY)
```

!!! summary "引数"
	- const char * `string` 文字列
	- int32_t `poX` X座標
	- int32_t `poY` Y座標

!!! note "戻り値"
	描画横幅


### 中央寄せ文字列描画(+font) drawCentreString()
中央寄せの文字列描画
```c
int16_t TFT_eSPI::drawCentreString(const char *string, int32_t dX, int32_t poY, uint8_t font)
```

!!! summary "引数"
	- const char * `string` 文字列
	- int32_t `dX` 
	- int32_t `poY` Y座標
	- uint8_t `font` フォント

!!! note "戻り値"
	描画横幅


### 右寄せ文字列描画(+font) drawRightString()
右寄せ文字列の描画
```c
int16_t TFT_eSPI::drawRightString(const char *string, int32_t dX, int32_t poY, uint8_t font)
```

!!! summary "引数"
	- const char * `string` 文字列
	- int32_t `dX` 
	- int32_t `poY` Y座標
	- uint8_t `font` フォント

!!! note "戻り値"
	描画横幅


### 文字列描画(const String+font) drawString()
文字列の描画
```c
int16_t TFT_eSPI::drawString(const String &string, int32_t poX, int32_t poY, uint8_t font)
```

!!! summary "引数"
	- const String & `string` 文字列
	- int32_t `poX` X座標
	- int32_t `poY` Y座標
	- uint8_t `font` フォント

!!! note "戻り値"
	描画横幅


### 文字列描画(String) drawString()
文字列の描画
```c
int16_t TFT_eSPI::drawString(const String &string, int32_t poX, int32_t poY)
```

!!! summary "引数"
	- const String & `string` 文字列
	- int32_t `poX` X座標
	- int32_t `poY` Y座標

!!! note "戻り値"
	描画横幅


### 中央寄せ文字列描画(String+font) drawCentreString()
中央寄せ文字列の描画
```c
int16_t TFT_eSPI::drawCentreString(const String &string, int32_t dX, int32_t poY, uint8_t font)
```

!!! summary "引数"
	- const String & `string` 文字列
	- int32_t `dX` 
	- int32_t `poY` Y座標
	- uint8_t `font` フォント

!!! note "戻り値"
	描画横幅


### 右寄せ文字列描画(String+font) drawRightString()
右寄せ文字列の描画
```c
int16_t TFT_eSPI::drawRightString(const String &string, int32_t dX, int32_t poY, uint8_t font)
```

!!! summary "引数"
	- const String & `string` 文字列
	- int32_t `dX` 
	- int32_t `poY` Y座標
	- uint8_t `font` フォント

!!! note "戻り値"
	描画横幅


### テキスト横幅取得(+font) textWidth()
テキストの横幅の取得
```c
int16_t TFT_eSPI::textWidth(const char *string, uint8_t font)
```

!!! summary "引数"
	- const char * `string` 文字列
	- uint8_t `font` フォント

!!! note "戻り値"
	テキスト横幅


### テキスト横幅取得 textWidth()
テキストの横幅の取得
```c
int16_t TFT_eSPI::textWidth(const char *string)
```

!!! summary "引数"
	- const char * `string` 文字列

!!! note "戻り値"
	テキスト横幅


### テキスト横幅取得(String+font) textWidth()
テキストの横幅の取得
```c
int16_t TFT_eSPI::textWidth(const String &string, uint8_t font)
```

!!! summary "引数"
	- const String & `string` 文字列
	- uint8_t `font` フォント

!!! note "戻り値"
	テキスト横幅


### テキスト横幅取得(String) textWidth()
テキストの横幅の取得
```c
int16_t TFT_eSPI::textWidth(const String &string)
```

!!! summary "引数"
	- const String & `string` 文字列

!!! note "戻り値"
	テキスト横幅


### テキスト縦幅取得 fontHeight()
テキストの縦幅の取得
```c
int16_t TFT_eSPI::fontHeight(int16_t font)
```

!!! summary "引数"
	- int16_t `font` フォント

!!! note "戻り値"
	テキスト縦幅


### フォント縦幅取得 fontHeight()
フォントの縦幅の取得
```c
int16_t TFT_eSPI::fontHeight(void)
```

!!! note "戻り値"
	フォント縦幅


### 描画ウインドウ設定 setAddrWindow()
描画ウインドウを設定
```c
void TFT_eSPI::setAddrWindow(int32_t xs, int32_t ys, int32_t w, int32_t h)
```

!!! summary "引数"
	- int32_t `xs` X座標
	- int32_t `ys` Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅



### 送信開始 startWrite()
SPI送信の開始
```c
void TFT_eSPI::startWrite(void)
```



### 色送信（16bit） writeColor()
色の送信
```c
void TFT_eSPI::writeColor(uint16_t color, uint32_t len)
```

!!! summary "引数"
	- uint16_t `color` 色
	- uint32_t `len` 長さ



### 送信完了 endWrite()
SPI送信の完了
```c
void TFT_eSPI::endWrite(void)
```



### UTF8デコード(複数バイト) decodeUTF8()
UTF8をUNICODEにデコード
```c
uint16_t TFT_eSPI::decodeUTF8(uint8_t *buf, uint16_t *index, uint16_t remaining)
```

!!! summary "引数"
	- uint8_t * `buf` UTF8
	- uint16_t * `index` インデックス
	- uint16_t `remaining` 追加バイト数

!!! note "戻り値"
	UNICODE


### UTF8デコード(1バイト) decodeUTF8()
UTF8をUNICODEにデコード
```c
uint16_t TFT_eSPI::decodeUTF8(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` UTF8

!!! note "戻り値"
	UNICODE


### 文字送信 write()
文字を送信
```c
size_t TFT_eSPI::write(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` 文字

!!! note "戻り値"
	1固定


### 属性設定 setAttribute()
属性の設定
```c
void TFT_eSPI::setAttribute(uint8_t id=0, uint8_t a=0)
```

!!! summary "引数"
	- uint8_t `id` 属性ID
	- uint8_t `a` 設定値



### 属性取得 getAttribute()
属性の取得
```c
uint8_t TFT_eSPI::getAttribute(uint8_t id=0)
```

!!! summary "引数"
	- uint8_t `id` 属性ID

!!! note "戻り値"
	設定値


### 設定取得 getSetup()
設定の取得
```c
void TFT_eSPI::getSetup(setup_t &tft_settings)
```

!!! summary "引数"
	- setup_t& `tft_settings` 設定


## 関連ブログ
- [M5StickCのDisplay周り解析](https://lang-ship.com/blog/?p=590)
- [[実験] M5StickC組み込み漢字をテスト](https://lang-ship.com/blog/?p=602)
- [[実験] M5StickCでArduino用美咲フォントライブラを使ってみた](https://lang-ship.com/blog/?p=607)
- [[実験] Arduino(M5StickC)でefont Unicodeフォント表示 PROGMEM版](https://lang-ship.com/blog/?p=631)
- [[実験] Arduino(M5StickC)でefont Unicodeフォント表示 SPIFFS版](https://lang-ship.com/blog/?p=637)
- [Arduino(M5StickC)でefont Unicodeフォント表示 完結編](https://lang-ship.com/blog/?p=646)


