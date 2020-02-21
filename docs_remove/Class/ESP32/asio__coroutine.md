# asio::coroutine

Provides support for implementing stackless coroutines. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1coroutine.html)

## メンバー



### coroutine()
Constructs a coroutine in its initial state.


```c
asio::coroutine::coroutine()
```



### is_child()
Returns true if the coroutine is the child of a fork.


```c
bool asio::coroutine::is_child() const
```

!!! note "戻り値"
	bool



### is_parent()
Returns true if the coroutine is the parent of a fork.


```c
bool asio::coroutine::is_parent() const
```

!!! note "戻り値"
	bool



### is_complete()
Returns true if the coroutine has reached its terminal state.


```c
bool asio::coroutine::is_complete() const
```

!!! note "戻り値"
	bool



