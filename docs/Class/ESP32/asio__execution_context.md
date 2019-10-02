# asio::execution_context

A context for function object execution. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1execution__context.html)

## メンバー



### notify_fork()
Notify the  of a fork-related event.

This function must not be called while any other  function, or any function associated with the 's derived class, is being called in another thread. It is, however, safe to call this function from within a completion handler, provided no other thread is accessing the  or its derived class.
```c
ASIO_DECL void asio::execution_context::notify_fork(fork_event event)
```

!!! summary "引数"
	- fork_event `event` A fork-related event.

!!! note "戻り値"
	ASIO_DECLvoid













