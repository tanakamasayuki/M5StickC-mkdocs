###  TFT_eSprite()

```c
TFT_eSprite::TFT_eSprite(TFT_eSPI *tft)
```



###  createSprite()

```c
void * TFT_eSprite::createSprite(int16_t width, int16_t height, uint8_t frames=1)
```



###  deleteSprite()

```c
void TFT_eSprite::deleteSprite(void)
```



###  frameBuffer()

```c
void * TFT_eSprite::frameBuffer(int8_t f)
```



###  setColorDepth()

```c
void * TFT_eSprite::setColorDepth(int8_t b)
```



###  getColorDepth()

```c
int8_t TFT_eSprite::getColorDepth(void)
```



###  setBitmapColor()

```c
void TFT_eSprite::setBitmapColor(uint16_t c, uint16_t b)
```



###  drawPixel()

```c
void TFT_eSprite::drawPixel(int32_t x, int32_t y, uint32_t color)
```



###  drawChar()

```c
void TFT_eSprite::drawChar(int32_t x, int32_t y, uint16_t c, uint32_t color, uint32_t bg, uint8_t size)
```



###  fillSprite()

```c
void TFT_eSprite::fillSprite(uint32_t color)
```



###  setWindow()

```c
void TFT_eSprite::setWindow(int32_t x0, int32_t y0, int32_t x1, int32_t y1)
```



###  pushColor()

```c
void TFT_eSprite::pushColor(uint32_t color)
```



###  pushColor()

```c
void TFT_eSprite::pushColor(uint32_t color, uint16_t len)
```



###  writeColor()

```c
void TFT_eSprite::writeColor(uint16_t color)
```



###  setScrollRect()

```c
void TFT_eSprite::setScrollRect(int32_t x, int32_t y, int32_t w, int32_t h, uint16_t color=TFT_BLACK)
```



###  scroll()

```c
void TFT_eSprite::scroll(int16_t dx, int16_t dy=0)
```



###  drawLine()

```c
void TFT_eSprite::drawLine(int32_t x0, int32_t y0, int32_t x1, int32_t y1, uint32_t color)
```



###  drawFastVLine()

```c
void TFT_eSprite::drawFastVLine(int32_t x, int32_t y, int32_t h, uint32_t color)
```



###  drawFastHLine()

```c
void TFT_eSprite::drawFastHLine(int32_t x, int32_t y, int32_t w, uint32_t color)
```



###  fillRect()

```c
void TFT_eSprite::fillRect(int32_t x, int32_t y, int32_t w, int32_t h, uint32_t color)
```



###  setRotation()

```c
void TFT_eSprite::setRotation(uint8_t rotation)
```



###  getRotation()

```c
uint8_t TFT_eSprite::getRotation(void)
```



###  pushRotated()

```c
bool TFT_eSprite::pushRotated(int16_t angle, int32_t transp=-1)
```



###  pushRotated()

```c
bool TFT_eSprite::pushRotated(TFT_eSprite *spr, int16_t angle, int32_t transp=-1)
```



###  setPivot()

```c
void TFT_eSprite::setPivot(int16_t x, int16_t y)
```



###  getPivotX()

```c
int16_t TFT_eSprite::getPivotX(void)
```



###  getPivotY()

```c
int16_t TFT_eSprite::getPivotY(void)
```



###  getRotatedBounds()

```c
void TFT_eSprite::getRotatedBounds(float sina, float cosa, int16_t w, int16_t h, int16_t xp, int16_t yp, int16_t *min_x, int16_t *min_y, int16_t *max_x, int16_t *max_y)
```



###  readPixel()

```c
uint16_t TFT_eSprite::readPixel(int32_t x0, int32_t y0)
```



###  pushImage()

```c
void TFT_eSprite::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, uint16_t *data)
```



###  pushImage()

```c
void TFT_eSprite::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, const uint16_t *data)
```



###  setSwapBytes()

```c
void TFT_eSprite::setSwapBytes(bool swap)
```



###  getSwapBytes()

```c
bool TFT_eSprite::getSwapBytes(void)
```



###  pushSprite()

```c
void TFT_eSprite::pushSprite(int32_t x, int32_t y)
```



###  pushSprite()

```c
void TFT_eSprite::pushSprite(int32_t x, int32_t y, uint16_t transparent)
```



###  drawChar()

```c
int16_t TFT_eSprite::drawChar(uint16_t uniCode, int32_t x, int32_t y, uint8_t font)
```



###  drawChar()

```c
int16_t TFT_eSprite::drawChar(uint16_t uniCode, int32_t x, int32_t y)
```



###  width()

```c
int16_t TFT_eSprite::width(void)
```



###  height()

```c
int16_t TFT_eSprite::height(void)
```



###  write()

```c
size_t TFT_eSprite::write(uint8_t)
```



###  drawGlyph()

```c
void TFT_eSprite::drawGlyph(uint16_t code)
```



###  printToSprite()

```c
void TFT_eSprite::printToSprite(String string)
```



###  printToSprite()

```c
void TFT_eSprite::printToSprite(char *cbuffer, uint16_t len)
```



###  printToSprite()

```c
int16_t TFT_eSprite::printToSprite(int16_t x, int16_t y, uint16_t index)
```



