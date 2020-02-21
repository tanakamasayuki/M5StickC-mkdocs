# _Esplora



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class___esplora.html)

## メンバー

### _Esplora()



```c
_Esplora::_Esplora()
```



### readSlider()



```c
unsigned int _Esplora::readSlider()
```

!!! note "戻り値"
	unsigned int



### readLightSensor()



```c
unsigned int _Esplora::readLightSensor()
```

!!! note "戻り値"
	unsigned int



### readTemperature()



```c
int _Esplora::readTemperature(const byte scale)
```

!!! summary "引数"
	- const `scale` 

!!! note "戻り値"
	int



### readMicrophone()



```c
unsigned int _Esplora::readMicrophone()
```

!!! note "戻り値"
	unsigned int



### readJoystickSwitch()



```c
unsigned int _Esplora::readJoystickSwitch()
```

!!! note "戻り値"
	unsigned int



### readJoystickX()



```c
int _Esplora::readJoystickX()
```

!!! note "戻り値"
	int



### readJoystickY()



```c
int _Esplora::readJoystickY()
```

!!! note "戻り値"
	int



### readAccelerometer()



```c
int _Esplora::readAccelerometer(const byte axis)
```

!!! summary "引数"
	- const `axis` 

!!! note "戻り値"
	int



### readButton()



```c
boolean _Esplora::readButton(byte channel)
```

!!! summary "引数"
	- byte `channel` 

!!! note "戻り値"
	boolean



### readJoystickButton()



```c
boolean _Esplora::readJoystickButton()
```

!!! note "戻り値"
	boolean



### writeRGB()



```c
void _Esplora::writeRGB(byte red, byte green, byte blue)
```

!!! summary "引数"
	- byte `red` 
	- byte `green` 
	- byte `blue` 



### writeRed()



```c
void _Esplora::writeRed(byte red)
```

!!! summary "引数"
	- byte `red` 



### writeGreen()



```c
void _Esplora::writeGreen(byte green)
```

!!! summary "引数"
	- byte `green` 



### writeBlue()



```c
void _Esplora::writeBlue(byte blue)
```

!!! summary "引数"
	- byte `blue` 



### readRed()



```c
byte _Esplora::readRed()
```

!!! note "戻り値"
	byte



### readGreen()



```c
byte _Esplora::readGreen()
```

!!! note "戻り値"
	byte



### readBlue()



```c
byte _Esplora::readBlue()
```

!!! note "戻り値"
	byte



### tone()



```c
void _Esplora::tone(unsigned int freq)
```

!!! summary "引数"
	- unsigned int `freq` 



### tone()



```c
void _Esplora::tone(unsigned int freq, unsigned long duration)
```

!!! summary "引数"
	- unsigned int `freq` 
	- unsigned long `duration` 



### noTone()



```c
void _Esplora::noTone()
```



### readTinkerkitInput()



```c
unsigned int _Esplora::readTinkerkitInput(byte whichInput)
```

!!! summary "引数"
	- byte `whichInput` 

!!! note "戻り値"
	unsigned int



### readTinkerkitInputA()



```c
unsigned int _Esplora::readTinkerkitInputA()
```

!!! note "戻り値"
	unsigned int



### readTinkerkitInputB()



```c
unsigned int _Esplora::readTinkerkitInputB()
```

!!! note "戻り値"
	unsigned int



