# SerialFirmata



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_serial_firmata.html)

## メンバー

### SerialFirmata()



```c
SerialFirmata::SerialFirmata()
```



### handlePinMode()



```c
boolean SerialFirmata::handlePinMode(byte pin, int mode)
```

!!! summary "引数"
	- byte `pin` 
	- int `mode` 

!!! note "戻り値"
	boolean



### handleCapability()



```c
void SerialFirmata::handleCapability(byte pin)
```

!!! summary "引数"
	- byte `pin` 



### handleSysex()



```c
boolean SerialFirmata::handleSysex(byte command, byte argc, byte *argv)
```

!!! summary "引数"
	- byte `command` 
	- byte `argc` 
	- byte* `argv` 

!!! note "戻り値"
	boolean



### update()



```c
void SerialFirmata::update()
```



### reset()



```c
void SerialFirmata::reset()
```



### checkSerial()



```c
void SerialFirmata::checkSerial()
```



