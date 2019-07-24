# EspClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_esp_class.html)

## メンバー

### EspClass()



```c
EspClass::EspClass()
```



### ~EspClass()



```c
EspClass::~EspClass()
```



### restart()



```c
void EspClass::restart()
```



### getHeapSize()



```c
uint32_t EspClass::getHeapSize()
```

!!! note "戻り値"
	uint32_t



### getFreeHeap()



```c
uint32_t EspClass::getFreeHeap()
```

!!! note "戻り値"
	uint32_t



### getMinFreeHeap()



```c
uint32_t EspClass::getMinFreeHeap()
```

!!! note "戻り値"
	uint32_t



### getMaxAllocHeap()



```c
uint32_t EspClass::getMaxAllocHeap()
```

!!! note "戻り値"
	uint32_t



### getPsramSize()



```c
uint32_t EspClass::getPsramSize()
```

!!! note "戻り値"
	uint32_t



### getFreePsram()



```c
uint32_t EspClass::getFreePsram()
```

!!! note "戻り値"
	uint32_t



### getMinFreePsram()



```c
uint32_t EspClass::getMinFreePsram()
```

!!! note "戻り値"
	uint32_t



### getMaxAllocPsram()



```c
uint32_t EspClass::getMaxAllocPsram()
```

!!! note "戻り値"
	uint32_t



### getChipRevision()



```c
uint8_t EspClass::getChipRevision()
```

!!! note "戻り値"
	uint8_t



### getCpuFreqMHz()



```c
uint8_t EspClass::getCpuFreqMHz()
```

!!! note "戻り値"
	uint8_t



### getCycleCount()



```c
uint32_t EspClass::getCycleCount()
```

!!! note "戻り値"
	uint32_t



### getSdkVersion()



```c
const char * EspClass::getSdkVersion()
```

!!! note "戻り値"
	constchar *



### deepSleep()



```c
void EspClass::deepSleep(uint32_t time_us)
```

!!! summary "引数"
	- uint32_t `time_us` 



### getFlashChipSize()



```c
uint32_t EspClass::getFlashChipSize()
```

!!! note "戻り値"
	uint32_t



### getFlashChipSpeed()



```c
uint32_t EspClass::getFlashChipSpeed()
```

!!! note "戻り値"
	uint32_t



### getFlashChipMode()



```c
FlashMode_t EspClass::getFlashChipMode()
```

!!! note "戻り値"
	FlashMode_t



### magicFlashChipSize()



```c
uint32_t EspClass::magicFlashChipSize(uint8_t byte)
```

!!! summary "引数"
	- uint8_t `byte` 

!!! note "戻り値"
	uint32_t



### magicFlashChipSpeed()



```c
uint32_t EspClass::magicFlashChipSpeed(uint8_t byte)
```

!!! summary "引数"
	- uint8_t `byte` 

!!! note "戻り値"
	uint32_t



### magicFlashChipMode()



```c
FlashMode_t EspClass::magicFlashChipMode(uint8_t byte)
```

!!! summary "引数"
	- uint8_t `byte` 

!!! note "戻り値"
	FlashMode_t



### getSketchSize()



```c
uint32_t EspClass::getSketchSize()
```

!!! note "戻り値"
	uint32_t



### getSketchMD5()



```c
String EspClass::getSketchMD5()
```

!!! note "戻り値"
	String



### getFreeSketchSpace()



```c
uint32_t EspClass::getFreeSketchSpace()
```

!!! note "戻り値"
	uint32_t



### flashEraseSector()



```c
bool EspClass::flashEraseSector(uint32_t sector)
```

!!! summary "引数"
	- uint32_t `sector` 

!!! note "戻り値"
	bool



### flashWrite()



```c
bool EspClass::flashWrite(uint32_t offset, uint32_t *data, size_t size)
```

!!! summary "引数"
	- uint32_t `offset` 
	- uint32_t* `data` 
	- size_t `size` 

!!! note "戻り値"
	bool



### flashRead()



```c
bool EspClass::flashRead(uint32_t offset, uint32_t *data, size_t size)
```

!!! summary "引数"
	- uint32_t `offset` 
	- uint32_t* `data` 
	- size_t `size` 

!!! note "戻り値"
	bool



### getEfuseMac()



```c
uint64_t EspClass::getEfuseMac()
```

!!! note "戻り値"
	uint64_t



