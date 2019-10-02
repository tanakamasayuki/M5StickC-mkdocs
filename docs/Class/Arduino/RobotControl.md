# RobotControl



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_robot_control.html)

## メンバー

###  IRarray

```c
uint16_t RobotControl::IRarray[5]
```


###  foreGround

```c
uint16_t RobotControl::foreGround
```


###  backGround

```c
uint16_t RobotControl::backGround
```


### RobotControl()



```c
RobotControl::RobotControl()
```



### begin()



```c
void RobotControl::begin()
```



### setMode()



```c
void RobotControl::setMode(uint8_t mode)
```

!!! summary "引数"
	- uint8_t `mode` 



### digitalRead()



```c
bool RobotControl::digitalRead(uint8_t port)
```

!!! summary "引数"
	- uint8_t `port` 

!!! note "戻り値"
	bool



### analogRead()



```c
int RobotControl::analogRead(uint8_t port)
```

!!! summary "引数"
	- uint8_t `port` 

!!! note "戻り値"
	int



### digitalWrite()



```c
void RobotControl::digitalWrite(uint8_t port, bool value)
```

!!! summary "引数"
	- uint8_t `port` 
	- bool `value` 



### analogWrite()



```c
void RobotControl::analogWrite(uint8_t port, uint8_t value)
```

!!! summary "引数"
	- uint8_t `port` 
	- uint8_t `value` 



### updateIR()



```c
void RobotControl::updateIR()
```



### knobRead()



```c
int RobotControl::knobRead()
```

!!! note "戻り値"
	int



### trimRead()



```c
int RobotControl::trimRead()
```

!!! note "戻り値"
	int



### beginSpeaker()



```c
void RobotControl::beginSpeaker(uint16_t frequency=44100)
```

!!! summary "引数"
	- uint16_t `frequency` 



### playMelody()



```c
void RobotControl::playMelody(char *script)
```

!!! summary "引数"
	- char * `script` 



### playFile()



```c
void RobotControl::playFile(char *filename)
```

!!! summary "引数"
	- char * `filename` 



### stopPlayFile()



```c
void RobotControl::stopPlayFile()
```



### beep()



```c
void RobotControl::beep(int beep_length=BEEP_SIMPLE)
```

!!! summary "引数"
	- int `beep_length` 



### tempoWrite()



```c
void RobotControl::tempoWrite(int tempo)
```

!!! summary "引数"
	- int `tempo` 



### tuneWrite()



```c
void RobotControl::tuneWrite(float tune)
```

!!! summary "引数"
	- float `tune` 



### compassRead()



```c
uint16_t RobotControl::compassRead()
```

!!! note "戻り値"
	uint16_t



### drawCompass()



```c
void RobotControl::drawCompass(uint16_t value)
```

!!! summary "引数"
	- uint16_t `value` 



### drawBase()



```c
void RobotControl::drawBase()
```



### drawDire()



```c
void RobotControl::drawDire(int16_t dire)
```

!!! summary "引数"
	- int16_t `dire` 



### keyboardCalibrate()



```c
void RobotControl::keyboardCalibrate(int *vals)
```

!!! summary "引数"
	- int * `vals` 



### keyboardRead()



```c
int8_t RobotControl::keyboardRead()
```

!!! note "戻り値"
	int8_t



### moveForward()



```c
void RobotControl::moveForward(int speed)
```

!!! summary "引数"
	- int `speed` 



### moveBackward()



```c
void RobotControl::moveBackward(int speed)
```

!!! summary "引数"
	- int `speed` 



### turnLeft()



```c
void RobotControl::turnLeft(int speed)
```

!!! summary "引数"
	- int `speed` 



### turnRight()



```c
void RobotControl::turnRight(int speed)
```

!!! summary "引数"
	- int `speed` 



### motorsStop()



```c
void RobotControl::motorsStop()
```



### motorsWritePct()



```c
void RobotControl::motorsWritePct(int speedLeftPct, int speedRightPct)
```

