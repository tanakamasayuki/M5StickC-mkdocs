# Arduino_LCD



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_arduino___l_c_d.html)

## メンバー

### Arduino_LCD()



```c
Arduino_LCD::Arduino_LCD(uint8_t CS, uint8_t RS, uint8_t SID, uint8_t SCLK, uint8_t RST)
```

!!! summary "引数"
	- uint8_t `CS` 
	- uint8_t `RS` 
	- uint8_t `SID` 
	- uint8_t `SCLK` 
	- uint8_t `RST` 



### Arduino_LCD()



```c
Arduino_LCD::Arduino_LCD(uint8_t CS, uint8_t RS, uint8_t RST)
```

!!! summary "引数"
	- uint8_t `CS` 
	- uint8_t `RS` 
	- uint8_t `RST` 



### initB()



```c
void Arduino_LCD::initB(void)
```



### initR()



```c
void Arduino_LCD::initR(uint8_t options=INITR_GREENTAB)
```

!!! summary "引数"
	- uint8_t `options` 



### setAddrWindow()



```c
void Arduino_LCD::setAddrWindow(uint8_t x0, uint8_t y0, uint8_t x1, uint8_t y1)
```

!!! summary "引数"
	- uint8_t `x0` 
	- uint8_t `y0` 
	- uint8_t `x1` 
	- uint8_t `y1` 



### pushColor()



```c
void Arduino_LCD::pushColor(uint16_t color)
```

!!! summary "引数"
	- uint16_t `color` 



### fillScreen()



```c
void Arduino_LCD::fillScreen(uint16_t color)
```

!!! summary "引数"
	- uint16_t `color` 



### drawPixel()



```c
void Arduino_LCD::drawPixel(int16_t x, int16_t y, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- uint16_t `color` 



### drawFastVLine()



```c
void Arduino_LCD::drawFastVLine(int16_t x, int16_t y, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `h` 
	- uint16_t `color` 



### drawFastHLine()



```c
void Arduino_LCD::drawFastHLine(int16_t x, int16_t y, int16_t w, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `w` 
	- uint16_t `color` 



### fillRect()



```c
void Arduino_LCD::fillRect(int16_t x, int16_t y, int16_t w, int16_t h, uint16_t color)
```

!!! summary "引数"
	- int16_t `x` 
	- int16_t `y` 
	- int16_t `w` 
	- int16_t `h` 
	- uint16_t `color` 



### setRotation()



```c
void Arduino_LCD::setRotation(uint8_t r)
```

!!! summary "引数"
	- uint8_t `r` 



### invertDisplay()



```c
void Arduino_LCD::invertDisplay(boolean i)
```

!!! summary "引数"
	- boolean `i` 



### Color565()



```c
uint16_t Arduino_LCD::Color565(uint8_t r, uint8_t g, uint8_t b)
```

!!! summary "引数"
	- uint8_t `r` 
	- uint8_t `g` 
	- uint8_t `b` 

!!! note "戻り値"
	uint16_t



