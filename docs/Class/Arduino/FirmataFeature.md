# FirmataFeature



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_firmata_feature.html)

## メンバー

### handleCapability()



```c
virtual void FirmataFeature::handleCapability(byte pin)=0
```

!!! summary "引数"
	- byte `pin` 



### handlePinMode()



```c
virtual boolean FirmataFeature::handlePinMode(byte pin, int mode)=0
```

!!! summary "引数"
	- byte `pin` 
	- int `mode` 

!!! note "戻り値"
	boolean



### handleSysex()



```c
virtual boolean FirmataFeature::handleSysex(byte command, byte argc, byte *argv)=0
```

!!! summary "引数"
	- byte `command` 
	- byte `argc` 
	- byte* `argv` 

!!! note "戻り値"
	boolean



### reset()



```c
virtual void FirmataFeature::reset()=0
```



