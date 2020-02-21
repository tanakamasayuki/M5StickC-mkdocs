# asio::detail::null_event



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1null__event.html)

## メンバー

### null_event()



```c
asio::detail::null_event::null_event()
```



### ~null_event()



```c
asio::detail::null_event::~null_event()
```



### signal()



```c
void asio::detail::null_event::signal(Lock &)
```

!!! summary "引数"
	- Lock& `` 



### signal_all()



```c
void asio::detail::null_event::signal_all(Lock &)
```

!!! summary "引数"
	- Lock& `` 



### unlock_and_signal_one()



```c
void asio::detail::null_event::unlock_and_signal_one(Lock &)
```

!!! summary "引数"
	- Lock& `` 



### maybe_unlock_and_signal_one()



```c
bool asio::detail::null_event::maybe_unlock_and_signal_one(Lock &)
```

!!! summary "引数"
	- Lock& `` 

!!! note "戻り値"
	bool



### clear()



```c
void asio::detail::null_event::clear(Lock &)
```

!!! summary "引数"
	- Lock& `` 



### wait()



```c
void asio::detail::null_event::wait(Lock &)
```

!!! summary "引数"
	- Lock& `` 



### wait_for_usec()



```c
bool asio::detail::null_event::wait_for_usec(Lock &, long usec)
```

!!! summary "引数"
	- Lock& `` 
	- long `usec` 

!!! note "戻り値"
	bool



