# asio::detail::conditionally_enabled_event



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1conditionally__enabled__event.html)

## メンバー

### conditionally_enabled_event()



```c
asio::detail::conditionally_enabled_event::conditionally_enabled_event()
```



### ~conditionally_enabled_event()



```c
asio::detail::conditionally_enabled_event::~conditionally_enabled_event()
```



### signal()



```c
void asio::detail::conditionally_enabled_event::signal(conditionally_enabled_mutex::scoped_lock &lock)
```

!!! summary "引数"
	- conditionally_enabled_mutex::scoped_lock& `lock` 



### signal_all()



```c
void asio::detail::conditionally_enabled_event::signal_all(conditionally_enabled_mutex::scoped_lock &lock)
```

!!! summary "引数"
	- conditionally_enabled_mutex::scoped_lock& `lock` 



### unlock_and_signal_one()



```c
void asio::detail::conditionally_enabled_event::unlock_and_signal_one(conditionally_enabled_mutex::scoped_lock &lock)
```

!!! summary "引数"
	- conditionally_enabled_mutex::scoped_lock& `lock` 



### maybe_unlock_and_signal_one()



```c
bool asio::detail::conditionally_enabled_event::maybe_unlock_and_signal_one(conditionally_enabled_mutex::scoped_lock &lock)
```

!!! summary "引数"
	- conditionally_enabled_mutex::scoped_lock& `lock` 

!!! note "戻り値"
	bool



### clear()



```c
void asio::detail::conditionally_enabled_event::clear(conditionally_enabled_mutex::scoped_lock &lock)
```

!!! summary "引数"
	- conditionally_enabled_mutex::scoped_lock& `lock` 



### wait()



```c
void asio::detail::conditionally_enabled_event::wait(conditionally_enabled_mutex::scoped_lock &lock)
```

!!! summary "引数"
	- conditionally_enabled_mutex::scoped_lock& `lock` 



### wait_for_usec()



```c
bool asio::detail::conditionally_enabled_event::wait_for_usec(conditionally_enabled_mutex::scoped_lock &lock, long usec)
```

!!! summary "引数"
	- conditionally_enabled_mutex::scoped_lock& `lock` 
	- long `usec` 

!!! note "戻り値"
	bool



