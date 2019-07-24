# FreeRTOS

Interface to FreeRTOS functions. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_free_r_t_o_s.html)

## メンバー

### sleep()



```c
void FreeRTOS::sleep(uint32_t ms)
```

!!! summary "引数"
	- uint32_t `ms` The period in milliseconds for which to sleep. 



### startTask()



```c
void FreeRTOS::startTask(void task(void *), std::string taskName, void *param=nullptr, uint32_t stackSize=2048)
```

!!! summary "引数"
	- void `task` The function pointer to the function to be run in the task. 
	- std::string `taskName` A string identifier for the task. 
	- void * `param` An optional parameter to be passed to the started task. 
	- uint32_t `stackSize` An optional paremeter supplying the size of the stack in which to run the task. 



### deleteTask()



```c
void FreeRTOS::deleteTask(TaskHandle_t pTask=nullptr)
```

!!! summary "引数"
	- TaskHandle_t `pTask` An optional handle to the task to be deleted. If not supplied the calling task will be deleted. 



### getTimeSinceStart()


Get the time in milliseconds since the FreeRTOS scheduler started. 

```c
uint32_t FreeRTOS::getTimeSinceStart()
```

!!! note "戻り値"
	uint32_t The time in milliseconds since the FreeRTOS scheduler started. 



