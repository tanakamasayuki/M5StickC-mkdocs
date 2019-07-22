###  cursor_x

```c
int32_t TFT_eSPI::cursor_x
```


###  cursor_y

```c
int32_t TFT_eSPI::cursor_y
```


###  padX

```c
int32_t TFT_eSPI::padX
```


###  textcolor

```c
uint32_t TFT_eSPI::textcolor
```


###  textbgcolor

```c
uint32_t TFT_eSPI::textbgcolor
```


###  bitmap_fg

```c
uint32_t TFT_eSPI::bitmap_fg
```


###  bitmap_bg

```c
uint32_t TFT_eSPI::bitmap_bg
```


###  textfont

```c
uint8_t TFT_eSPI::textfont
```


###  textsize

```c
uint8_t TFT_eSPI::textsize
```


###  textdatum

```c
uint8_t TFT_eSPI::textdatum
```


###  rotation

```c
uint8_t TFT_eSPI::rotation
```


###  _xpivot

```c
int16_t TFT_eSPI::_xpivot
```


###  _ypivot

```c
int16_t TFT_eSPI::_ypivot
```


###  decoderState

```c
uint8_t TFT_eSPI::decoderState
```


###  decoderBuffer

```c
uint16_t TFT_eSPI::decoderBuffer
```


###  TFT_eSPI()

```c
TFT_eSPI::TFT_eSPI(int16_t _W=TFT_WIDTH, int16_t _H=TFT_HEIGHT)
```



###  init()

```c
void TFT_eSPI::init(uint8_t tc=TAB_COLOUR)
```



###  begin()

```c
void TFT_eSPI::begin(uint8_t tc=TAB_COLOUR)
```



###  drawPixel()

```c
void TFT_eSPI::drawPixel(int32_t x, int32_t y, uint32_t color)
```



###  drawChar()

```c
void TFT_eSPI::drawChar(int32_t x, int32_t y, uint16_t c, uint32_t color, uint32_t bg, uint8_t size)
```



###  drawLine()

```c
void TFT_eSPI::drawLine(int32_t x0, int32_t y0, int32_t x1, int32_t y1, uint32_t color)
```



###  drawFastVLine()

```c
void TFT_eSPI::drawFastVLine(int32_t x, int32_t y, int32_t h, uint32_t color)
```



###  drawFastHLine()

```c
void TFT_eSPI::drawFastHLine(int32_t x, int32_t y, int32_t w, uint32_t color)
```



###  fillRect()

```c
void TFT_eSPI::fillRect(int32_t x, int32_t y, int32_t w, int32_t h, uint32_t color)
```



###  drawChar()

```c
int16_t TFT_eSPI::drawChar(uint16_t uniCode, int32_t x, int32_t y, uint8_t font)
```



###  drawChar()

```c
int16_t TFT_eSPI::drawChar(uint16_t uniCode, int32_t x, int32_t y)
```



###  height()

```c
int16_t TFT_eSPI::height(void)
```



###  width()

```c
int16_t TFT_eSPI::width(void)
```



###  setWindow()

```c
void TFT_eSPI::setWindow(int32_t xs, int32_t ys, int32_t xe, int32_t ye)
```



###  pushColor()

```c
void TFT_eSPI::pushColor(uint16_t color)
```



###  pushColor()

```c
void TFT_eSPI::pushColor(uint16_t color, uint32_t len)
```



###  pushColors()

```c
void TFT_eSPI::pushColors(uint16_t *data, uint32_t len, bool swap=true)
```



###  pushColors()

```c
void TFT_eSPI::pushColors(uint8_t *data, uint32_t len)
```



###  fillScreen()

```c
void TFT_eSPI::fillScreen(uint32_t color)
```



###  drawRect()

```c
void TFT_eSPI::drawRect(int32_t x, int32_t y, int32_t w, int32_t h, uint32_t color)
```



###  drawRoundRect()

```c
void TFT_eSPI::drawRoundRect(int32_t x0, int32_t y0, int32_t w, int32_t h, int32_t radius, uint32_t color)
```



###  fillRoundRect()

```c
void TFT_eSPI::fillRoundRect(int32_t x0, int32_t y0, int32_t w, int32_t h, int32_t radius, uint32_t color)
```



###  setRotation()

```c
void TFT_eSPI::setRotation(uint8_t r)
```



###  invertDisplay()

```c
void TFT_eSPI::invertDisplay(boolean i)
```



###  drawCircle()

```c
void TFT_eSPI::drawCircle(int32_t x0, int32_t y0, int32_t r, uint32_t color)
```



###  drawCircleHelper()

```c
void TFT_eSPI::drawCircleHelper(int32_t x0, int32_t y0, int32_t r, uint8_t cornername, uint32_t color)
```



###  fillCircle()

```c
void TFT_eSPI::fillCircle(int32_t x0, int32_t y0, int32_t r, uint32_t color)
```



