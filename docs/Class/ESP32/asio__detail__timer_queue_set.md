# asio::detail::timer_queue_set



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1timer__queue__set.html)

## メンバー

### timer_queue_set()



```c
ASIO_DECL asio::detail::timer_queue_set::timer_queue_set()
```

!!! note "戻り値"
	ASIO_DECL



### insert()



```c
ASIO_DECL void asio::detail::timer_queue_set::insert(timer_queue_base *q)
```

!!! summary "引数"
	- timer_queue_base* `q` 

!!! note "戻り値"
	ASIO_DECLvoid



### erase()



```c
ASIO_DECL void asio::detail::timer_queue_set::erase(timer_queue_base *q)
```

!!! summary "引数"
	- timer_queue_base* `q` 

!!! note "戻り値"
	ASIO_DECLvoid



### all_empty()



```c
ASIO_DECL bool asio::detail::timer_queue_set::all_empty() const
```

!!! note "戻り値"
	ASIO_DECL



### wait_duration_msec()



```c
ASIO_DECL long asio::detail::timer_queue_set::wait_duration_msec(long max_duration) const
```

!!! summary "引数"
	- long `max_duration` 

!!! note "戻り値"
	ASIO_DECLlong



### wait_duration_usec()



```c
ASIO_DECL long asio::detail::timer_queue_set::wait_duration_usec(long max_duration) const
```

!!! summary "引数"
	- long `max_duration` 

!!! note "戻り値"
	ASIO_DECLlong



### get_ready_timers()



```c
ASIO_DECL void asio::detail::timer_queue_set::get_ready_timers(op_queue< operation > &ops)
```

!!! summary "引数"
	- op_queue<  > & `ops` 

!!! note "戻り値"
	ASIO_DECLvoid



### get_all_timers()



```c
ASIO_DECL void asio::detail::timer_queue_set::get_all_timers(op_queue< operation > &ops)
```

!!! summary "引数"
	- op_queue<  > & `ops` 

!!! note "戻り値"
	ASIO_DECLvoid



