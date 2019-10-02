# GSM3SoftSerial



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_soft_serial.html)

## メンバー

###  cb

```c
GSM3CircularBuffer GSM3SoftSerial::cb
```


### tunedDelay()



```c
void GSM3SoftSerial::tunedDelay(uint16_t delay)
```

!!! summary "引数"
	- uint16_t `delay` Time to delay 



### handle_interrupt()


Manage interruptions 
```c
void GSM3SoftSerial::handle_interrupt()
```



### registerMgr()



```c
void GSM3SoftSerial::registerMgr(GSM3SoftSerialMgr *manager)
```

!!! summary "引数"
	- GSM3SoftSerialMgr* `manager` Serial manager 



### spaceAvailable()


If there is spaceAvailable in the buffer, lets send a XON 
```c
void GSM3SoftSerial::spaceAvailable()
```



### write()



```c
size_t GSM3SoftSerial::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t 1 if succesful, 0 if transmission delay = 0 



### GSM3SoftSerial()


Constructor 
```c
GSM3SoftSerial::GSM3SoftSerial()
```



### begin()



```c
int GSM3SoftSerial::begin(long speed)
```

!!! summary "引数"
	- long `speed` Baudrate 

!!! note "戻り値"
	int 



### close()


Close serial connection 
```c
void GSM3SoftSerial::close()
```



