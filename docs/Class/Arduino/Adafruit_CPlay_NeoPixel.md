# Adafruit_CPlay_NeoPixel

Class that stores state and functions for neopixels on CircuitPlayground boards 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_adafruit___c_play___neo_pixel.html)

## メンバー

### Adafruit_CPlay_NeoPixel()
Constructor when length, pin and type are known at compile-time


```c
Adafruit_CPlay_NeoPixel::Adafruit_CPlay_NeoPixel(uint16_t n, uint8_t p=17, neoPixelType t=NEO_GRB+NEO_KHZ800)
```

!!! summary "引数"
	- uint16_t `n` number of pixels 
	- uint8_t `p` pin the pixels are attached to 
	- neoPixelType `t` the type of neopixel. can be NEO_KHZ800 or NEO_KHZ400 



### Adafruit_CPlay_NeoPixel()
via Michael Vogt/neophob: empty constructor is used when strand length isn't known at compile-time; situations where program config might be read from internal flash memory or an SD card, or arrive via serial command. If using this constructor, MUST follow up with , , etc. to establish the strand type, length and pin number!


```c
Adafruit_CPlay_NeoPixel::Adafruit_CPlay_NeoPixel(void)
```



### ~Adafruit_CPlay_NeoPixel()



```c
Adafruit_CPlay_NeoPixel::~Adafruit_CPlay_NeoPixel()
```



### begin()
initialize necessary hardware to drive the pixels.


```c
void Adafruit_CPlay_NeoPixel::begin(void)
```



### show()
Write data to the neopixels



```c
void Adafruit_CPlay_NeoPixel::show(void)
```



### setPin()
Set the output pin number


```c
void Adafruit_CPlay_NeoPixel::setPin(uint8_t p)
```

!!! summary "引数"
	- uint8_t `p` the pin number 



### setPixelColor()
Set pixel color from separate R,G,B components:


```c
void Adafruit_CPlay_NeoPixel::setPixelColor(uint16_t n, uint8_t r, uint8_t g, uint8_t b)
```

!!! summary "引数"
	- uint16_t `n` the pixel number to set 
	- uint8_t `r` the red component 
	- uint8_t `g` the green component 
	- uint8_t `b` the blue component 



### setPixelColor()
Set pixel color from separate R,G,B,W components:


```c
void Adafruit_CPlay_NeoPixel::setPixelColor(uint16_t n, uint8_t r, uint8_t g, uint8_t b, uint8_t w)
```

!!! summary "引数"
	- uint16_t `n` the pixel number to set 
	- uint8_t `r` the red component 
	- uint8_t `g` the green component 
	- uint8_t `b` the blue component 
	- uint8_t `w` the white component 



### setPixelColor()
Set pixel color from 'packed' 32-bit RGB color:


```c
void Adafruit_CPlay_NeoPixel::setPixelColor(uint16_t n, uint32_t c)
```

!!! summary "引数"
	- uint16_t `n` the pixel number to set 
	- uint32_t `c` the packed 32-bit color data 



### setBrightness()
Adjust output brightness; 0=darkest (off), 255=brightest.


```c
void Adafruit_CPlay_NeoPixel::setBrightness(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 



### clear()
set all neopixel data to 'off' in internal memory.



```c
void Adafruit_CPlay_NeoPixel::clear()
```



### updateLength()
Set the number of pixels in the strip


```c
void Adafruit_CPlay_NeoPixel::updateLength(uint16_t n)
```

!!! summary "引数"
	- uint16_t `n` the number of pixels in the strip 



### updateType()
set the type of neopixel we are using


```c
void Adafruit_CPlay_NeoPixel::updateType(neoPixelType t)
```

!!! summary "引数"
	- neoPixelType `t` the type of neopixel. Can be NEO_KHZ800 or NEO_KHZ400 



### getPixels()
Returns pointer to pixels[] array. Pixel data is stored in device- native format and is not translated here. Application will need to be aware of specific pixel data format and handle colors appropriately.



```c
uint8_t * Adafruit_CPlay_NeoPixel::getPixels(void) const
```

!!! note "戻り値"
	uint8_t * pointer to the pixel array. 



### getBrightness()
get the global brightness value



```c
uint8_t Adafruit_CPlay_NeoPixel::getBrightness(void) const
```

!!! note "戻り値"
	uint8_t the global brightness 



### sine8()
Get a sinusoidal value from a sine table


```c
uint8_t Adafruit_CPlay_NeoPixel::sine8(uint8_t) const
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	uint8_t An 8-bit sinusoidal value back 



### gamma8()
Get a gamma-corrected value from a gamma table


```c
uint8_t Adafruit_CPlay_NeoPixel::gamma8(uint8_t) const
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	uint8_t An 8-bit gamma-corrected value back 



### numPixels()
get the number of pixels in the strip



```c
uint16_t Adafruit_CPlay_NeoPixel::numPixels(void) const
```

!!! note "戻り値"
	uint16_t the number of pixels 



### Color()
Convert separate R,G,B,W into packed 32-bit WRGB color.


```c
uint32_t Adafruit_CPlay_NeoPixel::Color(uint8_t r, uint8_t g, uint8_t b, uint8_t w)
```

!!! summary "引数"
	- uint8_t `r` the red component 
	- uint8_t `g` the green component 
	- uint8_t `b` the blue component 
	- uint8_t `w` the white component 

!!! note "戻り値"
	uint32_t the converted 32-bit color



### getPixelColor()
Query color from previously-set pixel (returns packed 32-bit RGB value)


```c
uint32_t Adafruit_CPlay_NeoPixel::getPixelColor(uint16_t n) const
```

!!! summary "引数"
	- uint16_t `n` the number of the pixel to check 

!!! note "戻り値"
	uint32_t the 32-bit color of the pixel



### canShow()
check if enough time has elapsed and the pixels are ready to refresh.



```c
bool Adafruit_CPlay_NeoPixel::canShow(void)
```

!!! note "戻り値"
	bool true if ready to show, false otherwise. 



### Color()
Convert separate R,G,B into packed 32-bit RGB color.


```c
uint32_t Adafruit_CPlay_NeoPixel::Color(uint8_t r, uint8_t g, uint8_t b)
```

!!! summary "引数"
	- uint8_t `r` the red component 
	- uint8_t `g` the green component 
	- uint8_t `b` the blue component 

!!! note "戻り値"
	uint32_t the converted 32-bit color



