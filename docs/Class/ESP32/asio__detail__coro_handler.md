# asio::detail::coro_handler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1coro__handler.html)

## メンバー

###  coro_

```c
shared_ptr<typename basic_yield_context<Handler>::callee_type> asio::detail::coro_handler< Handler, T >::coro_
```


###  ca_

```c
basic_yield_context<Handler>::caller_type& asio::detail::coro_handler< Handler, T >::ca_
```


###  handler_

```c
Handler asio::detail::coro_handler< Handler, T >::handler_
```


###  ready_

```c
atomic_count* asio::detail::coro_handler< Handler, T >::ready_
```


###  ec_

```c
asio::error_code* asio::detail::coro_handler< Handler, T >::ec_
```


###  value_

```c
T* asio::detail::coro_handler< Handler, T >::value_
```


### coro_handler()



```c
asio::detail::coro_handler< Handler, T >::coro_handler(basic_yield_context< Handler > ctx)
```

!!! summary "引数"
	- basic_yield_context< Handler > `ctx` 



### operator()()



```c
void asio::detail::coro_handler< Handler, T >::operator()(T value)
```

!!! summary "引数"
	- T `value` 



### operator()()



```c
void asio::detail::coro_handler< Handler, T >::operator()(asio::error_code ec, T value)
```

!!! summary "引数"
	- asio::error_code `ec` 
	- T `value` 



