# Adafruit_CPlay_Speaker

Class that stores state and functions for the speaker on CircuitPlayground boards 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_adafruit___c_play___speaker.html)

## メンバー

### Adafruit_CPlay_Speaker()



```c
Adafruit_CPlay_Speaker::Adafruit_CPlay_Speaker(void)
```



### begin()
Sets up Circuit Playground speaker for PWM audio output: enables 48 KHz high-speed PWM mode, configures Timer/Counter 4, sets PWM duty cycle to 50% (speaker idle position).


```c
void Adafruit_CPlay_Speaker::begin(void)
```



### end()
Turns off PWM output to the speaker.


```c
void Adafruit_CPlay_Speaker::end(void)
```



### set()
Sets speaker position, enables PWM output if needed.


```c
void Adafruit_CPlay_Speaker::set(uint8_t value)
```

!!! summary "引数"
	- uint8_t `value` the value to set (0-255; 127=idle) 



### playSound()
Plays digitized 8-bit audio (optionally 10 bits on Express board) from a PROGMEM (flash memory) buffer. Maybe 1-3 seconds tops depending on sampling rate (e.g. 8000 Hz = 8 Kbytes/second). Max ~20K space avail on Circuit Playground, lots more on Circuit Playground Express. This function currently "blocks"  it will not play sounds in the background while other code runs.


```c
void Adafruit_CPlay_Speaker::playSound(const uint8_t *data, uint32_t length, uint16_t sampleRate, bool tenBit=false)
```

!!! summary "引数"
	- constuint8_t * `data` pointer to the audio data to play 
	- uint32_t `length` 
	- uint16_t `sampleRate` the sample rate of the data in samples per second 
	- bool `tenBit` Optional flag if true 10-bit mode is enabled. AVR ONLY 



### say()
speak the data at the passed location


```c
void Adafruit_CPlay_Speaker::say(const uint8_t *addr)
```

!!! summary "引数"
	- constuint8_t * `addr` pointer to the data 



### enable()
enable or disable the speaker. This function only works on 'Express' boards.


```c
void Adafruit_CPlay_Speaker::enable(bool e)
```

!!! summary "引数"
	- bool `e` pass true to enable, false to disable 



### off()
disable the speaker.



```c
void Adafruit_CPlay_Speaker::off(void)
```



### on()
enable the speaker.



```c
void Adafruit_CPlay_Speaker::on(void)
```



