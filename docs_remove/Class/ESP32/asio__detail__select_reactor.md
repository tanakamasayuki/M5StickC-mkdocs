# asio::detail::select_reactor



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1select__reactor.html)

## メンバー



### select_reactor()



```c
ASIO_DECL asio::detail::select_reactor::select_reactor(asio::execution_context &ctx)
```

!!! summary "引数"
	- asio::execution_context& `ctx` 

!!! note "戻り値"
	ASIO_DECL



### ~select_reactor()



```c
ASIO_DECL asio::detail::select_reactor::~select_reactor()
```

!!! note "戻り値"
	ASIO_DECL



### shutdown()
Destroy all user-defined handler objects owned by the service.


```c
ASIO_DECL void asio::detail::select_reactor::shutdown()
```

!!! note "戻り値"
	ASIO_DECLvoid



### notify_fork()


Handle notification of a fork-related event to perform any necessary housekeeping. This function is not a pure virtual so that services only have to implement it if necessary. The default implementation does nothing. 
```c
ASIO_DECL void asio::detail::select_reactor::notify_fork(asio::execution_context::fork_event fork_ev)
```

!!! summary "引数"
	- asio::execution_context::fork_event `event` 

!!! note "戻り値"
	ASIO_DECLvoid



### init_task()



```c
ASIO_DECL void asio::detail::select_reactor::init_task()
```

!!! note "戻り値"
	ASIO_DECLvoid



### register_descriptor()



```c
ASIO_DECL int asio::detail::select_reactor::register_descriptor(socket_type, per_descriptor_data &)
```

!!! summary "引数"
	- per_descriptor_data& `` 

!!! note "戻り値"
	ASIO_DECLint



### register_internal_descriptor()



```c
ASIO_DECL int asio::detail::select_reactor::register_internal_descriptor(int op_type, socket_type descriptor, per_descriptor_data &descriptor_data, reactor_op *op)
```

!!! summary "引数"
	- int `op_type` 
	- socket_type `descriptor` 
	- per_descriptor_data& `descriptor_data` 
	- reactor_op* `op` 

!!! note "戻り値"
	ASIO_DECLint



### post_immediate_completion()



```c
void asio::detail::select_reactor::post_immediate_completion(reactor_op *op, bool is_continuation)
```

!!! summary "引数"
	- reactor_op* `op` 
	- bool `is_continuation` 



### start_op()



```c
ASIO_DECL void asio::detail::select_reactor::start_op(int op_type, socket_type descriptor, per_descriptor_data &, reactor_op *op, bool is_continuation, bool)
```

!!! summary "引数"
	- int `op_type` 
	- socket_type `descriptor` 
	- bool `` 
	- reactor_op* `op` 
	- bool `is_continuation` 

!!! note "戻り値"
	ASIO_DECLvoid



### cancel_ops()



```c
ASIO_DECL void asio::detail::select_reactor::cancel_ops(socket_type descriptor, per_descriptor_data &)
```

!!! summary "引数"
	- socket_type `descriptor` 
	- per_descriptor_data& `` 

!!! note "戻り値"
	ASIO_DECLvoid



### deregister_descriptor()



```c
ASIO_DECL void asio::detail::select_reactor::deregister_descriptor(socket_type descriptor, per_descriptor_data &, bool closing)
```

!!! summary "引数"
	- socket_type `descriptor` 
	- per_descriptor_data& `` 
	- bool `closing` 

!!! note "戻り値"
	ASIO_DECLvoid



### deregister_internal_descriptor()



```c
ASIO_DECL void asio::detail::select_reactor::deregister_internal_descriptor(socket_type descriptor, per_descriptor_data &)
```

!!! summary "引数"
	- socket_type `descriptor` 
	- per_descriptor_data& `` 

!!! note "戻り値"
	ASIO_DECLvoid



### cleanup_descriptor_data()



```c
ASIO_DECL void asio::detail::select_reactor::cleanup_descriptor_data(per_descriptor_data &)
```

!!! summary "引数"
	- per_descriptor_data& `` 

!!! note "戻り値"
	ASIO_DECLvoid



### move_descriptor()



```c
ASIO_DECL void asio::detail::select_reactor::move_descriptor(socket_type descriptor, per_descriptor_data &target_descriptor_data, per_descriptor_data &source_descriptor_data)
```

!!! summary "引数"
	- socket_type `descriptor` 
	- per_descriptor_data& `target_descriptor_data` 
	- per_descriptor_data& `source_descriptor_data` 

!!! note "戻り値"
	ASIO_DECLvoid



### add_timer_queue()



```c
void asio::detail::select_reactor::add_timer_queue(timer_queue< Time_Traits > &queue)
```

!!! summary "引数"
	- timer_queue< Time_Traits > & `queue` 



### remove_timer_queue()



```c
void asio::detail::select_reactor::remove_timer_queue(timer_queue< Time_Traits > &queue)
```

!!! summary "引数"
	- timer_queue< Time_Traits > & `queue` 



### schedule_timer()



```c
void asio::detail::select_reactor::schedule_timer(timer_queue< Time_Traits > &queue, const typename Time_Traits::time_type &time, typename timer_queue< Time_Traits >::per_timer_data &timer, wait_op *op)
```

!!! summary "引数"
	- timer_queue< Time_Traits > & `queue` 
	- consttypename Time_Traits::time_type & `time` 
	- timer_queuetypename < Time_Traits >::per_timer_data & `timer` 
	- wait_op* `op` 



### cancel_timer()



```c
std::size_t asio::detail::select_reactor::cancel_timer(timer_queue< Time_Traits > &queue, typename timer_queue< Time_Traits >::per_timer_data &timer, std::size_t max_cancelled=(std::numeric_limits< std::size_t >::max)())
```

!!! summary "引数"
	- timer_queue< Time_Traits > & `queue` 
	- timer_queuetypename < Time_Traits >::per_timer_data & `timer` 
	- std::size_t `max_cancelled` 

!!! note "戻り値"
	std::size_t



### move_timer()



```c
void asio::detail::select_reactor::move_timer(timer_queue< Time_Traits > &queue, typename timer_queue< Time_Traits >::per_timer_data &target, typename timer_queue< Time_Traits >::per_timer_data &source)
```

!!! summary "引数"
	- timer_queue< Time_Traits > & `queue` 
	- timer_queuetypename < Time_Traits >::per_timer_data & `target` 
	- timer_queuetypename < Time_Traits >::per_timer_data & `source` 



### run()



```c
ASIO_DECL void asio::detail::select_reactor::run(long usec, op_queue< operation > &ops)
```

!!! summary "引数"
	- long `usec` 
	- op_queue<  > & `ops` 

!!! note "戻り値"
	ASIO_DECLvoid



### interrupt()



```c
ASIO_DECL void asio::detail::select_reactor::interrupt()
```

!!! note "戻り値"
	ASIO_DECLvoid



