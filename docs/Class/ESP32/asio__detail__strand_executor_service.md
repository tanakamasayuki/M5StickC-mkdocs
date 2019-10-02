# asio::detail::strand_executor_service



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1strand__executor__service.html)

## メンバー



### strand_executor_service()



```c
ASIO_DECL asio::detail::strand_executor_service::strand_executor_service(execution_context &context)
```

!!! summary "引数"
	- execution_context& `context` 

!!! note "戻り値"
	ASIO_DECL



### shutdown()
Destroy all user-defined handler objects owned by the service.


```c
ASIO_DECL void asio::detail::strand_executor_service::shutdown()
```

!!! note "戻り値"
	ASIO_DECLvoid



### create_implementation()



```c
ASIO_DECL implementation_type asio::detail::strand_executor_service::create_implementation()
```

!!! note "戻り値"
	ASIO_DECL



### dispatch()



```c
void asio::detail::strand_executor_service::dispatch(const implementation_type &impl, Executor &ex, ASIO_MOVE_ARG(Function) function, const Allocator &a)
```

!!! summary "引数"
	- const& `impl` 
	- Executor & `ex` 
	- ASIO_MOVE_ARG(Function) `function` 
	- constAllocator & `a` 



### post()



```c
void asio::detail::strand_executor_service::post(const implementation_type &impl, Executor &ex, ASIO_MOVE_ARG(Function) function, const Allocator &a)
```

!!! summary "引数"
	- const& `impl` 
	- Executor & `ex` 
	- ASIO_MOVE_ARG(Function) `function` 
	- constAllocator & `a` 



### defer()



```c
void asio::detail::strand_executor_service::defer(const implementation_type &impl, Executor &ex, ASIO_MOVE_ARG(Function) function, const Allocator &a)
```

!!! summary "引数"
	- const& `impl` 
	- Executor & `ex` 
	- ASIO_MOVE_ARG(Function) `function` 
	- constAllocator & `a` 



### running_in_this_thread()



```c
static ASIO_DECL bool asio::detail::strand_executor_service::running_in_this_thread(const implementation_type &impl)
```

!!! summary "引数"
	- const& `impl` 

!!! note "戻り値"
	ASIO_DECL



