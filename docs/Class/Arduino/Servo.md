# Servo



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_servo.html)

## メンバー

### Servo()



```c
Servo::Servo()
```



### attach()



```c
uint8_t Servo::attach(int pin)
```

!!! summary "引数"
	- int `pin` 

!!! note "戻り値"
	uint8_t



### attach()



```c
uint8_t Servo::attach(int pin, int min, int max)
```

!!! summary "引数"
	- int `pin` 
	- int `min` 
	- int `max` 

!!! note "戻り値"
	uint8_t



### detach()



```c
void Servo::detach()
```



### write()



```c
void Servo::write(int value)
```

!!! summary "引数"
	- int `value` 



### writeMicroseconds()



```c
void Servo::writeMicroseconds(int value)
```

!!! summary "引数"
	- int `value` 



### read()



```c
int Servo::read()
```

!!! note "戻り値"
	int



### readMicroseconds()



```c
int Servo::readMicroseconds()
```

!!! note "戻り値"
	int



### attached()



```c
bool Servo::attached()
```

!!! note "戻り値"
	bool



### Servo()
Construct a new  instance.

The new instance will not be attached to any pin. 
```c
Servo::Servo()
```



### attach()
Associate this instance with a servomotor whose input is connected to pin.



```c
bool Servo::attach(uint8 pin, uint16 minPulseWidth=MIN_PULSE_WIDTH, uint16 maxPulseWidth=MAX_PULSE_WIDTH, int16 minAngle=MIN_ANGLE, int16 maxAngle=MAX_ANGLE)
```

!!! summary "引数"
	- uint8 `pin` Pin connected to the servo pulse wave input. This pin must be capable of PWM output.
	- uint16 `minPulseWidth` Minimum pulse width to write to pin, in microseconds. This will be associated with a minAngle degree angle. Defaults to SERVO_DEFAULT_MIN_PW = 544.
	- uint16 `maxPulseWidth` Maximum pulse width to write to pin, in microseconds. This will be associated with a maxAngle degree angle. Defaults to SERVO_DEFAULT_MAX_PW = 2400.
	- int16 `minAngle` Target angle (in degrees) associated with minPulseWidth. Defaults to SERVO_DEFAULT_MIN_ANGLE = 0.
	- int16 `maxAngle` Target angle (in degrees) associated with maxPulseWidth. Defaults to SERVO_DEFAULT_MAX_ANGLE = 180.

!!! note "戻り値"
	bool



### detach()
Stop driving the servo pulse train.



```c
bool Servo::detach()
```

!!! note "戻り値"
	bool



### write()
Set the servomotor target angle.


```c
void Servo::write(int angle)
```

!!! summary "引数"
	- int `angle` Target angle, in degrees. If the target angle is outside the range specified at  time, it will be clamped to lie in that range.



### writeMicroseconds()
Set the pulse width, in microseconds.


```c
void Servo::writeMicroseconds(uint16 pulseWidth)
```

!!! summary "引数"
	- uint16 `pulseWidth` Pulse width to send to the servomotor, in microseconds. If outside of the range specified at  time, it is clamped to lie in that range.



### read()




```c
int Servo::read() const
```

!!! note "戻り値"
	int



### readMicroseconds()




```c
uint16 Servo::readMicroseconds() const
```

!!! note "戻り値"
	uint16



### attached()
Check if this instance is attached to a servo.




```c
bool Servo::attached() const
```

!!! note "戻り値"
	bool true if this instance is attached to a servo, false otherwise. 



### attachedPin()
Get the pin this instance is attached to.




```c
int Servo::attachedPin() const
```

!!! note "戻り値"
	int Pin number if currently attached to a pin, NOT_ATTACHED otherwise. 



