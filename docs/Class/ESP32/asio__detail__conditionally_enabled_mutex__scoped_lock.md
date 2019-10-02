# asio::detail::conditionally_enabled_mutex::scoped_lock



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1conditionally__enabled__mutex_1_1scoped__lock.html)

## メンバー



### scoped_lock()



```c
asio::detail::conditionally_enabled_mutex::scoped_lock::scoped_lock(conditionally_enabled_mutex &m, adopt_lock_t)
```

!!! summary "引数"
	- conditionally_enabled_mutex& `m` 
	- adopt_lock_t `` 



### scoped_lock()



```c
asio::detail::conditionally_enabled_mutex::scoped_lock::scoped_lock(conditionally_enabled_mutex &m)
```

!!! summary "引数"
	- conditionally_enabled_mutex& `m` 



### ~scoped_lock()



```c
asio::detail::conditionally_enabled_mutex::scoped_lock::~scoped_lock()
```



### lock()



```c
void asio::detail::conditionally_enabled_mutex::scoped_lock::lock()
```



### unlock()



```c
void asio::detail::conditionally_enabled_mutex::scoped_lock::unlock()
```



### locked()



```c
bool asio::detail::conditionally_enabled_mutex::scoped_lock::locked() const
```

!!! note "戻り値"
	bool



### mutex()



```c
asio::detail::mutex& asio::detail::conditionally_enabled_mutex::scoped_lock::mutex()
```

!!! note "戻り値"
	asio::detail::mutex&



