# asio::system_executor

An executor that uses arbitrary threads. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1system__executor.html)

## メンバー

### context()
Obtain the underlying execution context.


```c
system_context & asio::system_executor::context() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	system_context&



### on_work_started()
Inform the executor that it has some outstanding work to do.

For the system executor, this is a no-op. 
```c
void asio::system_executor::on_work_started() const ASIO_NOEXCEPT
```



### on_work_finished()
Inform the executor that some work is no longer outstanding.

For the system executor, this is a no-op. 
```c
void asio::system_executor::on_work_finished() const ASIO_NOEXCEPT
```



### dispatch()
Request the system executor to invoke the given function object.

This function is used to ask the executor to execute the given function object. The function object will always be executed inside this function.
```c
void asio::system_executor::dispatch(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### post()
Request the system executor to invoke the given function object.

This function is used to ask the executor to execute the given function object. The function object will never be executed inside this function. Instead, it will be scheduled to run on an unspecified system thread pool.
```c
void asio::system_executor::post(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### defer()
Request the system executor to invoke the given function object.

This function is used to ask the executor to execute the given function object. The function object will never be executed inside this function. Instead, it will be scheduled to run on an unspecified system thread pool.
```c
void asio::system_executor::defer(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 







