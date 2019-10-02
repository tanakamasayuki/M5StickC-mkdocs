# GSM3CircularBuffer



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_circular_buffer.html)

## メンバー

### GSM3CircularBuffer()



```c
GSM3CircularBuffer::GSM3CircularBuffer(GSM3CircularBufferManager *mgr=0)
```

!!! summary "引数"
	- GSM3CircularBufferManager* `mgr` Circular buffer manager 



### availableBytes()


Get available bytes in circular buffer 

```c
byte GSM3CircularBuffer::availableBytes()
```

!!! note "戻り値"
	byte available bytes 



### storedBytes()


Stored bytes in circular buffer 

```c
byte GSM3CircularBuffer::storedBytes()
```

!!! note "戻り値"
	byte stored bytes 



### write()



```c
int GSM3CircularBuffer::write(char c)
```

!!! summary "引数"
	- char `c` Character 

!!! note "戻り値"
	int 1 if successful 



### read()


Returns a character and moves the pointer 

```c
char GSM3CircularBuffer::read()
```

!!! note "戻り値"
	char character 



### peek()



```c
char GSM3CircularBuffer::peek(int increment)
```

!!! summary "引数"
	- int `increment` Increment 

!!! note "戻り値"
	char character 



### firstString()


Returns a pointer to the head of the buffer 

```c
char* GSM3CircularBuffer::firstString()
```

!!! note "戻り値"
	char * buffer with pointer in head 



### nextString()


Go forward one string 

```c
char * GSM3CircularBuffer::nextString()
```

!!! note "戻り値"
	char * buffer with one string advance 



### flush()


Flush circular buffer 
```c
void GSM3CircularBuffer::flush()
```



### getTail()


Get tail 

```c
byte GSM3CircularBuffer::getTail()
```

!!! note "戻り値"
	byte tail 



### getHead()


Get head 

```c
byte GSM3CircularBuffer::getHead()
```

!!! note "戻り値"
	byte head 



### deleteToTheEnd()



```c
void GSM3CircularBuffer::deleteToTheEnd(byte from)
```

!!! summary "引数"
	- byte `from` Initial byte position 



### locate()



```c
bool GSM3CircularBuffer::locate(const char *reference)
```

!!! summary "引数"
	- constchar * `reference` 

!!! note "戻り値"
	bool true if exists, in otherwise return false 



### chopUntil()



```c
bool GSM3CircularBuffer::chopUntil(const char *reference, bool movetotheend, bool head=true)
```

!!! summary "引数"
	- constchar * `reference` 
	- bool `movetotheend` 
	- bool `head` 

!!! note "戻り値"
	bool true if successful 



### readInt()


Reads an integer from the head. Stops with first non blank, non number character 

```c
int GSM3CircularBuffer::readInt()
```

!!! note "戻り値"
	int integer from the head 



### extractSubstring()



```c
bool GSM3CircularBuffer::extractSubstring(const char *from, const char *to, char *buffer, int bufsize)
```

!!! summary "引数"
	- constchar * `from` Initial byte position 
	- constchar * `to` Final byte position 
	- char * `buffer` Buffer for copy substring 
	- int `bufsize` Buffer size 

!!! note "戻り値"
	bool true if successful, false if substring does not exists 



### retrieveBuffer()



```c
bool GSM3CircularBuffer::retrieveBuffer(char *buffer, int bufsize, int &SizeWritten)
```

!!! summary "引数"
	- char * `buffer` 
	- int `bufsize` 
	- int & `SizeWritten` 

!!! note "戻り値"
	bool true if successful 



### debugBuffer()


Debug function to print the buffer after receiving data from the modem. 
```c
void GSM3CircularBuffer::debugBuffer()
```



### printCharDebug()



```c
void GSM3CircularBuffer::printCharDebug(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` Character 



