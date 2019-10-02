# asio::io_context

Provides core I/O functionality. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1io__context.html)

## メンバー







### io_context()
Constructor.


```c
ASIO_DECL asio::io_context::io_context()
```

!!! note "戻り値"
	ASIO_DECL



### io_context()
Constructor.

Construct with a hint about the required level of concurrency.
```c
ASIO_DECL asio::io_context::io_context(int concurrency_hint)
```

!!! summary "引数"
	- int `concurrency_hint` A suggestion to the implementation on how many threads it should allow to run simultaneously. 

!!! note "戻り値"
	ASIO_DECL



### ~io_context()
Destructor.








```c
ASIO_DECL asio::io_context::~io_context()
```

!!! note "戻り値"
	ASIO_DECL



### get_executor()
Obtains the executor associated with the .


```c
io_context::executor_type asio::io_context::get_executor() ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



### run()
Run the  object's event processing loop.



The  function may also be used to dispatch ready handlers, but without blocking. 
```c
ASIO_DECL count_type asio::io_context::run()
```

!!! note "戻り値"
	ASIO_DECL



### run()


A normal exit from the  function implies that the  object is stopped (the  function returns ). Subsequent calls to , ,  or  will return immediately unless there is a prior call to .
```c
ASIO_DECL count_type asio::io_context::run(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### run_one()





```c
ASIO_DECL count_type asio::io_context::run_one()
```

!!! note "戻り値"
	ASIO_DECL



### run_one()






```c
ASIO_DECL count_type asio::io_context::run_one(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_DECL



### poll()




```c
ASIO_DECL count_type asio::io_context::poll()
```

!!! note "戻り値"
	ASIO_DECL



### poll()


(Deprecated: Use non-error_code overload.) Run the  object's event processing loop to execute ready handlers. The  function runs handlers that are ready to run, without blocking, until the  has been stopped or there are no more ready handlers.
```c
ASIO_DECL count_type asio::io_context::poll(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### poll_one()




```c
ASIO_DECL count_type asio::io_context::poll_one()
```

!!! note "戻り値"
	ASIO_DECL



### poll_one()


(Deprecated: Use non-error_code overload.) Run the  object's event processing loop to execute one ready handler. The  function runs at most one handler that is ready to run, without blocking.
```c
ASIO_DECL count_type asio::io_context::poll_one(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_DECL



### stop()
Stop the  object's event processing loop.

This function does not block, but instead simply signals the  to stop. All invocations of its  or  member functions should return as soon as possible. Subsequent calls to , ,  or  will return immediately until  is called. 
```c
ASIO_DECL void asio::io_context::stop()
```

!!! note "戻り値"
	ASIO_DECLvoid



### stopped()
Determine whether the  object has been stopped.



```c
ASIO_DECL bool asio::io_context::stopped() const
```

!!! note "戻り値"
	ASIO_DECL



### restart()
Restart the  in preparation for a subsequent  invocation.

This function must not be called while there are any unfinished calls to the , ,  or  functions. 
```c
ASIO_DECL void asio::io_context::restart()
```

!!! note "戻り値"
	ASIO_DECLvoid



### reset()


This function must not be called while there are any unfinished calls to the , ,  or  functions. 
```c
void asio::io_context::reset()
```



### dispatch()


The  guarantees that the handler will only be called in a thread in which the , ,  or  member functions is currently being invoked. The handler may be executed inside this function if the guarantee can be met.
```c
asio::io_context::dispatch(ASIO_MOVE_ARG(LegacyCompletionHandler) handler)
```

!!! summary "引数"
	- ASIO_MOVE_ARG(LegacyCompletionHandler) `handler` The handler to be called. The  will make a copy of the handler object as required. The function signature of the handler must be:



### post()


The  guarantees that the handler will only be called in a thread in which the , ,  or  member functions is currently being invoked.
```c
asio::io_context::post(ASIO_MOVE_ARG(LegacyCompletionHandler) handler)
```

!!! summary "引数"
	- ASIO_MOVE_ARG(LegacyCompletionHandler) `handler` The handler to be called. The  will make a copy of the handler object as required. The function signature of the handler must be:



### wrap()


(Deprecated: Use .) Create a new handler that automatically dispatches the wrapped handler on the . This function is used to create a new handler function object that, when invoked, will automatically pass the wrapped handler to the  object's dispatch function.
```c
detail::wrapped_handler< io_context &, Handler > asio::io_context::wrap(Handler handler)
```

!!! summary "引数"
	- Handler `handler` The handler to be wrapped. The  will make a copy of the handler object as required. The function signature of the handler must be:

!!! note "戻り値"
	detail::wrapped_handler<  &, Handler >



