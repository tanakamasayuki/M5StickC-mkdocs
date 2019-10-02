# asio::experimental::detail::awaiter_task



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1experimental_1_1detail_1_1awaiter__task.html)

## メンバー



### awaiter_task()



```c
asio::experimental::detail::awaiter_task< Executor >::awaiter_task(awaiter< Executor > *a)
```

!!! summary "引数"
	- awaiter< Executor > * `a` 



### awaiter_task()



```c
asio::experimental::detail::awaiter_task< Executor >::awaiter_task(awaiter_task &&other) noexcept
```

!!! summary "引数"
	- awaiter_task&& `other` 



### ~awaiter_task()



```c
asio::experimental::detail::awaiter_task< Executor >::~awaiter_task()
```



### get_executor()



```c
executor_type asio::experimental::detail::awaiter_task< Executor >::get_executor() const noexcept
```

!!! note "戻り値"
	executor_type



