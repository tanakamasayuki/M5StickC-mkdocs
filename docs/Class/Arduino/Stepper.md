# Stepper



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_stepper.html)

## メンバー

### Stepper()



```c
Stepper::Stepper(int number_of_steps, int motor_pin_1, int motor_pin_2)
```

!!! summary "引数"
	- int `number_of_steps` 
	- int `motor_pin_1` 
	- int `motor_pin_2` 



### Stepper()



```c
Stepper::Stepper(int number_of_steps, int motor_pin_1, int motor_pin_2, int motor_pin_3, int motor_pin_4)
```

!!! summary "引数"
	- int `number_of_steps` 
	- int `motor_pin_1` 
	- int `motor_pin_2` 
	- int `motor_pin_3` 
	- int `motor_pin_4` 



### Stepper()



```c
Stepper::Stepper(int number_of_steps, int motor_pin_1, int motor_pin_2, int motor_pin_3, int motor_pin_4, int motor_pin_5)
```

!!! summary "引数"
	- int `number_of_steps` 
	- int `motor_pin_1` 
	- int `motor_pin_2` 
	- int `motor_pin_3` 
	- int `motor_pin_4` 
	- int `motor_pin_5` 



### setSpeed()



```c
void Stepper::setSpeed(long whatSpeed)
```

!!! summary "引数"
	- long `whatSpeed` 



### step()



```c
void Stepper::step(int number_of_steps)
```

!!! summary "引数"
	- int `number_of_steps` 



### version()



```c
int Stepper::version(void)
```

!!! note "戻り値"
	int



