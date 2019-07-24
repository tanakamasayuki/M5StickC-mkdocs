# Print



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_print.html)

## メンバー

### Print()



```c
Print::Print()
```



### getWriteError()



```c
int Print::getWriteError()
```

!!! note "戻り値"
	int



### clearWriteError()



```c
void Print::clearWriteError()
```



### write()



```c
virtual size_t Print::write(uint8_t)=0
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### write()



```c
size_t Print::write(const char *str)
```

!!! summary "引数"
	- constchar * `str` 

!!! note "戻り値"
	size_t



### write()



```c
size_t Print::write(const uint8_t *buffer, size_t size)
```

!!! summary "引数"
	- constuint8_t * `buffer` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### write()



```c
size_t Print::write(const char *buffer, size_t size)
```

!!! summary "引数"
	- constchar * `buffer` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### availableForWrite()



```c
virtual int Print::availableForWrite()
```

!!! note "戻り値"
	int



### print()



```c
size_t Print::print(const __FlashStringHelper *)
```

!!! summary "引数"
	- const__FlashStringHelper * `` 

!!! note "戻り値"
	size_t



### print()



```c
size_t Print::print(const String &)
```

!!! summary "引数"
	- constString & `` 

!!! note "戻り値"
	size_t



### print()



```c
size_t Print::print(const char[])
```

!!! summary "引数"
	- constchar `` 

!!! note "戻り値"
	size_t



### print()



```c
size_t Print::print(char)
```

!!! summary "引数"
	- char `` 

!!! note "戻り値"
	size_t



### print()



```c
size_t Print::print(unsigned char, int=DEC)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	size_t



### print()



```c
size_t Print::print(int, int=DEC)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	size_t



### print()



```c
size_t Print::print(unsigned int, int=DEC)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	size_t



### print()



```c
size_t Print::print(long, int=DEC)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	size_t



### print()



```c
size_t Print::print(unsigned long, int=DEC)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	size_t



### print()



```c
size_t Print::print(double, int=2)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	size_t



### print()



```c
size_t Print::print(const Printable &)
```

!!! summary "引数"
	- const& `` 

!!! note "戻り値"
	size_t



### println()



```c
size_t Print::println(const __FlashStringHelper *)
```

!!! summary "引数"
	- const__FlashStringHelper * `` 

!!! note "戻り値"
	size_t



### println()



```c
size_t Print::println(const String &s)
```

!!! summary "引数"
	- constString & `s` 

!!! note "戻り値"
	size_t



### println()



```c
size_t Print::println(const char[])
```

!!! summary "引数"
	- constchar `` 

!!! note "戻り値"
	size_t



### println()



```c
size_t Print::println(char)
```

!!! summary "引数"
	- char `` 

!!! note "戻り値"
	size_t



### println()



```c
size_t Print::println(unsigned char, int=DEC)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	size_t



### println()



```c
size_t Print::println(int, int=DEC)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	size_t



### println()



```c
size_t Print::println(unsigned int, int=DEC)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	size_t



### println()



```c
size_t Print::println(long, int=DEC)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	size_t



### println()



```c
size_t Print::println(unsigned long, int=DEC)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	size_t



### println()



```c
size_t Print::println(double, int=2)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	size_t



### println()



```c
size_t Print::println(const Printable &)
```

!!! summary "引数"
	- const& `` 

!!! note "戻り値"
	size_t



### println()



```c
size_t Print::println(void)
```

!!! note "戻り値"
	size_t



### flush()



```c
virtual void Print::flush()
```



