# asio::experimental::detail::await_handler_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1experimental_1_1detail_1_1await__handler__base.html)

## メンバー



### await_handler_base()



```c
asio::experimental::detail::await_handler_base< Executor, T >::await_handler_base(await_token< Executor > token)
```

!!! summary "引数"
	- await_token< Executor > `token` 



### await_handler_base()



```c
asio::experimental::detail::await_handler_base< Executor, T >::await_handler_base(await_handler_base &&other) noexcept
```

!!! summary "引数"
	- await_handler_base&& `other` 



### attach_awaitee()



```c
void asio::experimental::detail::await_handler_base< Executor, T >::attach_awaitee(const awaitable< T, Executor > &a)
```

!!! summary "引数"
	- constawaitable< , Executor > & `a` 



