# Adafruit_GFX



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_adafruit___g_f_x.html)

## メンバー

### Adafruit_GFX()



```c
Adafruit_GFX::Adafruit_GFX(int16_t w, int16_t h)
```

!!! summary "引数"
	- int16_t `w` 
	- int16_t `h` 



### drawPixel()



```c
virtual void Adafruit_GFX::drawPixel(int16_t x, int16_t y, uint16_t color)=0
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- uint16_t `color` 



### drawLine()



```c
void Adafruit_GFX::drawLine(int16_t x0, int16_t y0, int16_t x1, int16_t y1, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `x1` 
	- int16_t `y1` 
	- uint16_t `color` 



### drawFastVLine()



```c
void Adafruit_GFX::drawFastVLine(int16_t x, int16_t y, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `h` 
	- uint16_t `color` 



### drawFastHLine()



```c
void Adafruit_GFX::drawFastHLine(int16_t x, int16_t y, int16_t w, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `w` 
	- uint16_t `color` 



### drawRect()



```c
void Adafruit_GFX::drawRect(int16_t x, int16_t y, int16_t w, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `w` 
	- int16_t `h` 
	- uint16_t `color` 



### fillRect()



```c
void Adafruit_GFX::fillRect(int16_t x, int16_t y, int16_t w, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `w` 
	- int16_t `h` 
	- uint16_t `color` 



### fillScreen()



```c
void Adafruit_GFX::fillScreen(uint16_t color)
```

!!! summary "引数"
	- uint16_t `color` 



### invertDisplay()



```c
void Adafruit_GFX::invertDisplay(boolean i)
```

!!! summary "引数"
	- boolean `i` 



### drawCircle()



```c
void Adafruit_GFX::drawCircle(int16_t x0, int16_t y0, int16_t r, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `r` 
	- uint16_t `color` 



### drawCircleHelper()



```c
void Adafruit_GFX::drawCircleHelper(int16_t x0, int16_t y0, int16_t r, uint8_t cornername, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `r` 
	- uint8_t `cornername` 
	- uint16_t `color` 



### fillCircle()



```c
void Adafruit_GFX::fillCircle(int16_t x0, int16_t y0, int16_t r, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `r` 
	- uint16_t `color` 



### fillCircleHelper()



```c
void Adafruit_GFX::fillCircleHelper(int16_t x0, int16_t y0, int16_t r, uint8_t cornername, int16_t delta, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `r` 
	- uint8_t `cornername` 
	- int16_t `delta` 
	- uint16_t `color` 



### drawTriangle()



```c
void Adafruit_GFX::drawTriangle(int16_t x0, int16_t y0, int16_t x1, int16_t y1, int16_t x2, int16_t y2, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `x1` 
	- int16_t `y1` 
	- int16_t `x2` 
	- int16_t `y2` 
	- uint16_t `color` 



### fillTriangle()



```c
void Adafruit_GFX::fillTriangle(int16_t x0, int16_t y0, int16_t x1, int16_t y1, int16_t x2, int16_t y2, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `x1` 
	- int16_t `y1` 
	- int16_t `x2` 
	- int16_t `y2` 
	- uint16_t `color` 



### drawRoundRect()



```c
void Adafruit_GFX::drawRoundRect(int16_t x0, int16_t y0, int16_t w, int16_t h, int16_t radius, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `w` 
	- int16_t `h` 
	- int16_t `radius` 
	- uint16_t `color` 



### fillRoundRect()



```c
void Adafruit_GFX::fillRoundRect(int16_t x0, int16_t y0, int16_t w, int16_t h, int16_t radius, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `w` 
	- int16_t `h` 
	- int16_t `radius` 
	- uint16_t `color` 



### drawBitmap()



```c
void Adafruit_GFX::drawBitmap(int16_t x, int16_t y, const uint8_t *bitmap, int16_t w, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- constuint8_t * `bitmap` 
	- int16_t `w` 
	- int16_t `h` 
	- uint16_t `color` 



### drawChar()



```c
void Adafruit_GFX::drawChar(int16_t x, int16_t y, unsigned char c, uint16_t color, uint16_t bg, uint8_t size)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- unsigned char `c` 
	- uint16_t `color` 
	- uint16_t `bg` 
	- uint8_t `size` 



### setCursor()



```c
void Adafruit_GFX::setCursor(int16_t x, int16_t y)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 



### setTextColor()



```c
void Adafruit_GFX::setTextColor(uint16_t c)
```

!!! summary "引数"
	- uint16_t `c` 



### setTextColor()



```c
void Adafruit_GFX::setTextColor(uint16_t c, uint16_t bg)
```

!!! summary "引数"
	- uint16_t `c` 
	- uint16_t `bg` 



### setTextSize()



```c
void Adafruit_GFX::setTextSize(uint8_t s)
```

!!! summary "引数"
	- uint8_t `s` 



### setTextWrap()



```c
void Adafruit_GFX::setTextWrap(boolean w)
```

!!! summary "引数"
	- boolean `w` 



### setRotation()



```c
void Adafruit_GFX::setRotation(uint8_t r)
```

!!! summary "引数"
	- uint8_t `r` 



### write()



```c
void Adafruit_GFX::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 



### height()



```c
int16_t Adafruit_GFX::height(void)
```

!!! note "戻り値"
	int16_t



### width()



```c
int16_t Adafruit_GFX::width(void)
```

!!! note "戻り値"
	int16_t



### getRotation()



```c
uint8_t Adafruit_GFX::getRotation(void)
```

!!! note "戻り値"
	uint8_t



### newColor()


transforms a color in 16-bit form given the RGB components. The default implementation makes a 5-bit red, a 6-bit green and a 5-bit blue (MSB to LSB). Devices that use different scheme should override this. 
```c
uint16_t Adafruit_GFX::newColor(uint8_t red, uint8_t green, uint8_t blue)
```

!!! summary "引数"
	- uint8_t `red` 
	- uint8_t `green` 
	- uint8_t `blue` 

!!! note "戻り値"
	uint16_t



### background()



```c
void Adafruit_GFX::background(uint8_t red, uint8_t green, uint8_t blue)
```

!!! summary "引数"
	- uint8_t `red` 
	- uint8_t `green` 
	- uint8_t `blue` 



### background()



```c
void Adafruit_GFX::background(color c)
```

!!! summary "引数"
	- color `c` 



### fill()



```c
void Adafruit_GFX::fill(uint8_t red, uint8_t green, uint8_t blue)
```

!!! summary "引数"
	- uint8_t `red` 
	- uint8_t `green` 
	- uint8_t `blue` 



### fill()



```c
void Adafruit_GFX::fill(color c)
```

!!! summary "引数"
	- color `c` 



### noFill()



```c
void Adafruit_GFX::noFill()
```



### stroke()



```c
void Adafruit_GFX::stroke(uint8_t red, uint8_t green, uint8_t blue)
```

!!! summary "引数"
	- uint8_t `red` 
	- uint8_t `green` 
	- uint8_t `blue` 



### stroke()



```c
void Adafruit_GFX::stroke(color c)
```

!!! summary "引数"
	- color `c` 



### noStroke()



```c
void Adafruit_GFX::noStroke()
```



### text()



```c
void Adafruit_GFX::text(const char *text, int16_t x, int16_t y)
```

!!! summary "引数"
	- constchar * `text` 
	- int16_t `x` 
	- int16_t `y` 



### text()



```c
void Adafruit_GFX::text(int value, uint8_t posX, uint8_t posY)
```

!!! summary "引数"
	- int `value` 
	- uint8_t `posX` 
	- uint8_t `posY` 



### text()



```c
void Adafruit_GFX::text(long value, uint8_t posX, uint8_t posY)
```

!!! summary "引数"
	- long `value` 
	- uint8_t `posX` 
	- uint8_t `posY` 



### text()



```c
void Adafruit_GFX::text(char value, uint8_t posX, uint8_t posY)
```

!!! summary "引数"
	- char `value` 
	- uint8_t `posX` 
	- uint8_t `posY` 



### textWrap()



```c
void Adafruit_GFX::textWrap(const char *text, int16_t x, int16_t y)
```

!!! summary "引数"
	- constchar * `text` 
	- int16_t `x` 
	- int16_t `y` 



### textSize()



```c
void Adafruit_GFX::textSize(uint8_t size)
```

!!! summary "引数"
	- uint8_t `size` 



### circle()



```c
void Adafruit_GFX::circle(int16_t x, int16_t y, int16_t r)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `r` 



### point()



```c
void Adafruit_GFX::point(int16_t x, int16_t y)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 



### line()



```c
void Adafruit_GFX::line(int16_t x1, int16_t y1, int16_t x2, int16_t y2)
```

!!! summary "引数"
	- int16_t `x1` 
	- int16_t `y1` 
	- int16_t `x2` 
	- int16_t `y2` 



### quad()



```c
void Adafruit_GFX::quad(int16_t x1, int16_t y1, int16_t x2, int16_t y2, int16_t x3, int16_t y3, int16_t x4, int16_t y4)
```

!!! summary "引数"
	- int16_t `x1` 
	- int16_t `y1` 
	- int16_t `x2` 
	- int16_t `y2` 
	- int16_t `x3` 
	- int16_t `y3` 
	- int16_t `x4` 
	- int16_t `y4` 



### rect()



```c
void Adafruit_GFX::rect(int16_t x, int16_t y, int16_t width, int16_t height)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `width` 
	- int16_t `height` 



### rect()



```c
void Adafruit_GFX::rect(int16_t x, int16_t y, int16_t width, int16_t height, int16_t radius)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `width` 
	- int16_t `height` 
	- int16_t `radius` 



### triangle()



```c
void Adafruit_GFX::triangle(int16_t x1, int16_t y1, int16_t x2, int16_t y2, int16_t x3, int16_t y3)
```

!!! summary "引数"
	- int16_t `x1` 
	- int16_t `y1` 
	- int16_t `x2` 
	- int16_t `y2` 
	- int16_t `x3` 
	- int16_t `y3` 



### Adafruit_GFX()



```c
Adafruit_GFX::Adafruit_GFX(int16_t w, int16_t h)
```

!!! summary "引数"
	- int16_t `w` 
	- int16_t `h` 



### drawPixel()



```c
virtual void Adafruit_GFX::drawPixel(int16_t x, int16_t y, uint16_t color)=0
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- uint16_t `color` 



### drawLine()



```c
virtual void Adafruit_GFX::drawLine(int16_t x0, int16_t y0, int16_t x1, int16_t y1, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `x1` 
	- int16_t `y1` 
	- uint16_t `color` 



### drawFastVLine()



```c
virtual void Adafruit_GFX::drawFastVLine(int16_t x, int16_t y, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `h` 
	- uint16_t `color` 



### drawFastHLine()



```c
virtual void Adafruit_GFX::drawFastHLine(int16_t x, int16_t y, int16_t w, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `w` 
	- uint16_t `color` 



### drawRect()



```c
virtual void Adafruit_GFX::drawRect(int16_t x, int16_t y, int16_t w, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `w` 
	- int16_t `h` 
	- uint16_t `color` 



### fillRect()



```c
virtual void Adafruit_GFX::fillRect(int16_t x, int16_t y, int16_t w, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `w` 
	- int16_t `h` 
	- uint16_t `color` 



### fillScreen()



```c
virtual void Adafruit_GFX::fillScreen(uint16_t color)
```

!!! summary "引数"
	- uint16_t `color` 



### invertDisplay()



```c
virtual void Adafruit_GFX::invertDisplay(boolean i)
```

!!! summary "引数"
	- boolean `i` 



### drawCircle()



```c
void Adafruit_GFX::drawCircle(int16_t x0, int16_t y0, int16_t r, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `r` 
	- uint16_t `color` 



### drawCircleHelper()



```c
void Adafruit_GFX::drawCircleHelper(int16_t x0, int16_t y0, int16_t r, uint8_t cornername, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `r` 
	- uint8_t `cornername` 
	- uint16_t `color` 



### fillCircle()



```c
void Adafruit_GFX::fillCircle(int16_t x0, int16_t y0, int16_t r, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `r` 
	- uint16_t `color` 



### fillCircleHelper()



```c
void Adafruit_GFX::fillCircleHelper(int16_t x0, int16_t y0, int16_t r, uint8_t cornername, int16_t delta, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `r` 
	- uint8_t `cornername` 
	- int16_t `delta` 
	- uint16_t `color` 



### drawTriangle()



```c
void Adafruit_GFX::drawTriangle(int16_t x0, int16_t y0, int16_t x1, int16_t y1, int16_t x2, int16_t y2, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `x1` 
	- int16_t `y1` 
	- int16_t `x2` 
	- int16_t `y2` 
	- uint16_t `color` 



### fillTriangle()



```c
void Adafruit_GFX::fillTriangle(int16_t x0, int16_t y0, int16_t x1, int16_t y1, int16_t x2, int16_t y2, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `x1` 
	- int16_t `y1` 
	- int16_t `x2` 
	- int16_t `y2` 
	- uint16_t `color` 



### drawRoundRect()



```c
void Adafruit_GFX::drawRoundRect(int16_t x0, int16_t y0, int16_t w, int16_t h, int16_t radius, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `w` 
	- int16_t `h` 
	- int16_t `radius` 
	- uint16_t `color` 



### fillRoundRect()



```c
void Adafruit_GFX::fillRoundRect(int16_t x0, int16_t y0, int16_t w, int16_t h, int16_t radius, uint16_t color)
```

!!! summary "引数"
	- int16_t `x0` 
	- int16_t `y0` 
	- int16_t `w` 
	- int16_t `h` 
	- int16_t `radius` 
	- uint16_t `color` 



### drawBitmap()



```c
void Adafruit_GFX::drawBitmap(int16_t x, int16_t y, const uint8_t *bitmap, int16_t w, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- constuint8_t * `bitmap` 
	- int16_t `w` 
	- int16_t `h` 
	- uint16_t `color` 



### drawChar()



```c
void Adafruit_GFX::drawChar(int16_t x, int16_t y, unsigned char c, uint16_t color, uint16_t bg, uint8_t size)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- unsigned char `c` 
	- uint16_t `color` 
	- uint16_t `bg` 
	- uint8_t `size` 



### setCursor()



```c
void Adafruit_GFX::setCursor(int16_t x, int16_t y)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 



### setTextColor()



```c
void Adafruit_GFX::setTextColor(uint16_t c)
```

!!! summary "引数"
	- uint16_t `c` 



### setTextColor()



```c
void Adafruit_GFX::setTextColor(uint16_t c, uint16_t bg)
```

!!! summary "引数"
	- uint16_t `c` 
	- uint16_t `bg` 



### setTextSize()



```c
void Adafruit_GFX::setTextSize(uint8_t s)
```

!!! summary "引数"
	- uint8_t `s` 



### setTextWrap()



```c
void Adafruit_GFX::setTextWrap(boolean w)
```

!!! summary "引数"
	- boolean `w` 



### setRotation()



```c
void Adafruit_GFX::setRotation(uint8_t r)
```

!!! summary "引数"
	- uint8_t `r` 



### write()



```c
virtual void Adafruit_GFX::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 



### height()



```c
int16_t Adafruit_GFX::height(void)
```

!!! note "戻り値"
	int16_t



### width()



```c
int16_t Adafruit_GFX::width(void)
```

!!! note "戻り値"
	int16_t



### getRotation()



```c
uint8_t Adafruit_GFX::getRotation(void)
```

!!! note "戻り値"
	uint8_t



### newColor()


transforms a color in 16-bit form given the RGB components. The default implementation makes a 5-bit red, a 6-bit green and a 5-bit blue (MSB to LSB). Devices that use different scheme should override this. 
```c
virtual uint16_t Adafruit_GFX::newColor(uint8_t red, uint8_t green, uint8_t blue)
```

!!! summary "引数"
	- uint8_t `red` 
	- uint8_t `green` 
	- uint8_t `blue` 

!!! note "戻り値"
	uint16_t



### background()



```c
void Adafruit_GFX::background(uint8_t red, uint8_t green, uint8_t blue)
```

!!! summary "引数"
	- uint8_t `red` 
	- uint8_t `green` 
	- uint8_t `blue` 



### background()



```c
void Adafruit_GFX::background(color c)
```

!!! summary "引数"
	- color `c` 



### fill()



```c
void Adafruit_GFX::fill(uint8_t red, uint8_t green, uint8_t blue)
```

!!! summary "引数"
	- uint8_t `red` 
	- uint8_t `green` 
	- uint8_t `blue` 



### fill()



```c
void Adafruit_GFX::fill(color c)
```

!!! summary "引数"
	- color `c` 



### noFill()



```c
void Adafruit_GFX::noFill()
```



### stroke()



```c
void Adafruit_GFX::stroke(uint8_t red, uint8_t green, uint8_t blue)
```

!!! summary "引数"
	- uint8_t `red` 
	- uint8_t `green` 
	- uint8_t `blue` 



### stroke()



```c
void Adafruit_GFX::stroke(color c)
```

!!! summary "引数"
	- color `c` 



### noStroke()



```c
void Adafruit_GFX::noStroke()
```



### text()



```c
void Adafruit_GFX::text(const char *text, int16_t x, int16_t y)
```

!!! summary "引数"
	- constchar * `text` 
	- int16_t `x` 
	- int16_t `y` 



### textWrap()



```c
void Adafruit_GFX::textWrap(const char *text, int16_t x, int16_t y)
```

!!! summary "引数"
	- constchar * `text` 
	- int16_t `x` 
	- int16_t `y` 



### textSize()



```c
void Adafruit_GFX::textSize(uint8_t size)
```

!!! summary "引数"
	- uint8_t `size` 



### circle()



```c
void Adafruit_GFX::circle(int16_t x, int16_t y, int16_t r)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `r` 



### point()



```c
void Adafruit_GFX::point(int16_t x, int16_t y)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 



### line()



```c
void Adafruit_GFX::line(int16_t x1, int16_t y1, int16_t x2, int16_t y2)
```

!!! summary "引数"
	- int16_t `x1` 
	- int16_t `y1` 
	- int16_t `x2` 
	- int16_t `y2` 



### quad()



```c
void Adafruit_GFX::quad(int16_t x1, int16_t y1, int16_t x2, int16_t y2, int16_t x3, int16_t y3, int16_t x4, int16_t y4)
```

!!! summary "引数"
	- int16_t `x1` 
	- int16_t `y1` 
	- int16_t `x2` 
	- int16_t `y2` 
	- int16_t `x3` 
	- int16_t `y3` 
	- int16_t `x4` 
	- int16_t `y4` 



### rect()



```c
void Adafruit_GFX::rect(int16_t x, int16_t y, int16_t width, int16_t height)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `width` 
	- int16_t `height` 



### rect()



```c
void Adafruit_GFX::rect(int16_t x, int16_t y, int16_t width, int16_t height, int16_t radius)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `width` 
	- int16_t `height` 
	- int16_t `radius` 



### triangle()



```c
void Adafruit_GFX::triangle(int16_t x1, int16_t y1, int16_t x2, int16_t y2, int16_t x3, int16_t y3)
```

!!! summary "引数"
	- int16_t `x1` 
	- int16_t `y1` 
	- int16_t `x2` 
	- int16_t `y2` 
	- int16_t `x3` 
	- int16_t `y3` 



