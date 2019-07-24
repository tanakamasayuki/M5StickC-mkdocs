# Adafruit_Sensor

Sensor API class for CircuitPlayground board 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_adafruit___sensor.html)

## メンバー

### Adafruit_Sensor()



```c
Adafruit_Sensor::Adafruit_Sensor()
```



### ~Adafruit_Sensor()



```c
virtual Adafruit_Sensor::~Adafruit_Sensor()
```



### enableAutoRange()
enable or disable auto-ranging for the sensor


```c
virtual void Adafruit_Sensor::enableAutoRange(bool enabled)
```

!!! summary "引数"
	- bool `enabled` pass true to enable auto-ranging, false to disable 



### getEvent()
enable auto-ranging for the sensor



```c
virtual bool Adafruit_Sensor::getEvent(sensors_event_t *)=0
```

!!! summary "引数"
	- sensors_event_t* `` 

!!! note "戻り値"
	bool true on success, false on failure 



### getSensor()
get information on the sensor


```c
virtual void Adafruit_Sensor::getSensor(sensor_t *)=0
```

!!! summary "引数"
	- sensor_t* `` 



