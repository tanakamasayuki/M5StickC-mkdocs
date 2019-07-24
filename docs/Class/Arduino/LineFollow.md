# LineFollow



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_line_follow.html)

## メンバー

### LineFollow()



```c
LineFollow::LineFollow()
```



### calibIRs()



```c
void LineFollow::calibIRs()
```



### runLineFollow()



```c
void LineFollow::runLineFollow()
```



### config()



```c
void LineFollow::config(uint8_t KP, uint8_t KD, uint8_t robotSpeed, uint8_t intergrationTime)
```

!!! summary "引数"
	- uint8_t `KP` 
	- uint8_t `KD` 
	- uint8_t `robotSpeed` 
	- uint8_t `intergrationTime` 



### motorsWritePct()



```c
virtual void LineFollow::motorsWritePct(int speedLpct, int speedRpct)=0
```

!!! summary "引数"
	- int `speedLpct` 
	- int `speedRpct` 



### motorsStop()



```c
virtual void LineFollow::motorsStop()=0
```



### _IRread()



```c
virtual int LineFollow::_IRread(uint8_t num)=0
```

!!! summary "引数"
	- uint8_t `num` 

!!! note "戻り値"
	int



