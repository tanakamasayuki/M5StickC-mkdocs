# asio::detail::timer_queue_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1timer__queue__base.html)

## メンバー

### timer_queue_base()



```c
asio::detail::timer_queue_base::timer_queue_base()
```



### ~timer_queue_base()



```c
virtual asio::detail::timer_queue_base::~timer_queue_base()
```



### empty()



```c
virtual bool asio::detail::timer_queue_base::empty() const =0
```

!!! note "戻り値"
	bool



### wait_duration_msec()



```c
virtual long asio::detail::timer_queue_base::wait_duration_msec(long max_duration) const =0
```

!!! summary "引数"
	- long `max_duration` 

!!! note "戻り値"
	long



### wait_duration_usec()



```c
virtual long asio::detail::timer_queue_base::wait_duration_usec(long max_duration) const =0
```

!!! summary "引数"
	- long `max_duration` 

!!! note "戻り値"
	long



### get_ready_timers()



```c
virtual void asio::detail::timer_queue_base::get_ready_timers(op_queue< operation > &ops)=0
```

!!! summary "引数"
	- op_queue<  > & `ops` 



### get_all_timers()



```c
virtual void asio::detail::timer_queue_base::get_all_timers(op_queue< operation > &ops)=0
```

!!! summary "引数"
	- op_queue<  > & `ops` 



