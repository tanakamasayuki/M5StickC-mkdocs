# その他関数群

delay()やmillis()などのシステム系関数群です。

## メンバー









### vPortYield()



```c
void vPortYield(void)
```



### yield()



```c
void yield(void)
```


### temperatureRead()



```c
float temperatureRead()
```

!!! note "戻り値"
	float



### enableCore0WDT()



```c
void enableCore0WDT()
```


### disableCore0WDT()



```c
void disableCore0WDT()
```




### enableCore1WDT()



```c
void enableCore1WDT()
```





### disableCore1WDT()



```c
void disableCore1WDT()
```




### xTaskCreateUniversal()



```c
BaseType_t xTaskCreateUniversal(TaskFunction_t pxTaskCode, const char *const pcName, const uint32_t usStackDepth, void *const pvParameters, UBaseType_t uxPriority, TaskHandle_t *const pxCreatedTask, const BaseType_t xCoreID)
```

!!! summary "引数"
	- TaskFunction_t `pxTaskCode` 
	- const char *const `pcName` 
	- const uint32_t `usStackDepth` 
	- void *const `pvParameters` 
	- UBaseType_t `uxPriority` 
	- TaskHandle_t *const `pxCreatedTask` 
	- const BaseType_t `xCoreID` 

!!! note "戻り値"
	BaseType_t



### micros()



```c
unsigned long micros()
```

!!! note "戻り値"
	unsigned long



### millis()



```c
unsigned long millis()
```

!!! note "戻り値"
	unsigned long



### delay()



```c
void delay(uint32_t)
```

!!! summary "引数"
	- uint32_t `` 




### delayMicroseconds()



```c
void delayMicroseconds(uint32_t us)
```

!!! summary "引数"
	- uint32_t `us` 





### arduino_phy_init()



```c
void arduino_phy_init()
```





### initArduino()



```c
void initArduino()
```





