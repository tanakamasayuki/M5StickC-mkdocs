# asio::experimental::detail::awaitee_base::awaitable_executor



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1experimental_1_1detail_1_1awaitee__base_1_1awaitable__executor.html)

## メンバー

### awaitable_executor()



```c
asio::experimental::detail::awaitee_base< Executor >::awaitable_executor::awaitable_executor(awaitee_base *a)
```

!!! summary "引数"
	- awaitee_base* `a` 



### await_ready()



```c
bool asio::experimental::detail::awaitee_base< Executor >::awaitable_executor::await_ready() const noexcept
```

!!! note "戻り値"
	bool



### await_suspend()



```c
void asio::experimental::detail::awaitee_base< Executor >::awaitable_executor::await_suspend(coroutine_handle< detail::awaitee< U, Ex >> h) noexcept
```

!!! summary "引数"
	- detail::awaiteecoroutine_handle< < U, Ex >> `h` 



### await_resume()



```c
Executor asio::experimental::detail::awaitee_base< Executor >::awaitable_executor::await_resume()
```

!!! note "戻り値"
	Executor



