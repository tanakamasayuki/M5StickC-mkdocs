# cbuf



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classcbuf.html)

## メンバー

###  next

```c
cbuf* cbuf::next
```


### cbuf()



```c
cbuf::cbuf(size_t size)
```

!!! summary "引数"
	- size_t `size` 



### ~cbuf()



```c
cbuf::~cbuf()
```



### resizeAdd()



```c
size_t cbuf::resizeAdd(size_t addSize)
```

!!! summary "引数"
	- size_t `addSize` 

!!! note "戻り値"
	size_t



### resize()



```c
size_t cbuf::resize(size_t newSize)
```

!!! summary "引数"
	- size_t `newSize` 

!!! note "戻り値"
	size_t



### available()



```c
size_t cbuf::available() const
```

!!! note "戻り値"
	size_t



### size()



```c
size_t cbuf::size()
```

!!! note "戻り値"
	size_t



### room()



```c
size_t cbuf::room() const
```

!!! note "戻り値"
	size_t



### empty()



```c
bool cbuf::empty() const
```

!!! note "戻り値"
	bool



### full()



```c
bool cbuf::full() const
```

!!! note "戻り値"
	bool



### peek()



```c
int cbuf::peek()
```

!!! note "戻り値"
	int



### peek()



```c
size_t cbuf::peek(char *dst, size_t size)
```

!!! summary "引数"
	- char * `dst` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### read()



```c
int cbuf::read()
```

!!! note "戻り値"
	int



### read()



```c
size_t cbuf::read(char *dst, size_t size)
```

!!! summary "引数"
	- char * `dst` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### write()



```c
size_t cbuf::write(char c)
```

!!! summary "引数"
	- char `c` 

!!! note "戻り値"
	size_t



### write()



```c
size_t cbuf::write(const char *src, size_t size)
```

!!! summary "引数"
	- constchar * `src` 
	- size_t `size` 

!!! note "戻り値"
	size_t



### flush()



```c
void cbuf::flush()
```



### remove()



```c
size_t cbuf::remove(size_t size)
```

!!! summary "引数"
	- size_t `size` 

!!! note "戻り値"
	size_t



