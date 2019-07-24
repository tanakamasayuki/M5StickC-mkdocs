# Adafruit_CircuitPlayground

Class that stores state and functions for interacting with CircuitPlayground hardware 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_adafruit___circuit_playground.html)

## メンバー

### the neopixel strip object strip

```c
Adafruit_CPlay_NeoPixel Adafruit_CircuitPlayground::strip
```


### the accelerometer object lis

```c
Adafruit_CPlay_LIS3DH Adafruit_CircuitPlayground::lis
```


### the microphone object mic

```c
Adafruit_CPlay_Mic Adafruit_CircuitPlayground::mic
```


### the speaker object speaker

```c
Adafruit_CPlay_Speaker Adafruit_CircuitPlayground::speaker
```


### the array of capacitive touch sensors cap

```c
Adafruit_CPlay_FreeTouch Adafruit_CircuitPlayground::cap[7]
```


### the IR receiver object irReceiver

```c
IRrecvPCI Adafruit_CircuitPlayground::irReceiver
```


### the IR decoder object irDecoder

```c
IRdecode Adafruit_CircuitPlayground::irDecoder
```


### the IR send object irSend

```c
IRsend Adafruit_CircuitPlayground::irSend
```


### begin()
Set up the CircuitPlayground hardware


```c
boolean Adafruit_CircuitPlayground::begin(uint8_t brightness=20)
```

!!! summary "引数"
	- uint8_t `brightness` Optional brightness to set the neopixels to 

!!! note "戻り値"
	boolean True if device is set up, false on any failure 



### slideSwitch()
read the slide switch



```c
boolean Adafruit_CircuitPlayground::slideSwitch(void)
```

!!! note "戻り値"
	boolean true if slide switch in set, false if not 



### redLED()
turn on or off the red LED on pin #13


```c
void Adafruit_CircuitPlayground::redLED(boolean v)
```

!!! summary "引数"
	- boolean `v` pass true to turn LED on, false to turn LED off 



### playTone()
play a tone on the onboard buzzer


```c
void Adafruit_CircuitPlayground::playTone(uint16_t freq, uint16_t time, boolean wait=true)
```

!!! summary "引数"
	- uint16_t `freq` the frequency to play 
	- uint16_t `time` the duration of the tone in milliseconds 
	- boolean `wait` Optional flag to wait for time milliseconds after playing the tone. Defaults to true. 



### leftButton()
read the left button



```c
boolean Adafruit_CircuitPlayground::leftButton(void)
```

!!! note "戻り値"
	boolean true if button is pressed, false if not 



### rightButton()
read the right button



```c
boolean Adafruit_CircuitPlayground::rightButton(void)
```

!!! note "戻り値"
	boolean true if button is pressed, false if not 



### lightSensor()
read the onboard lightsensor




```c
uint16_t Adafruit_CircuitPlayground::lightSensor(void)
```

!!! note "戻り値"
	uint16_t value between 0 and 1023 read from the light sensor 



### soundSensor()
read the onboard sound sensor. A reading of ~0 is silent, and loud audio will result in a reading between -500 and 500 or so.



```c
int16_t Adafruit_CircuitPlayground::soundSensor(void)
```

!!! note "戻り値"
	int16_t value of the sound sensor 



### temperature()
read the onboard thermistor.



```c
float Adafruit_CircuitPlayground::temperature(void)
```

!!! note "戻り値"
	float temperature reading in Centigrade. 



### temperatureF()
read the onboard thermistor.



```c
float Adafruit_CircuitPlayground::temperatureF(void)
```

!!! note "戻り値"
	float temperature reading in Farenheight. 



### readCap()
read capacitive touch sensor


```c
uint16_t Adafruit_CircuitPlayground::readCap(uint8_t p, uint8_t samples=10)
```

!!! summary "引数"
	- uint8_t `p` the pin to read. Must be a captouch enabled pin. 
	- uint8_t `samples` Optional number of samples to take. Defaults to 10. 

!!! note "戻り値"
	uint16_t measured captouch value 



### motionX()
read the X parameter of the onboard accelerometer. Value returned is defined by .



```c
float Adafruit_CircuitPlayground::motionX(void)
```

!!! note "戻り値"
	float X value of the accelerometer 



### motionY()
read the Y parameter of the onboard accelerometer. Value returned is defined by .



```c
float Adafruit_CircuitPlayground::motionY(void)
```

!!! note "戻り値"
	float Y value of the accelerometer 



### motionZ()
read the Z parameter of the onboard accelerometer. Value returned is defined by .



```c
float Adafruit_CircuitPlayground::motionZ(void)
```

!!! note "戻り値"
	float the Z value of the onboard accelerometer 