!!! summary "引数"
	- int `speedLeftPct` 
	- int `speedRightPct` 



### motorsWrite()



```c
void RobotControl::motorsWrite(int speedLeft, int speedRight)
```

!!! summary "引数"
	- int `speedLeft` 
	- int `speedRight` 



### pointTo()



```c
void RobotControl::pointTo(int degrees)
```

!!! summary "引数"
	- int `degrees` 



### turn()



```c
void RobotControl::turn(int degress)
```

!!! summary "引数"
	- int `degress` 



### lineFollowConfig()



```c
void RobotControl::lineFollowConfig(uint8_t KP, uint8_t KD, uint8_t robotSpeed, uint8_t intergrationTime)
```

!!! summary "引数"
	- uint8_t `KP` 
	- uint8_t `KD` 
	- uint8_t `robotSpeed` 
	- uint8_t `intergrationTime` 



### beginTFT()



```c
void RobotControl::beginTFT(uint16_t foreGround=BLACK, uint16_t background=WHITE)
```

!!! summary "引数"
	- uint16_t `foreGround` 
	- uint16_t `background` 



### debugPrint()



```c
void RobotControl::debugPrint(long value, uint8_t x=0, uint8_t y=0)
```

!!! summary "引数"
	- long `value` 
	- uint8_t `x` 
	- uint8_t `y` 



### clearScreen()



```c
void RobotControl::clearScreen()
```



### drawBMP()



```c
void RobotControl::drawBMP(char *filename, uint8_t x, uint8_t y)
```

!!! summary "引数"
	- char * `filename` 
	- uint8_t `x` 
	- uint8_t `y` 



### _drawBMP()



```c
void RobotControl::_drawBMP(uint32_t iconOffset, uint8_t x, uint8_t y, uint8_t width, uint8_t height)
```

!!! summary "引数"
	- uint32_t `iconOffset` 
	- uint8_t `x` 
	- uint8_t `y` 
	- uint8_t `width` 
	- uint8_t `height` 



### _drawBMP()



```c
void RobotControl::_drawBMP(char *filename, uint8_t x, uint8_t y)
```

!!! summary "引数"
	- char * `filename` 
	- uint8_t `x` 
	- uint8_t `y` 



### beginBMPFromEEPROM()



```c
void RobotControl::beginBMPFromEEPROM()
```



### endBMPFromEEPROM()



```c
void RobotControl::endBMPFromEEPROM()
```



### beginSD()



```c
void RobotControl::beginSD()
```



### userNameRead()



```c
void RobotControl::userNameRead(char *container)
```

!!! summary "引数"
	- char * `container` 



### robotNameRead()



```c
void RobotControl::robotNameRead(char *container)
```

!!! summary "引数"
	- char * `container` 



### cityNameRead()



```c
void RobotControl::cityNameRead(char *container)
```

!!! summary "引数"
	- char * `container` 



### countryNameRead()



```c
void RobotControl::countryNameRead(char *container)
```

!!! summary "引数"
	- char * `container` 



### userNameWrite()



```c
void RobotControl::userNameWrite(char *text)
```

!!! summary "引数"
	- char * `text` 



### robotNameWrite()



```c
void RobotControl::robotNameWrite(char *text)
```

!!! summary "引数"
	- char * `text` 



### cityNameWrite()



```c
void RobotControl::cityNameWrite(char *text)
```

!!! summary "引数"
	- char * `text` 



### countryNameWrite()



```c
void RobotControl::countryNameWrite(char *text)
```

!!! summary "引数"
	- char * `text` 



### isActionDone()



```c
bool RobotControl::isActionDone()
```

!!! note "戻り値"
	bool



### pauseMode()



```c
void RobotControl::pauseMode(uint8_t onOff)
```

!!! summary "引数"
	- uint8_t `onOff` 



### displayLogos()



```c
void RobotControl::displayLogos()
```



### waitContinue()



```c
void RobotControl::waitContinue(uint8_t key=BUTTON_MIDDLE)
```

!!! summary "引数"
	- uint8_t `key` 