###  fillCircleHelper()

```c
void TFT_eSPI::fillCircleHelper(int32_t x0, int32_t y0, int32_t r, uint8_t cornername, int32_t delta, uint32_t color)
```



###  drawEllipse()

```c
void TFT_eSPI::drawEllipse(int16_t x0, int16_t y0, int32_t rx, int32_t ry, uint16_t color)
```



###  fillEllipse()

```c
void TFT_eSPI::fillEllipse(int16_t x0, int16_t y0, int32_t rx, int32_t ry, uint16_t color)
```



###  drawTriangle()

```c
void TFT_eSPI::drawTriangle(int32_t x0, int32_t y0, int32_t x1, int32_t y1, int32_t x2, int32_t y2, uint32_t color)
```



###  fillTriangle()

```c
void TFT_eSPI::fillTriangle(int32_t x0, int32_t y0, int32_t x1, int32_t y1, int32_t x2, int32_t y2, uint32_t color)
```



###  drawBitmap()

```c
void TFT_eSPI::drawBitmap(int16_t x, int16_t y, const uint8_t *bitmap, int16_t w, int16_t h, uint16_t color)
```



###  drawXBitmap()

```c
void TFT_eSPI::drawXBitmap(int16_t x, int16_t y, const uint8_t *bitmap, int16_t w, int16_t h, uint16_t color)
```



###  drawXBitmap()

```c
void TFT_eSPI::drawXBitmap(int16_t x, int16_t y, const uint8_t *bitmap, int16_t w, int16_t h, uint16_t fgcolor, uint16_t bgcolor)
```



###  setBitmapColor()

```c
void TFT_eSPI::setBitmapColor(uint16_t fgcolor, uint16_t bgcolor)
```



###  setPivot()

```c
void TFT_eSPI::setPivot(int16_t x, int16_t y)
```



###  setCursor()

```c
void TFT_eSPI::setCursor(int16_t x, int16_t y)
```



###  setCursor()

```c
void TFT_eSPI::setCursor(int16_t x, int16_t y, uint8_t font)
```



###  setTextColor()

```c
void TFT_eSPI::setTextColor(uint16_t color)
```



###  setTextColor()

```c
void TFT_eSPI::setTextColor(uint16_t fgcolor, uint16_t bgcolor)
```



###  setTextSize()

```c
void TFT_eSPI::setTextSize(uint8_t size)
```



###  setTextWrap()

```c
void TFT_eSPI::setTextWrap(boolean wrapX, boolean wrapY=false)
```



###  setTextDatum()

```c
void TFT_eSPI::setTextDatum(uint8_t datum)
```



###  setTextPadding()

```c
void TFT_eSPI::setTextPadding(uint16_t x_width)
```



###  setFreeFont()

```c
void TFT_eSPI::setFreeFont(const GFXfont *f=NULL)
```



###  setTextFont()

```c
void TFT_eSPI::setTextFont(uint8_t font)
```



###  spiwrite()

```c
void TFT_eSPI::spiwrite(uint8_t)
```



###  writecommand()

```c
void TFT_eSPI::writecommand(uint8_t c)
```



###  writedata()

```c
void TFT_eSPI::writedata(uint8_t d)
```



###  commandList()

```c
void TFT_eSPI::commandList(const uint8_t *addr)
```



###  readcommand8()

```c
uint8_t TFT_eSPI::readcommand8(uint8_t cmd_function, uint8_t index=0)
```



###  readcommand16()

```c
uint16_t TFT_eSPI::readcommand16(uint8_t cmd_function, uint8_t index=0)
```



###  readcommand32()

```c
uint32_t TFT_eSPI::readcommand32(uint8_t cmd_function, uint8_t index=0)
```



###  readPixel()

```c
uint16_t TFT_eSPI::readPixel(int32_t x0, int32_t y0)
```



###  readRect()

```c
void TFT_eSPI::readRect(int32_t x0, int32_t y0, int32_t w, int32_t h, uint16_t *data)
```



###  pushRect()

```c
void TFT_eSPI::pushRect(int32_t x0, int32_t y0, int32_t w, int32_t h, uint16_t *data)
```



###  pushImage()

```c
void TFT_eSPI::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, uint16_t *data)
```



###  pushImage()

```c
void TFT_eSPI::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, uint16_t *data, uint16_t transparent)
```



###  pushImage()

```c
void TFT_eSPI::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, const uint16_t *data, uint16_t transparent)
```



###  pushImage()

```c
void TFT_eSPI::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, const uint16_t *data)
```



###  pushImage()

```c
void TFT_eSPI::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, uint8_t *data, bool bpp8=true)
```



###  pushImage()

```c
void TFT_eSPI::pushImage(int32_t x0, int32_t y0, int32_t w, int32_t h, uint8_t *data, uint8_t transparent, bool bpp8=true)
```



