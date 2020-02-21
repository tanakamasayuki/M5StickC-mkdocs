# asio::strand

Provides serialised function invocation for any executor type. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1strand.html)

## メンバー



### strand()
Default constructor.

This constructor is only valid if the underlying executor type is default constructible. 
```c
asio::strand< Executor >::strand()
```



### strand()
Construct a strand for the specified executor.


```c
asio::strand< Executor >::strand(const Executor &e)
```

!!! summary "引数"
	- constExecutor & `e` 



### strand()
Copy constructor.


```c
asio::strand< Executor >::strand(const strand &other) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `other` 



### strand()
Converting constructor.

This constructor is only valid if the  type is convertible to . 
```c
asio::strand< Executor >::strand(const strand< OtherExecutor > &other) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const< OtherExecutor > & `other` 



### operator=()
Assignment operator.


```c
strand& asio::strand< Executor >::operator=(const strand &other) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	strand&



### operator=()
Converting assignment operator.

This assignment operator is only valid if the  type is convertible to . 
```c
strand& asio::strand< Executor >::operator=(const strand< OtherExecutor > &other) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const< OtherExecutor > & `other` 

!!! note "戻り値"
	strand&



### ~strand()
Destructor.


```c
asio::strand< Executor >::~strand()
```



### get_inner_executor()
Obtain the underlying executor.


```c
inner_executor_type asio::strand< Executor >::get_inner_executor() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	inner_executor_type



### context()
Obtain the underlying execution context.


```c
execution_context& asio::strand< Executor >::context() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	execution_context&



### on_work_started()
Inform the strand that it has some outstanding work to do.

The strand delegates this call to its underlying executor. 
```c
void asio::strand< Executor >::on_work_started() const ASIO_NOEXCEPT
```



### on_work_finished()
Inform the strand that some work is no longer outstanding.

The strand delegates this call to its underlying executor. 
```c
void asio::strand< Executor >::on_work_finished() const ASIO_NOEXCEPT
```



### dispatch()
Request the strand to invoke the given function object.

This function is used to ask the strand to execute the given function object on its underlying executor. The function object will be executed inside this function if the strand is not otherwise busy and if the underlying executor's  function is also able to execute the function before returning.
```c
void asio::strand< Executor >::dispatch(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### post()
Request the strand to invoke the given function object.

This function is used to ask the executor to execute the given function object. The function object will never be executed inside this function. Instead, it will be scheduled by the underlying executor's defer function.
```c
void asio::strand< Executor >::post(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### defer()
Request the strand to invoke the given function object.

This function is used to ask the executor to execute the given function object. The function object will never be executed inside this function. Instead, it will be scheduled by the underlying executor's defer function.
```c
void asio::strand< Executor >::defer(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### running_in_this_thread()
Determine whether the strand is running in the current thread.



```c
bool asio::strand< Executor >::running_in_this_thread() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	bool  if the current thread is executing a function that was submitted to the strand using ,  or . Otherwise returns . 







