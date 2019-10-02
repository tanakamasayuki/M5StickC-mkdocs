# asio::io_context::strand

Provides serialised handler execution. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1io__context_1_1strand.html)

## メンバー

### strand()
Constructor.

Constructs the strand.
```c
asio::io_context::strand::strand(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### ~strand()
Destructor.

Handlers posted through the strand that have not yet been invoked will still be dispatched in a way that meets the guarantee of non-concurrency. 
```c
asio::io_context::strand::~strand()
```



### get_io_context()




```c
asio::io_context& asio::io_context::strand::get_io_context()
```

!!! note "戻り値"
	asio::io_context&



### get_io_service()




```c
asio::io_context& asio::io_context::strand::get_io_service()
```

!!! note "戻り値"
	asio::io_context&



### context()
Obtain the underlying execution context.


```c
asio::io_context& asio::io_context::strand::context() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	asio::io_context&



### on_work_started()
Inform the strand that it has some outstanding work to do.

The strand delegates this call to its underlying . 
```c
void asio::io_context::strand::on_work_started() const ASIO_NOEXCEPT
```



### on_work_finished()
Inform the strand that some work is no longer outstanding.

The strand delegates this call to its underlying . 
```c
void asio::io_context::strand::on_work_finished() const ASIO_NOEXCEPT
```



### dispatch()
Request the strand to invoke the given function object.

This function is used to ask the strand to execute the given function object on its underlying . The function object will be executed inside this function if the strand is not otherwise busy and if the underlying 's executor's  function is also able to execute the function before returning.
```c
void asio::io_context::strand::dispatch(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### dispatch()


The strand's guarantee is in addition to the guarantee provided by the underlying . The  guarantees that the handler will only be called in a thread in which the 's run member function is currently being invoked.
```c
asio::io_context::strand::dispatch(ASIO_MOVE_ARG(LegacyCompletionHandler) handler)
```

!!! summary "引数"
	- ASIO_MOVE_ARG(LegacyCompletionHandler) `handler` The handler to be called. The strand will make a copy of the handler object as required. The function signature of the handler must be:  



### post()
Request the strand to invoke the given function object.

This function is used to ask the executor to execute the given function object. The function object will never be executed inside this function. Instead, it will be scheduled to run by the underlying .
```c
void asio::io_context::strand::post(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### post()


The strand object guarantees that handlers posted or dispatched through the strand will not be executed concurrently. The strand's guarantee is in addition to the guarantee provided by the underlying . The  guarantees that the handler will only be called in a thread in which the 's run member function is currently being invoked.
```c
asio::io_context::strand::post(ASIO_MOVE_ARG(LegacyCompletionHandler) handler)
```

!!! summary "引数"
	- ASIO_MOVE_ARG(LegacyCompletionHandler) `handler` The handler to be called. The strand will make a copy of the handler object as required. The function signature of the handler must be:  



### defer()
Request the strand to invoke the given function object.

This function is used to ask the executor to execute the given function object. The function object will never be executed inside this function. Instead, it will be scheduled to run by the underlying .
```c
void asio::io_context::strand::defer(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### wrap()


(Deprecated: Use .) Create a new handler that automatically dispatches the wrapped handler on the strand. This function is used to create a new handler function object that, when invoked, will automatically pass the wrapped handler to the strand's dispatch function.
```c
detail::wrapped_handler<strand, Handler, detail::is_continuation_if_running> asio::io_context::strand::wrap(Handler handler)
```

!!! summary "引数"
	- Handler `handler` The handler to be wrapped. The strand will make a copy of the handler object as required. The function signature of the handler must be:

!!! note "戻り値"
	detail::wrapped_handler< , Handler,  >



### running_in_this_thread()
Determine whether the strand is running in the current thread.



```c
bool asio::io_context::strand::running_in_this_thread() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	bool  if the current thread is executing a handler that was submitted to the strand using ,  or . Otherwise returns . 







