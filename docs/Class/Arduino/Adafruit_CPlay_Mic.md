# Adafruit_CPlay_Mic

Class that stores state and functions for the microphone on CircuitPlayground boards 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_adafruit___c_play___mic.html)

## メンバー

### Adafruit_CPlay_Mic()



```c
Adafruit_CPlay_Mic::Adafruit_CPlay_Mic(void)
```



### peak()
Reads ADC for given interval (in milliseconds, 1-65535). Uses ADC free-run mode w/polling on AVR. Any currently-installed ADC interrupt handler will be temporarily disabled while this runs.


```c
int Adafruit_CPlay_Mic::peak(uint16_t ms) __attribute__((deprecated))
```

!!! summary "引数"
	- uint16_t `ms` the number of milliseconds to sample 

!!! note "戻り値"
	int max deviation from DC_OFFSET (e.g. 0-341) 



### capture()
capture the passed number of samples and place them in buf.


```c
void Adafruit_CPlay_Mic::capture(int16_t *buf, uint16_t nSamples)
```

!!! summary "引数"
	- int16_t * `buf` the buffer to store the samples in 
	- uint16_t `nSamples` the number of samples to take



### fft()
AVR ONLY: Performs one cycle of fast Fourier transform (FFT) with audio captured from mic on A4. Output is 32 'bins,' each covering an equal range of frequencies from 0 to 4800 Hz (i.e. 0-150 Hz, 150-300 Hz, 300-450, etc). Needs about 450 bytes free RAM to operate.


```c
void Adafruit_CPlay_Mic::fft(uint16_t *spectrum)
```

!!! summary "引数"
	- uint16_t * `spectrum` the buffer to store the results in. Must be 32 bytes in length.



### soundPressureLevel()
Returns somewhat-calibrated sound pressure level.


```c
float Adafruit_CPlay_Mic::soundPressureLevel(uint16_t ms)
```

!!! summary "引数"
	- uint16_t `ms` Milliseconds to continuously sample microphone over, 10ms is a good start. 

!!! note "戻り値"
	float Floating point Sound Pressure Level, tends to range from 40-120 db SPL 



