# スプライト(TFT_eSprite)

## 概要

スプライト表示ライブラリ。標準で入っているクラスですが、利用例が少ないのであまり利用しないほうが無難です。

## メンバー

### コンストラクタ TFT_eSprite()
初期化
```c
TFT_eSprite::TFT_eSprite(TFT_eSPI *tft)
```

!!! summary "引数"
	- TFT_eSPI* `tft` 親クラス



### スプライト作成 createSprite()
スプライトを作成
```c
void * TFT_eSprite::createSprite(int16_t width, int16_t height, uint8_t frames=1)
```

!!! summary "引数"
	- int16_t `width` 横幅
	- int16_t `height` 縦幅
	- uint8_t `frames` フレーム



### スプライト削除 deleteSprite()
スプライトを削除
```c
void TFT_eSprite::deleteSprite(void)
```



### フレームバッファ選択 frameBuffer()
フレームバッファを選択
```c
void * TFT_eSprite::frameBuffer(int8_t f)
```

!!! summary "引数"
	- int8_t `f` フレーム(1 or 2)



### 色ビット数選択 setColorDepth()
色のビット数を選択
```c
void * TFT_eSprite::setColorDepth(int8_t b)
```

!!! summary "引数"
	- int8_t `b` ビット数(1, 8 or 16)



### 色ビット数取得 getColorDepth()
色のビット数を取得
```c
int8_t TFT_eSprite::getColorDepth(void)
```

!!! note "戻り値"
	ビット数(1, 8 or 16)


### Bitmap描画色設定 setBitmapColor()
Bitmapの描画色を設定
```c
void TFT_eSprite::setBitmapColor(uint16_t c, uint16_t b)
```

!!! summary "引数"
	- uint16_t `c` 描画色
	- uint16_t `b` 背景色



### 点描画 drawPixel()
点を描画
```c
void TFT_eSprite::drawPixel(int32_t x, int32_t y, uint32_t color)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- uint32_t `color` カラー



### 文字描画 drawChar()
文字を描画
```c
void TFT_eSprite::drawChar(int32_t x, int32_t y, uint16_t c, uint32_t color, uint32_t bg, uint8_t size)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- uint16_t `c` 文字
	- uint32_t `color` 描画色
	- uint32_t `bg` 背景色
	- uint8_t `size` フォントサイズ



### スプライト塗りつぶし fillSprite()
スプライトを塗りつぶす
```c
void TFT_eSprite::fillSprite(uint32_t color)
```

!!! summary "引数"
	- uint32_t `color` カラー



### 描画ウインドウ設定 setWindow()
描画ウインドウを設定
```c
void TFT_eSprite::setWindow(int32_t x0, int32_t y0, int32_t x1, int32_t y1)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `x1` 完了X座標
	- int32_t `y1` 完了Y座標



### 描画ウインドウ色送信 pushColor()
描画ウインドウに色を送信
```c
void TFT_eSprite::pushColor(uint32_t color)
```

!!! summary "引数"
	- uint32_t `color` カラー



### 描画ウインドウ色送信(複数) pushColor()
描画ウインドウに色を送信
```c
void TFT_eSprite::pushColor(uint32_t color, uint16_t len)
```

!!! summary "引数"
	- uint32_t `color` カラー
	- uint16_t `len` 長さ



### 色送信 writeColor()
色を送信
```c
void TFT_eSprite::writeColor(uint16_t color)
```

!!! summary "引数"
	- uint16_t `color` カラー



### スクロール矩形設定 setScrollRect()
スクロール矩形を設定
```c
void TFT_eSprite::setScrollRect(int32_t x, int32_t y, int32_t w, int32_t h, uint16_t color=TFT_BLACK)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- uint16_t `color` カラー



### スクロール設定 scroll()
スクロールを設定
```c
void TFT_eSprite::scroll(int16_t dx, int16_t dy=0)
```

!!! summary "引数"
	- int16_t `dx` X座標
	- int16_t `dy` Y座標



### 線描画 drawLine()
線を描画
```c
void TFT_eSprite::drawLine(int32_t x0, int32_t y0, int32_t x1, int32_t y1, uint32_t color)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `x1` 完了X座標
	- int32_t `y1` 完了Y座標
	- uint32_t `color` カラー



### 垂直線描画 drawFastVLine()
垂直線を描画
```c
void TFT_eSprite::drawFastVLine(int32_t x, int32_t y, int32_t h, uint32_t color)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- int32_t `h` 縦幅
	- uint32_t `color` カラー



### 水平線描画 drawFastHLine()
水平線を描画
```c
void TFT_eSprite::drawFastHLine(int32_t x, int32_t y, int32_t w, uint32_t color)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- int32_t `w` 横幅
	- uint32_t `color` カラー



### 矩形描画 fillRect()
矩形を描画
```c
void TFT_eSprite::fillRect(int32_t x, int32_t y, int32_t w, int32_t h, uint32_t color)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- uint32_t `color` カラー



### 画面描画方向設定 setRotation()
画面の描画方向を設定
```c
void TFT_eSprite::setRotation(uint8_t rotation)
```

!!! summary "引数"
	- uint8_t `rotation` 画面描画方向(0-3)



### 画面描画方向取得 getRotation()
画面描画方向を取得
```c
uint8_t TFT_eSprite::getRotation(void)
```

!!! note "戻り値"
	画面描画方向(0-3)


### 描画(回転) pushRotated()
回転して描画
```c
bool TFT_eSprite::pushRotated(int16_t angle, int32_t transp=-1)
```

!!! summary "引数"
	- int16_t `angle` 角度
	- int32_t `transp` 透過色

