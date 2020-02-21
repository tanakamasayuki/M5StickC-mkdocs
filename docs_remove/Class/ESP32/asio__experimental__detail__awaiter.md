# asio::experimental::detail::awaiter



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1experimental_1_1detail_1_1awaiter.html)

## メンバー





### ~awaiter()



```c
asio::experimental::detail::awaiter< Executor >::~awaiter()
```



### set_executor()



```c
void asio::experimental::detail::awaiter< Executor >::set_executor(const Executor &ex)
```

!!! summary "引数"
	- constExecutor & `ex` 



### get_executor()



```c
executor_type asio::experimental::detail::awaiter< Executor >::get_executor() const noexcept
```

!!! note "戻り値"
	executor_type



### get_return_object()



```c
awaiter* asio::experimental::detail::awaiter< Executor >::get_return_object()
```

!!! note "戻り値"
	awaiter*



### initial_suspend()



```c
auto asio::experimental::detail::awaiter< Executor >::initial_suspend()
```

!!! note "戻り値"
	auto



### final_suspend()



```c
auto asio::experimental::detail::awaiter< Executor >::final_suspend()
```

!!! note "戻り値"
	auto



### return_void()



```c
void asio::experimental::detail::awaiter< Executor >::return_void()
```



### add_ref()



```c
awaiter* asio::experimental::detail::awaiter< Executor >::add_ref()
```

!!! note "戻り値"
	awaiter*



### release()



```c
void asio::experimental::detail::awaiter< Executor >::release()
```



### unhandled_exception()



```c
void asio::experimental::detail::awaiter< Executor >::unhandled_exception()
```



### rethrow_unhandled_exception()



```c
void asio::experimental::detail::awaiter< Executor >::rethrow_unhandled_exception()
```



