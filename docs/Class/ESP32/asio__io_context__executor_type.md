# asio::io_context::executor_type

Executor used to submit functions to an . 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1io__context_1_1executor__type.html)

## メンバー





### context()
Obtain the underlying execution context.


```c
io_context & asio::io_context::executor_type::context() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	io_context&



### on_work_started()
Inform the  that it has some outstanding work to do.

This function is used to inform the  that some work has begun. This ensures that the 's  and  functions do not exit while the work is underway. 
```c
void asio::io_context::executor_type::on_work_started() const ASIO_NOEXCEPT
```



### on_work_finished()
Inform the  that some work is no longer outstanding.

This function is used to inform the  that some work has finished. Once the count of unfinished work reaches zero, the  is stopped and the  and  functions may exit. 
```c
void asio::io_context::executor_type::on_work_finished() const ASIO_NOEXCEPT
```



### dispatch()
Request the  to invoke the given function object.

This function is used to ask the  to execute the given function object. If the current thread is running the ,  executes the function before returning. Otherwise, the function will be scheduled to run on the .
```c
void asio::io_context::executor_type::dispatch(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### post()
Request the  to invoke the given function object.

This function is used to ask the  to execute the given function object. The function object will never be executed inside . Instead, it will be scheduled to run on the .
```c
void asio::io_context::executor_type::post(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### defer()
Request the  to invoke the given function object.

If the current thread belongs to the ,  will delay scheduling the function object until the current thread returns control to the pool.
```c
void asio::io_context::executor_type::defer(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### running_in_this_thread()
Determine whether the  is running in the current thread.



```c
bool asio::io_context::executor_type::running_in_this_thread() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	bool  if the current thread is running the . Otherwise returns . 



