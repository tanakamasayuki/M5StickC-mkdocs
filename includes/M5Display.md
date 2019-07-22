###  M5Display()

```c
M5Display::M5Display()
```



###  begin()

```c
void M5Display::begin()
```



###  sleep()

```c
void M5Display::sleep()
```



###  setBrightness()

```c
void M5Display::setBrightness(uint8_t brightness)
```



###  drawBitmap()

```c
void M5Display::drawBitmap(int16_t x0, int16_t y0, int16_t w, int16_t h, const uint16_t *data)
```



###  drawBitmap()

```c
void M5Display::drawBitmap(int16_t x0, int16_t y0, int16_t w, int16_t h, const uint8_t *data)
```



###  drawBitmap()

```c
void M5Display::drawBitmap(int16_t x0, int16_t y0, int16_t w, int16_t h, uint16_t *data)
```



###  drawBitmap()

```c
void M5Display::drawBitmap(int16_t x0, int16_t y0, int16_t w, int16_t h, uint8_t *data)
```



###  drawBitmap()

```c
void M5Display::drawBitmap(int16_t x0, int16_t y0, int16_t w, int16_t h, const uint16_t *data, uint16_t transparent)
```



###  loadHzk16()

```c
void M5Display::loadHzk16(Hzk16Types hzkTypes=InternalHzk16, const char *HZK16Path="/HZK16", const char *ASC16Path="/ASC16")
```



###  setTextWrap()

```c
void M5Display::setTextWrap(boolean wrap)
```



###  writeHzk()

```c
void M5Display::writeHzk(char *c)
```



###  highlight()

```c
void M5Display::highlight(bool isHighlight)
```



###  setHighlightColor()

```c
void M5Display::setHighlightColor(uint16_t color)
```



###  qrcode()

```c
void M5Display::qrcode(const char *string, uint16_t x=5, uint16_t y=45, uint8_t width=70, uint8_t version=7)
```



###  qrcode()

```c
void M5Display::qrcode(const String &string, uint16_t x=5, uint16_t y=45, uint8_t width=70, uint8_t version=7)
```



