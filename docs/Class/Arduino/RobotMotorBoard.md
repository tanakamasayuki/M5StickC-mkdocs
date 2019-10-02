# RobotMotorBoard



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_robot_motor_board.html)

## メンバー

### RobotMotorBoard()



```c
RobotMotorBoard::RobotMotorBoard()
```



### begin()



```c
void RobotMotorBoard::begin()
```



### process()



```c
void RobotMotorBoard::process()
```



### parseCommand()



```c
void RobotMotorBoard::parseCommand()
```



### IRread()



```c
int RobotMotorBoard::IRread(uint8_t num)
```

!!! summary "引数"
	- uint8_t `num` 

!!! note "戻り値"
	int



### setMode()



```c
void RobotMotorBoard::setMode(uint8_t mode)
```

!!! summary "引数"
	- uint8_t `mode` 



### pauseMode()



```c
void RobotMotorBoard::pauseMode(bool onOff)
```

!!! summary "引数"
	- bool `onOff` 



### motorsWrite()



```c
void RobotMotorBoard::motorsWrite(int speedL, int speedR)
```

!!! summary "引数"
	- int `speedL` 
	- int `speedR` 



### motorsWritePct()



```c
void RobotMotorBoard::motorsWritePct(int speedLpct, int speedRpct)
```

!!! summary "引数"
	- int `speedLpct` 
	- int `speedRpct` 



### motorsStop()



```c
void RobotMotorBoard::motorsStop()
```