!!! note "戻り値"
	描画結果(true:成功, false:失敗)


### スプライト描画(回転) pushRotated()
スプライトを回転して描画
```c
bool TFT_eSprite::pushRotated(TFT_eSprite *spr, int16_t angle, int32_t transp=-1)
```

!!! summary "引数"
	- TFT_eSprite* `spr` スプライト
	- int16_t `angle` 角度
	- int32_t `transp` 透過色

!!! note "戻り値"
	描画結果(true:成功, false:失敗)


### ピボット設定 setPivot()
ピボットを設定
```c
void TFT_eSprite::setPivot(int16_t x, int16_t y)
```

!!! summary "引数"
	- int16_t `x` X座標
	- int16_t `y` Y座標



### ピボットX座標設定 getPivotX()
ピボットX座標を設定
```c
int16_t TFT_eSprite::getPivotX(void)
```

!!! note "戻り値"
	ピボットX座標


### ピボットY座標設定 getPivotY()
ピボットY座標を設定
```c
int16_t TFT_eSprite::getPivotY(void)
```

!!! note "戻り値"
	ピボットY座標


### 回転バウンディング取得 getRotatedBounds()
回転したバウンディングを取得
```c
void TFT_eSprite::getRotatedBounds(float sina, float cosa, int16_t w, int16_t h, int16_t xp, int16_t yp, int16_t *min_x, int16_t *min_y, int16_t *max_x, int16_t *max_y)
```

!!! summary "引数"
	- float `sina` サイン値
	- float `cosa` コサイン値
	- int16_t `w` 横幅
	- int16_t `h` 縦幅
	- int16_t `xp` X座標
	- int16_t `yp` Y座標
	- int16_t * `min_x` 最小X座標
	- int16_t * `min_y` 最小Y座標
	- int16_t * `max_x` 最大X座標
	- int16_t * `max_y` 最大Y座標



### 点取得 readPixel()
点を取得
```c
uint16_t TFT_eSprite::readPixel(int32_t x0, int32_t y0)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標

!!! note "戻り値"
	色


### イメージ送信 pushImage()
イメージを送信
```c
void TFT_eSprite::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, uint16_t *data)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- uint16_t * `data` データ



### イメージ送信(const) pushImage()
イメージを送信
```c
void TFT_eSprite::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, const uint16_t *data)
```

!!! summary "引数"
	- int32_t `x0` 開始X座標
	- int32_t `y0` 開始Y座標
	- int32_t `w` 横幅
	- int32_t `h` 縦幅
	- const uint16_t * `data` データ



### スワップ設定 setSwapBytes()
スワップを設定
```c
void TFT_eSprite::setSwapBytes(bool swap)
```

!!! summary "引数"
	- bool `swap` 色のバイトオーダー変換をするか



### スワップ取得 getSwapBytes()
スワップを取得
```c
bool TFT_eSprite::getSwapBytes(void)
```

!!! note "戻り値"
	swap


### スプライト描画 pushSprite()
スプライトを描画
```c
void TFT_eSprite::pushSprite(int32_t x, int32_t y)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標



### スプライト描画(透過色) pushSprite()
スプライトを描画
```c
void TFT_eSprite::pushSprite(int32_t x, int32_t y, uint16_t transparent)
```

!!! summary "引数"
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- uint16_t `transparent` 透過色



### 文字描画(font) drawChar()
文字を描画
```c
int16_t TFT_eSprite::drawChar(uint16_t uniCode, int32_t x, int32_t y, uint8_t font)
```

!!! summary "引数"
	- uint16_t `uniCode` UNICODE
	- int32_t `x` X座標
	- int32_t `y` Y座標
	- uint8_t `font` フォント

!!! note "戻り値"
	描画横幅


### 文字描画 drawChar()
文字を描画
```c
int16_t TFT_eSprite::drawChar(uint16_t uniCode, int32_t x, int32_t y)
```

!!! summary "引数"
	- uint16_t `uniCode` UNICODE
	- int32_t `x` X座標
	- int32_t `y` Y座標

!!! note "戻り値"
	描画横幅


### 画面横幅取得 width()
画面の横幅を取得
```c
int16_t TFT_eSprite::width(void)
```

!!! note "戻り値"
	画面横幅


### 画面縦幅取得 height()
画面の縦幅を取得
```c
int16_t TFT_eSprite::height(void)
```

!!! note "戻り値"
	画面縦幅


### 文字描画 write()
文字を描画
```c
size_t TFT_eSprite::write(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` 

!!! note "戻り値"
	描画横幅


### 文字描画 drawGlyph()
文字を描画
```c
void TFT_eSprite::drawGlyph(uint16_t code)
```

!!! summary "引数"
	- uint16_t `code` 文字コード



### (未実装)スプライト文字描画 printToSprite()
(未実装)スプライトに文字を描画
```c
void TFT_eSprite::printToSprite(String string)
```

!!! summary "引数"
	- String `string` 文字列



### (未実装)スプライト文字列描画 printToSprite()
(未実装)スプライトに文字列を描画
```c
void TFT_eSprite::printToSprite(char *cbuffer, uint16_t len)
```

!!! summary "引数"
	- char * `cbuffer` 
	- uint16_t `len` 長さ



### (未実装)スプライト文字描画 printToSprite()
(未実装)スプライトに文字を描画
```c
int16_t TFT_eSprite::printToSprite(int16_t x, int16_t y, uint16_t index)
```

!!! summary "引数"
	- int16_t `x` X座標
	- int16_t `y` Y座標
	- uint16_t `index` インデックス

!!! note "戻り値"
	描画横幅



