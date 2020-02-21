# タイマー(Ticker)

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_ticker.html)

## メンバー

### コンストラクタ Ticker()

```c
Ticker::Ticker()
```



### デストラクタ ~Ticker()

```c
Ticker::~Ticker()
```



### タイマー追加 attach()


```c
void Ticker::attach(float seconds, callback_t callback)
```

!!! summary "引数"
	- float `seconds` 秒
	- callback_t `callback` コールバック関数



### attach_ms()



```c
void Ticker::attach_ms(uint32_t milliseconds, callback_t callback)
```

!!! summary "引数"
	- uint32_t `milliseconds` ミリ秒
	- callback_t `callback` コールバック関数 



### attach()



```c
void Ticker::attach(float seconds, void(*callback)(TArg), TArg arg)
```

!!! summary "引数"
	- float `seconds` 秒 秒
	- void(*)(TArg) `callback` コールバック関数コールバック関数
	- TArg `arg` コールバック関数の引数



### attach_ms()



```c
void Ticker::attach_ms(uint32_t milliseconds, void(*callback)(TArg), TArg arg)
```

!!! summary "引数"
	- uint32_t `milliseconds` ミリ秒
	- void(*)(TArg) `callback` コールバック関数
	- TArg `arg` コールバック関数の引数



### once()



```c
void Ticker::once(float seconds, callback_t callback)
```

!!! summary "引数"
	- float `seconds` 秒 
	- callback_t `callback` コールバック関数 



### once_ms()



```c
void Ticker::once_ms(uint32_t milliseconds, callback_t callback)
```

!!! summary "引数"
	- uint32_t `milliseconds` ミリ秒
	- callback_t `callback` コールバック関数 



### once()



```c
void Ticker::once(float seconds, void(*callback)(TArg), TArg arg)
```

!!! summary "引数"
	- float `seconds` 秒 
	- void(*)(TArg) `callback` コールバック関数
	- TArg `arg` コールバック関数の引数



### once_ms()



```c
void Ticker::once_ms(uint32_t milliseconds, void(*callback)(TArg), TArg arg)
```

!!! summary "引数"
	- uint32_t `milliseconds` ミリ秒
	- void(*)(TArg) `callback` コールバック関数
	- TArg `arg` コールバック関数の引数



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



