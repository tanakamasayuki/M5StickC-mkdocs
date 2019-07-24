# Ticker



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_ticker.html)

## メンバー





### Ticker()



```c
Ticker::Ticker()
```



### ~Ticker()



```c
Ticker::~Ticker()
```



### attach()



```c
void Ticker::attach(float seconds, callback_t callback)
```

!!! summary "引数"
	- float `seconds` 
	- callback_t `callback` 



### attach_ms()



```c
void Ticker::attach_ms(uint32_t milliseconds, callback_t callback)
```

!!! summary "引数"
	- uint32_t `milliseconds` 
	- callback_t `callback` 



### attach()



```c
void Ticker::attach(float seconds, void(*callback)(TArg), TArg arg)
```

!!! summary "引数"
	- float `seconds` 
	- void(*)(TArg) `callback` 
	- TArg `arg` 



### attach_ms()



```c
void Ticker::attach_ms(uint32_t milliseconds, void(*callback)(TArg), TArg arg)
```

!!! summary "引数"
	- uint32_t `milliseconds` 
	- void(*)(TArg) `callback` 
	- TArg `arg` 



### once()



```c
void Ticker::once(float seconds, callback_t callback)
```

!!! summary "引数"
	- float `seconds` 
	- callback_t `callback` 



### once_ms()



```c
void Ticker::once_ms(uint32_t milliseconds, callback_t callback)
```

!!! summary "引数"
	- uint32_t `milliseconds` 
	- callback_t `callback` 



### once()



```c
void Ticker::once(float seconds, void(*callback)(TArg), TArg arg)
```

!!! summary "引数"
	- float `seconds` 
	- void(*)(TArg) `callback` 
	- TArg `arg` 



### once_ms()



```c
void Ticker::once_ms(uint32_t milliseconds, void(*callback)(TArg), TArg arg)
```

!!! summary "引数"
	- uint32_t `milliseconds` 
	- void(*)(TArg) `callback` 
	- TArg `arg` 



### detach()



```c
void Ticker::detach()
```



### active()



```c
bool Ticker::active()
```

!!! note "戻り値"
	bool