### setAccelRange()
set the range of the MEMS accelerometer.


```c
void Adafruit_CircuitPlayground::setAccelRange(lis3dh_range_t range)
```

!!! summary "引数"
	- lis3dh_range_t `range` the range to set the accelerometer to. LIS3DH_RANGE_2_G is the smallest (+-2G) but will give the greatest precision, while LIS3DH_RANGE_8_G is the largest (+-8G) but with the lease precision. LIS3DH_RANGE_4_G is in the middle. 



### setAccelTap()
turn on tap detection. Tap detection can detect single taps or 'double taps' (like a double-click).


```c
void Adafruit_CircuitPlayground::setAccelTap(uint8_t c, uint8_t clickthresh)
```

!!! summary "引数"
	- uint8_t `c` If c is 1 you will only detect single taps, one at a time. If c is 2, you will be able to detect both single taps and double taps. 
	- uint8_t `clickthresh` the threshold over which to register a tap 



### getAccelTap()
test whether or not a tap has been detected



```c
uint8_t Adafruit_CircuitPlayground::getAccelTap(void)
```

!!! note "戻り値"
	uint8_t 0 if no tap is detected, 1 if a single tap is detected, and 2 or 3 if double tap is detected. 



### clearPixels()
turn off all neopixels on the board


```c
void Adafruit_CircuitPlayground::clearPixels(void)
```



### setPixelColor()
set the color of a neopixel on the board


```c
void Adafruit_CircuitPlayground::setPixelColor(uint8_t p, uint32_t c)
```

!!! summary "引数"
	- uint8_t `p` the pixel to set. Pixel 0 is above the pad labeled 'GND' right next to the USB connector, while pixel 9 is above the pad labeled '3.3V' on the other side of the USB connector. 
	- uint32_t `c` a 24bit color value to set the pixel to 



### setPixelColor()
set the color of a neopixel on the board


```c
void Adafruit_CircuitPlayground::setPixelColor(uint8_t p, uint8_t r, uint8_t g, uint8_t b)
```

!!! summary "引数"
	- uint8_t `p` the pixel to set. Pixel 0 is above the pad labeled 'GND' right next to the USB connector, while pixel 9 is above the pad labeled '3.3V' on the other side of the USB connector. 
	- uint8_t `r` a 0 to 255 value corresponding to the red component of the desired color.
	- uint8_t `g` a 0 to 255 value corresponding to the green component of the desired color. 
	- uint8_t `b` a 0 to 255 value corresponding to the blue component of the desired color. 



### setBrightness()
set the global brightness of all neopixels.


```c
void Adafruit_CircuitPlayground::setBrightness(uint16_t b)
```

!!! summary "引数"
	- uint16_t `b` a 0 to 255 value corresponding to the desired brightness. The default brightness of all neopixels is 30. 



### sine8()
Get a sinusoidal value from a sine table


```c
uint8_t Adafruit_CircuitPlayground::sine8(uint8_t x)
```

!!! summary "引数"
	- uint8_t `x` a 0 to 255 value corresponding to an index to the sine table 

!!! note "戻り値"
	uint8_t An 8-bit sinusoidal value back 



### gamma8()
Get a gamma-corrected value from a gamma table


```c
uint8_t Adafruit_CircuitPlayground::gamma8(uint8_t x)
```

!!! summary "引数"
	- uint8_t `x` a 0 to 255 value corresponding to an index to the gamma table 

!!! note "戻り値"
	uint8_t An 8-bit gamma-corrected value back 



### colorWheel()
get a color value from the color wheel.


```c
uint32_t Adafruit_CircuitPlayground::colorWheel(uint8_t x)
```

!!! summary "引数"
	- uint8_t `x` 

!!! note "戻り値"
	uint32_t a color value. The colours are a transition r - g - b - back to r. 



### senseColor()
detect a color value from the light sensor


```c
void Adafruit_CircuitPlayground::senseColor(uint8_t &red, uint8_t &green, uint8_t &blue)
```

!!! summary "引数"
	- uint8_t & `red` the pointer to where the red component should be stored. 
	- uint8_t & `green` the pointer to where the green component should be stored. 
	- uint8_t & `blue` the pointer to where the blue component should be stored.



### senseColor()
detect a color using the onboard light sensor



```c
uint32_t Adafruit_CircuitPlayground::senseColor()
```

!!! note "戻り値"
	uint32_t a 24 bit color. The most significant byte is red, followed by green, and the least significant byte is blue. 



### isExpress()
check whether or not this device is a CircuitPlayground Express.



```c
boolean Adafruit_CircuitPlayground::isExpress(void)
```

!!! note "戻り値"
	boolean True if the device is a CircuitPlayground Express, false if it is a 'classic'. 



