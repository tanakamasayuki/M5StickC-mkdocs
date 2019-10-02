# asio::detail::scheduler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1scheduler.html)

## メンバー



### scheduler()



```c
ASIO_DECL asio::detail::scheduler::scheduler(asio::execution_context &ctx, int concurrency_hint=0)
```

!!! summary "引数"
	- asio::execution_context& `ctx` 
	- int `concurrency_hint` 

!!! note "戻り値"
	ASIO_DECL



### shutdown()
Destroy all user-defined handler objects owned by the service.


```c
ASIO_DECL void asio::detail::scheduler::shutdown()
```

!!! note "戻り値"
	ASIO_DECLvoid



### init_task()



```c
ASIO_DECL void asio::detail::scheduler::init_task()
```

!!! note "戻り値"
	ASIO_DECLvoid



### run()



```c
ASIO_DECL std::size_t asio::detail::scheduler::run(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECLstd::size_t



### run_one()



```c
ASIO_DECL std::size_t asio::detail::scheduler::run_one(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECLstd::size_t



### wait_one()



```c
ASIO_DECL std::size_t asio::detail::scheduler::wait_one(long usec, asio::error_code &ec)
```

!!! summary "引数"
	- long `usec` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECLstd::size_t



### poll()



```c
ASIO_DECL std::size_t asio::detail::scheduler::poll(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECLstd::size_t



### poll_one()



```c
ASIO_DECL std::size_t asio::detail::scheduler::poll_one(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECLstd::size_t



### stop()



```c
ASIO_DECL void asio::detail::scheduler::stop()
```

!!! note "戻り値"
	ASIO_DECLvoid



### stopped()



```c
ASIO_DECL bool asio::detail::scheduler::stopped() const
```

!!! note "戻り値"
	ASIO_DECL



### restart()



```c
ASIO_DECL void asio::detail::scheduler::restart()
```

!!! note "戻り値"
	ASIO_DECLvoid



### work_started()



```c
void asio::detail::scheduler::work_started()
```



### compensating_work_started()



```c
ASIO_DECL void asio::detail::scheduler::compensating_work_started()
```

!!! note "戻り値"
	ASIO_DECLvoid



### work_finished()



```c
void asio::detail::scheduler::work_finished()
```



### can_dispatch()



```c
bool asio::detail::scheduler::can_dispatch()
```

!!! note "戻り値"
	bool



### post_immediate_completion()



```c
ASIO_DECL void asio::detail::scheduler::post_immediate_completion(operation *op, bool is_continuation)
```

!!! summary "引数"
	- operation* `op` 
	- bool `is_continuation` 

!!! note "戻り値"
	ASIO_DECLvoid



### post_deferred_completion()



```c
ASIO_DECL void asio::detail::scheduler::post_deferred_completion(operation *op)
```

!!! summary "引数"
	- operation* `op` 

!!! note "戻り値"
	ASIO_DECLvoid



### post_deferred_completions()



```c
ASIO_DECL void asio::detail::scheduler::post_deferred_completions(op_queue< operation > &ops)
```

!!! summary "引数"
	- op_queue<  > & `ops` 

!!! note "戻り値"
	ASIO_DECLvoid



### do_dispatch()



```c
ASIO_DECL void asio::detail::scheduler::do_dispatch(operation *op)
```

!!! summary "引数"
	- operation* `op` 

!!! note "戻り値"
	ASIO_DECLvoid



### abandon_operations()



```c
ASIO_DECL void asio::detail::scheduler::abandon_operations(op_queue< operation > &ops)
```

!!! summary "引数"
	- op_queue<  > & `ops` 

!!! note "戻り値"
	ASIO_DECLvoid



### concurrency_hint()



```c
int asio::detail::scheduler::concurrency_hint() const
```

!!! note "戻り値"
	int



