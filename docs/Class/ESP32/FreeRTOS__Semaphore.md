# FreeRTOS::Semaphore



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_free_r_t_o_s_1_1_semaphore.html)

## メンバー

### Semaphore()



```c
FreeRTOS::Semaphore::Semaphore(std::string owner="<Unknown>")
```

!!! summary "引数"
	- std::string `owner` 



### ~Semaphore()



```c
FreeRTOS::Semaphore::~Semaphore()
```



### give()
Give a semaphore. The  is given.


```c
void FreeRTOS::Semaphore::give()
```



### give()
Give a semaphore. The  is given with an associated value.


```c
void FreeRTOS::Semaphore::give(uint32_t value)
```

!!! summary "引数"
	- uint32_t `value` The value to associate with the semaphore. 



### giveFromISR()
Give a semaphore from an ISR.


```c
void FreeRTOS::Semaphore::giveFromISR()
```



### setName()
Set the name of the semaphore.


```c
void FreeRTOS::Semaphore::setName(std::string name)
```

!!! summary "引数"
	- std::string `name` The name of the semaphore. 



### take()
Take a semaphore. Take a semaphore and wait indefinitely.


```c
bool FreeRTOS::Semaphore::take(std::string owner="<Unknown>")
```

!!! summary "引数"
	- std::string `owner` The new owner (for debugging) 

!!! note "戻り値"
	bool True if we took the semaphore. 



### take()
Take a semaphore. Take a semaphore but return if we haven't obtained it in the given period of milliseconds.


```c
bool FreeRTOS::Semaphore::take(uint32_t timeoutMs, std::string owner="<Unknown>")
```

!!! summary "引数"
	- uint32_t `timeoutMs` Timeout in milliseconds. 
	- std::string `owner` The new owner (for debugging) 

!!! note "戻り値"
	bool True if we took the semaphore. 



### toString()
Create a string representation of the semaphore.



```c
std::string FreeRTOS::Semaphore::toString()
```

!!! note "戻り値"
	std::string A string representation of the semaphore. 



### wait()
Wait for a semaphore to be released by trying to take it and then releasing it again.


```c
uint32_t FreeRTOS::Semaphore::wait(std::string owner="<Unknown>")
```

!!! summary "引数"
	- std::string `owner` A debug tag. 

!!! note "戻り値"
	uint32_t The value associated with the semaphore. 



### timedWait()
Wait for a semaphore to be released in a given period of time by trying to take it and then releasing it again. The value associated with the semaphore can be taken by  call after return


```c
bool FreeRTOS::Semaphore::timedWait(std::string owner="<Unknown>", uint32_t timeoutMs=portMAX_DELAY)
```

!!! summary "引数"
	- std::string `owner` A debug tag. 
	- uint32_t `timeoutMs` timeout to wait in ms. 

!!! note "戻り値"
	bool True if we took the semaphore within timeframe. 



### value()



```c
uint32_t FreeRTOS::Semaphore::value()
```

!!! note "戻り値"
	uint32_t



