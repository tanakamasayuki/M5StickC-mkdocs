# asio::experimental::detail::awaitee



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1experimental_1_1detail_1_1awaitee.html)

## メンバー

### awaitee()



```c
asio::experimental::detail::awaitee< T, Executor >::awaitee()
```



### awaitee()



```c
asio::experimental::detail::awaitee< T, Executor >::awaitee(awaitee &&other) noexcept
```

!!! summary "引数"
	- awaitee&& `other` 



### ~awaitee()



```c
asio::experimental::detail::awaitee< T, Executor >::~awaitee()
```



### get_return_object()



```c
awaitable<T, Executor> asio::experimental::detail::awaitee< T, Executor >::get_return_object()
```

!!! note "戻り値"
	Tawaitable< , Executor >



### return_value()



```c
void asio::experimental::detail::awaitee< T, Executor >::return_value(U &&u)
```

!!! summary "引数"
	- U && `u` 



### get()



```c
T asio::experimental::detail::awaitee< T, Executor >::get()
```

!!! note "戻り値"
	T



