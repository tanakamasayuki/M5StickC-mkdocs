# Adafruit_ST7735



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_adafruit___s_t7735.html)

## メンバー

### Adafruit_ST7735()



```c
Adafruit_ST7735::Adafruit_ST7735(uint8_t CS, uint8_t RS, uint8_t SID, uint8_t SCLK, uint8_t RST)
```

!!! summary "引数"
	- uint8_t `CS` 
	- uint8_t `RS` 
	- uint8_t `SID` 
	- uint8_t `SCLK` 
	- uint8_t `RST` 



### Adafruit_ST7735()



```c
Adafruit_ST7735::Adafruit_ST7735(uint8_t CS, uint8_t RS, uint8_t RST)
```

!!! summary "引数"
	- uint8_t `CS` 
	- uint8_t `RS` 
	- uint8_t `RST` 



### initB()



```c
void Adafruit_ST7735::initB(void)
```



### initG()



```c
void Adafruit_ST7735::initG(void)
```



### initR()



```c
void Adafruit_ST7735::initR(uint8_t options=INITR_GREENTAB)
```

!!! summary "引数"
	- uint8_t `options` 



### setAddrWindow()



```c
void Adafruit_ST7735::setAddrWindow(uint8_t x0, uint8_t y0, uint8_t x1, uint8_t y1)
```

!!! summary "引数"
	- uint8_t `x0` 
	- uint8_t `y0` 
	- uint8_t `x1` 
	- uint8_t `y1` 



### pushColor()



```c
void Adafruit_ST7735::pushColor(uint16_t color)
```

!!! summary "引数"
	- uint16_t `color` 



### fillScreen()



```c
void Adafruit_ST7735::fillScreen(uint16_t color)
```

!!! summary "引数"
	- uint16_t `color` 



### drawPixel()



```c
void Adafruit_ST7735::drawPixel(int16_t x, int16_t y, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- uint16_t `color` 



### drawFastVLine()



```c
void Adafruit_ST7735::drawFastVLine(int16_t x, int16_t y, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `h` 
	- uint16_t `color` 



### drawFastHLine()



```c
void Adafruit_ST7735::drawFastHLine(int16_t x, int16_t y, int16_t w, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `w` 
	- uint16_t `color` 



### fillRect()



```c
void Adafruit_ST7735::fillRect(int16_t x, int16_t y, int16_t w, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `w` 
	- int16_t `h` 
	- uint16_t `color` 



### setRotation()



```c
void Adafruit_ST7735::setRotation(uint8_t r)
```

!!! summary "引数"
	- uint8_t `r` 



### invertDisplay()



```c
void Adafruit_ST7735::invertDisplay(boolean i)
```

!!! summary "引数"
	- boolean `i` 



### Color565()



```c
uint16_t Adafruit_ST7735::Color565(uint8_t r, uint8_t g, uint8_t b)
```

!!! summary "引数"
	- uint8_t `r` 
	- uint8_t `g` 
	- uint8_t `b` 

!!! note "戻り値"
	uint16_t



