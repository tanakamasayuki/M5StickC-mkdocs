# Stream



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_stream.html)

## メンバー

### available()



```c
virtual int Stream::available()=0
```

!!! note "戻り値"
	int



### read()



```c
virtual int Stream::read()=0
```

!!! note "戻り値"
	int



### peek()



```c
virtual int Stream::peek()=0
```

!!! note "戻り値"
	int



### Stream()



```c
Stream::Stream()
```



### setTimeout()



```c
void Stream::setTimeout(unsigned long timeout)
```

!!! summary "引数"
	- unsigned long `timeout` 



### getTimeout()



```c
unsigned long Stream::getTimeout(void)
```

!!! note "戻り値"
	unsigned long



### find()



```c
bool Stream::find(char *target)
```

!!! summary "引数"
	- char * `target` 

!!! note "戻り値"
	bool



### find()



```c
bool Stream::find(uint8_t *target)
```

!!! summary "引数"
	- uint8_t * `target` 

!!! note "戻り値"
	bool



### find()



```c
bool Stream::find(char *target, size_t length)
```

!!! summary "引数"
	- char * `target` 
	- size_t `length` 

!!! note "戻り値"
	bool



### find()



```c
bool Stream::find(uint8_t *target, size_t length)
```

!!! summary "引数"
	- uint8_t * `target` 
	- size_t `length` 

!!! note "戻り値"
	bool



### find()



```c
bool Stream::find(char target)
```

!!! summary "引数"
	- char `target` 

!!! note "戻り値"
	bool



### findUntil()



```c
bool Stream::findUntil(char *target, char *terminator)
```

!!! summary "引数"
	- char * `target` 
	- char * `terminator` 

!!! note "戻り値"
	bool



### findUntil()



```c
bool Stream::findUntil(uint8_t *target, char *terminator)
```

!!! summary "引数"
	- uint8_t * `target` 
	- char * `terminator` 

!!! note "戻り値"
	bool



### findUntil()



```c
bool Stream::findUntil(char *target, size_t targetLen, char *terminate, size_t termLen)
```

!!! summary "引数"
	- char * `target` 
	- size_t `targetLen` 
	- char * `terminate` 
	- size_t `termLen` 

!!! note "戻り値"
	bool



### findUntil()



```c
bool Stream::findUntil(uint8_t *target, size_t targetLen, char *terminate, size_t termLen)
```

!!! summary "引数"
	- uint8_t * `target` 
	- size_t `targetLen` 
	- char * `terminate` 
	- size_t `termLen` 

!!! note "戻り値"
	bool



### parseInt()



```c
long Stream::parseInt(LookaheadMode lookahead=SKIP_ALL, char ignore=NO_IGNORE_CHAR)
```

!!! summary "引数"
	- LookaheadMode `lookahead` 
	- char `ignore` 

!!! note "戻り値"
	long



### parseFloat()



```c
float Stream::parseFloat(LookaheadMode lookahead=SKIP_ALL, char ignore=NO_IGNORE_CHAR)
```

!!! summary "引数"
	- LookaheadMode `lookahead` 
	- char `ignore` 

!!! note "戻り値"
	float



### readBytes()



```c
size_t Stream::readBytes(char *buffer, size_t length)
```

!!! summary "引数"
	- char * `buffer` 
	- size_t `length` 

!!! note "戻り値"
	size_t



### readBytes()



```c
size_t Stream::readBytes(uint8_t *buffer, size_t length)
```

!!! summary "引数"
	- uint8_t * `buffer` 
	- size_t `length` 

!!! note "戻り値"
	size_t



### readBytesUntil()



```c
size_t Stream::readBytesUntil(char terminator, char *buffer, size_t length)
```

!!! summary "引数"
	- char `terminator` 
	- char * `buffer` 
	- size_t `length` 

!!! note "戻り値"
	size_t



### readBytesUntil()



```c
size_t Stream::readBytesUntil(char terminator, uint8_t *buffer, size_t length)
```

!!! summary "引数"
	- char `terminator` 
	- uint8_t * `buffer` 
	- size_t `length` 

!!! note "戻り値"
	size_t



### readString()



```c
String Stream::readString()
```

!!! note "戻り値"
	String



### readStringUntil()



```c
String Stream::readStringUntil(char terminator)
```

!!! summary "引数"
	- char `terminator` 

!!! note "戻り値"
	String



