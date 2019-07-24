# ConsoleClass



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_console_class.html)

## メンバー

### ConsoleClass()



```c
ConsoleClass::ConsoleClass()
```



### ConsoleClass()



```c
ConsoleClass::ConsoleClass(BridgeClass &_b)
```

!!! summary "引数"
	- BridgeClass& `_b` 



### ~ConsoleClass()



```c
ConsoleClass::~ConsoleClass()
```



### begin()



```c
void ConsoleClass::begin()
```



### end()



```c
void ConsoleClass::end()
```



### buffer()



```c
void ConsoleClass::buffer(uint8_t size)
```

!!! summary "引数"
	- uint8_t `size` 



### noBuffer()



```c
void ConsoleClass::noBuffer()
```



### connected()



```c
bool ConsoleClass::connected()
```

!!! note "戻り値"
	bool



### available()



```c
int ConsoleClass::available()
```

!!! note "戻り値"
	int



### read()



```c
int ConsoleClass::read()
```

!!! note "戻り値"
	int



### peek()



```c
int ConsoleClass::peek()
```

!!! note "戻り値"
	int



### write()



```c
size_t ConsoleClass::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t ConsoleClass::write(const uint8_t *buffer, size_t size)
```

!!! summary "引数"
	- constuint8_t * `buffer` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### flush()



```c
void ConsoleClass::flush()
```



### operator bool()



```c
ConsoleClass::operator bool()
```



