# asio::detail::timer_queue



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1timer__queue.html)

## メンバー





### timer_queue()



```c
asio::detail::timer_queue< Time_Traits >::timer_queue()
```



### enqueue_timer()



```c
bool asio::detail::timer_queue< Time_Traits >::enqueue_timer(const time_type &time, per_timer_data &timer, wait_op *op)
```

!!! summary "引数"
	- const& `time` 
	- per_timer_data& `timer` 
	- wait_op* `op` 

!!! note "戻り値"
	bool



### empty()



```c
virtual bool asio::detail::timer_queue< Time_Traits >::empty() const
```

!!! note "戻り値"
	bool



### wait_duration_msec()



```c
virtual long asio::detail::timer_queue< Time_Traits >::wait_duration_msec(long max_duration) const
```

!!! summary "引数"
	- long `max_duration` 

!!! note "戻り値"
	long



### wait_duration_usec()



```c
virtual long asio::detail::timer_queue< Time_Traits >::wait_duration_usec(long max_duration) const
```

!!! summary "引数"
	- long `max_duration` 

!!! note "戻り値"
	long



### get_ready_timers()



```c
virtual void asio::detail::timer_queue< Time_Traits >::get_ready_timers(op_queue< operation > &ops)
```

!!! summary "引数"
	- op_queue<  > & `ops` 



### get_all_timers()



```c
virtual void asio::detail::timer_queue< Time_Traits >::get_all_timers(op_queue< operation > &ops)
```

!!! summary "引数"
	- op_queue<  > & `ops` 



### cancel_timer()



```c
std::size_t asio::detail::timer_queue< Time_Traits >::cancel_timer(per_timer_data &timer, op_queue< operation > &ops, std::size_t max_cancelled=(std::numeric_limits< std::size_t >::max)())
```

!!! summary "引数"
	- per_timer_data& `timer` 
	- op_queue<  > & `ops` 
	- std::size_t `max_cancelled` 

!!! note "戻り値"
	std::size_t



### move_timer()



```c
void asio::detail::timer_queue< Time_Traits >::move_timer(per_timer_data &target, per_timer_data &source)
```

!!! summary "引数"
	- per_timer_data& `target` 
	- per_timer_data& `source` 



