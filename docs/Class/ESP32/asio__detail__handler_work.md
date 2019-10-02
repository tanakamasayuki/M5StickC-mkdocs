# asio::detail::handler_work



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1handler__work.html)

## メンバー

### handler_work()



```c
asio::detail::handler_work< Handler, Executor >::handler_work(Handler &handler) ASIO_NOEXCEPT
```

!!! summary "引数"
	- Handler & `handler` 



### ~handler_work()



```c
asio::detail::handler_work< Handler, Executor >::~handler_work()
```



### complete()



```c
void asio::detail::handler_work< Handler, Executor >::complete(Function &function, Handler &handler)
```

!!! summary "引数"
	- Function & `function` 
	- Handler & `handler` 



### start()



```c
static void asio::detail::handler_work< Handler, Executor >::start(Handler &handler) ASIO_NOEXCEPT
```

!!! summary "引数"
	- Handler & `handler` 



