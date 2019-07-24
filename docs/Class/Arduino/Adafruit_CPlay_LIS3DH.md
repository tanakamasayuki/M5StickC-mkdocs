# Adafruit_CPlay_LIS3DH

Class that stores state and functions for LIS3DH accelerometer on the circuitPlayground board 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_adafruit___c_play___l_i_s3_d_h.html)

## メンバー

### integer axis readings x

```c
int16_t Adafruit_CPlay_LIS3DH::x
```


###  y

```c
int16_t Adafruit_CPlay_LIS3DH::y
```


###  z

```c
int16_t Adafruit_CPlay_LIS3DH::z
```


###  x_g
floating point axis readings
```c
float Adafruit_CPlay_LIS3DH::x_g
```


###  y_g

```c
float Adafruit_CPlay_LIS3DH::y_g
```


###  z_g

```c
float Adafruit_CPlay_LIS3DH::z_g
```


### Adafruit_CPlay_LIS3DH()
Instantiates a new LIS3DH class in I2C mode


```c
Adafruit_CPlay_LIS3DH::Adafruit_CPlay_LIS3DH(void)
```



### Adafruit_CPlay_LIS3DH()
Instantiates a new LIS3DH class in hardware SPI mode


```c
Adafruit_CPlay_LIS3DH::Adafruit_CPlay_LIS3DH(int8_t cspin)
```

!!! summary "引数"
	- int8_t `cspin` the pin used as a chip select 



### Adafruit_CPlay_LIS3DH()
Instantiates a new LIS3DH class in software SPI mode


```c
Adafruit_CPlay_LIS3DH::Adafruit_CPlay_LIS3DH(int8_t cspin, int8_t mosipin, int8_t misopin, int8_t sckpin)
```

!!! summary "引数"
	- int8_t `cspin` the pin used as a chip select 
	- int8_t `mosipin` the pin used as master-out-slave-in 
	- int8_t `misopin` the pin used as master-in-slave-out 
	- int8_t `sckpin` the pin used as SPI serial clock 



### begin()
Setups the HW (reads coefficients values, etc.)


```c
bool Adafruit_CPlay_LIS3DH::begin(uint8_t addr=LIS3DH_DEFAULT_ADDRESS)
```

!!! summary "引数"
	- uint8_t `addr` 

!!! note "戻り値"
	bool true on success, false on any failure 



### read()
read x, y, and z axis data and store in class variables.


```c
void Adafruit_CPlay_LIS3DH::read()
```



### readADC()
Read the auxilary ADC


```c
int16_t Adafruit_CPlay_LIS3DH::readADC(uint8_t a)
```

!!! summary "引数"
	- uint8_t `a` 

!!! note "戻り値"
	int16_t the measured value 



### setRange()
Sets the g range for the accelerometer


```c
void Adafruit_CPlay_LIS3DH::setRange(lis3dh_range_t range)
```

!!! summary "引数"
	- lis3dh_range_t `range` the desired range of the device. Pass LIS3DH_RANGE_2_G for highest sensitivity and lowest max/min value (+-2G), LIS3DH_RANGE_16_G for lowest sensitivity and highest max/min value (+-16G). Other acceptable values are LIS3DH_RANGE_4_G and LIS3DH_RANGE_8_G. 



### getRange()
Sets the g range for the accelerometer



```c
lis3dh_range_t Adafruit_CPlay_LIS3DH::getRange(void)
```

!!! note "戻り値"
	lis3dh_range_t the range reading from the sensor. 



### setDataRate()
Sets the data rate for the LIS3DH (controls power consumption)


```c
void Adafruit_CPlay_LIS3DH::setDataRate(lis3dh_dataRate_t dataRate)
```

!!! summary "引数"
	- lis3dh_dataRate_t `dataRate` the desired datarate. 



### getDataRate()
Sets the data rate for the LIS3DH (controls power consumption)



```c
lis3dh_dataRate_t Adafruit_CPlay_LIS3DH::getDataRate(void)
```

!!! note "戻り値"
	lis3dh_dataRate_t the data rate reading from the sensor. 



### getEvent()
Gets the most recent sensor event


```c
bool Adafruit_CPlay_LIS3DH::getEvent(sensors_event_t *event)
```

!!! summary "引数"
	- sensors_event_t* `event` the pointer to place the event reading in 

!!! note "戻り値"
	bool none 



### getSensor()
Gets the  data


```c
void Adafruit_CPlay_LIS3DH::getSensor(sensor_t *sensor)
```

!!! summary "引数"
	- sensor_t* `sensor` the pointer to place sensor information into. 



### setClick()
Set INT to output for single or double click


```c
void Adafruit_CPlay_LIS3DH::setClick(uint8_t c, uint8_t clickthresh, uint8_t timelimit=10, uint8_t timelatency=20, uint8_t timewindow=255)
```

!!! summary "引数"
	- uint8_t `c` the number of taps to detect. pass 1 for single tap on all axis, 2 for double tap on all axis. Pass 0 to disable taps. 
	- uint8_t `clickthresh` the threshold over which to register a tap. 
	- uint8_t `timelimit` Optional time limit for a tap. Defaults to 10 
	- uint8_t `timelatency` Optional tap latency. defaults to 20 
	- uint8_t `timewindow` Optional time window. defaults to 255 



### getClick()
get a tap reading



```c
uint8_t Adafruit_CPlay_LIS3DH::getClick(void)
```

!!! note "戻り値"
	uint8_t the tap reading 



