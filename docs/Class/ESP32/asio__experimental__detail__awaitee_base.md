# asio::experimental::detail::awaitee_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1experimental_1_1detail_1_1awaitee__base.html)

## メンバー

### operator new()



```c
void* asio::experimental::detail::awaitee_base< Executor >::operator new(std::size_t size)
```

!!! summary "引数"
	- std::size_t `size` 

!!! note "戻り値"
	void *



### operator delete()



```c
void asio::experimental::detail::awaitee_base< Executor >::operator delete(void *pointer, std::size_t size)
```

!!! summary "引数"
	- void * `pointer` 
	- std::size_t `size` 



### initial_suspend()



```c
auto asio::experimental::detail::awaitee_base< Executor >::initial_suspend()
```

!!! note "戻り値"
	auto



### final_suspend()



```c
auto asio::experimental::detail::awaitee_base< Executor >::final_suspend()
```

!!! note "戻り値"
	auto



### set_except()



```c
void asio::experimental::detail::awaitee_base< Executor >::set_except(std::exception_ptr e)
```

!!! summary "引数"
	- std::exception_ptr `e` 



### unhandled_exception()



```c
void asio::experimental::detail::awaitee_base< Executor >::unhandled_exception()
```



### rethrow_exception()



```c
void asio::experimental::detail::awaitee_base< Executor >::rethrow_exception()
```



### top()



```c
awaiter<Executor>* asio::experimental::detail::awaitee_base< Executor >::top()
```

!!! note "戻り値"
	awaiter< Executor > *



### caller()



```c
coroutine_handle<void> asio::experimental::detail::awaitee_base< Executor >::caller()
```

!!! note "戻り値"
	coroutine_handle< void >



### ready()



```c
bool asio::experimental::detail::awaitee_base< Executor >::ready() const
```

!!! note "戻り値"
	bool



### wake_caller()



```c
void asio::experimental::detail::awaitee_base< Executor >::wake_caller()
```



### await_transform()



```c
awaitable_executor asio::experimental::detail::awaitee_base< Executor >::await_transform(this_coro::executor_t) noexcept
```

!!! summary "引数"
	- this_coro::executor_t `` 

!!! note "戻り値"
	awaitable_executor



### await_transform()



```c
awaitable_token asio::experimental::detail::awaitee_base< Executor >::await_transform(this_coro::token_t) noexcept
```

!!! summary "引数"
	- this_coro::token_t `` 

!!! note "戻り値"
	awaitable_token



### await_transform()



```c
awaitable<T, Executor> asio::experimental::detail::awaitee_base< Executor >::await_transform(awaitable< T, Executor > &t) const
```

!!! summary "引数"
	- Tawaitable< , Executor > & `t` 

!!! note "戻り値"
	Tawaitable< , Executor >



### await_transform()



```c
awaitable<T, Executor> asio::experimental::detail::awaitee_base< Executor >::await_transform(awaitable< T, Executor > &&t) const
```

!!! summary "引数"
	- Tawaitable< , Executor > && `t` 

!!! note "戻り値"
	Tawaitable< , Executor >



### await_transform()



```c
std::experimental::suspend_always asio::experimental::detail::awaitee_base< Executor >::await_transform(std::experimental::suspend_always) const
```

!!! summary "引数"
	- std::experimental::suspend_always `` 

!!! note "戻り値"
	std::experimental::suspend_always



### attach_caller()



```c
void asio::experimental::detail::awaitee_base< Executor >::attach_caller(coroutine_handle< awaiter< Executor >> h)
```

!!! summary "引数"
	- awaitercoroutine_handle< < Executor >> `h` 



### attach_caller()



```c
void asio::experimental::detail::awaitee_base< Executor >::attach_caller(coroutine_handle< awaitee< U, Executor >> h)
```

!!! summary "引数"
	- awaiteecoroutine_handle< < U, Executor >> `h` 



### attach_callees()



```c
void asio::experimental::detail::awaitee_base< Executor >::attach_callees(awaiter< Executor > *a)
```

!!! summary "引数"
	- awaiter< Executor > * `a` 