###  setSwapBytes()

```c
void TFT_eSPI::setSwapBytes(bool swap)
```



###  getSwapBytes()

```c
bool TFT_eSPI::getSwapBytes(void)
```



###  readRectRGB()

```c
void TFT_eSPI::readRectRGB(int32_t x0, int32_t y0, int32_t w, int32_t h, uint8_t *data)
```



###  getRotation()

```c
uint8_t TFT_eSPI::getRotation(void)
```



###  getTextDatum()

```c
uint8_t TFT_eSPI::getTextDatum(void)
```



###  color16to8()

```c
uint8_t TFT_eSPI::color16to8(uint16_t color565)
```



###  getCursorX()

```c
int16_t TFT_eSPI::getCursorX(void)
```



###  getCursorY()

```c
int16_t TFT_eSPI::getCursorY(void)
```



###  getPivotX()

```c
int16_t TFT_eSPI::getPivotX(void)
```



###  getPivotY()

```c
int16_t TFT_eSPI::getPivotY(void)
```



###  fontsLoaded()

```c
uint16_t TFT_eSPI::fontsLoaded(void)
```



###  color565()

```c
uint16_t TFT_eSPI::color565(uint8_t red, uint8_t green, uint8_t blue)
```



###  color8to16()

```c
uint16_t TFT_eSPI::color8to16(uint8_t color332)
```



###  drawNumber()

```c
int16_t TFT_eSPI::drawNumber(long long_num, int32_t poX, int32_t poY, uint8_t font)
```



###  drawNumber()

```c
int16_t TFT_eSPI::drawNumber(long long_num, int32_t poX, int32_t poY)
```



###  drawFloat()

```c
int16_t TFT_eSPI::drawFloat(float floatNumber, uint8_t decimal, int32_t poX, int32_t poY, uint8_t font)
```



###  drawFloat()

```c
int16_t TFT_eSPI::drawFloat(float floatNumber, uint8_t decimal, int32_t poX, int32_t poY)
```



###  drawString()

```c
int16_t TFT_eSPI::drawString(const char *string, int32_t poX, int32_t poY, uint8_t font)
```



###  drawString()

```c
int16_t TFT_eSPI::drawString(const char *string, int32_t poX, int32_t poY)
```



###  drawCentreString()

```c
int16_t TFT_eSPI::drawCentreString(const char *string, int32_t dX, int32_t poY, uint8_t font)
```



###  drawRightString()

```c
int16_t TFT_eSPI::drawRightString(const char *string, int32_t dX, int32_t poY, uint8_t font)
```



###  drawString()

```c
int16_t TFT_eSPI::drawString(const String &string, int32_t poX, int32_t poY, uint8_t font)
```



###  drawString()

```c
int16_t TFT_eSPI::drawString(const String &string, int32_t poX, int32_t poY)
```



###  drawCentreString()

```c
int16_t TFT_eSPI::drawCentreString(const String &string, int32_t dX, int32_t poY, uint8_t font)
```



###  drawRightString()

```c
int16_t TFT_eSPI::drawRightString(const String &string, int32_t dX, int32_t poY, uint8_t font)
```



###  textWidth()

```c
int16_t TFT_eSPI::textWidth(const char *string, uint8_t font)
```



###  textWidth()

```c
int16_t TFT_eSPI::textWidth(const char *string)
```



###  textWidth()

```c
int16_t TFT_eSPI::textWidth(const String &string, uint8_t font)
```



###  textWidth()

```c
int16_t TFT_eSPI::textWidth(const String &string)
```



###  fontHeight()

```c
int16_t TFT_eSPI::fontHeight(int16_t font)
```



###  fontHeight()

```c
int16_t TFT_eSPI::fontHeight(void)
```



###  setAddrWindow()

```c
void TFT_eSPI::setAddrWindow(int32_t xs, int32_t ys, int32_t w, int32_t h)
```



###  startWrite()

```c
void TFT_eSPI::startWrite(void)
```



###  writeColor()

```c
void TFT_eSPI::writeColor(uint16_t color, uint32_t len)
```



###  endWrite()

```c
void TFT_eSPI::endWrite(void)
```



###  decodeUTF8()

```c
uint16_t TFT_eSPI::decodeUTF8(uint8_t *buf, uint16_t *index, uint16_t remaining)
```



###  decodeUTF8()

```c
uint16_t TFT_eSPI::decodeUTF8(uint8_t c)
```



###  write()

```c
size_t TFT_eSPI::write(uint8_t)
```



###  setAttribute()

```c
void TFT_eSPI::setAttribute(uint8_t id=0, uint8_t a=0)
```



###  getAttribute()

```c
uint8_t TFT_eSPI::getAttribute(uint8_t id=0)
```



###  getSetup()

```c
void TFT_eSPI::getSetup(setup_t &tft_settings)
```



