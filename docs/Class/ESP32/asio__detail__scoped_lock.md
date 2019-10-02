# asio::detail::scoped_lock



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1scoped__lock.html)

## メンバー



### scoped_lock()



```c
asio::detail::scoped_lock< Mutex >::scoped_lock(Mutex &m, adopt_lock_t)
```

!!! summary "引数"
	- Mutex & `m` 
	- adopt_lock_t `` 



### scoped_lock()



```c
asio::detail::scoped_lock< Mutex >::scoped_lock(Mutex &m)
```

!!! summary "引数"
	- Mutex & `m` 



### ~scoped_lock()



```c
asio::detail::scoped_lock< Mutex >::~scoped_lock()
```



### lock()



```c
void asio::detail::scoped_lock< Mutex >::lock()
```



### unlock()



```c
void asio::detail::scoped_lock< Mutex >::unlock()
```



### locked()



```c
bool asio::detail::scoped_lock< Mutex >::locked() const
```

!!! note "戻り値"
	bool



### mutex()



```c
Mutex& asio::detail::scoped_lock< Mutex >::mutex()
```

!!! note "戻り値"
	Mutex &



