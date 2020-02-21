# asio::basic_yield_context

Context object the represents the currently executing coroutine. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1basic__yield__context.html)

## メンバー





###  coro_

```c
detail::weak_ptr<callee_type> asio::basic_yield_context< Handler >::coro_
```


###  ca_

```c
caller_type& asio::basic_yield_context< Handler >::ca_
```


###  handler_

```c
Handler asio::basic_yield_context< Handler >::handler_
```


###  ec_

```c
asio::error_code* asio::basic_yield_context< Handler >::ec_
```


### basic_yield_context()
Construct a yield context to represent the specified coroutine.

Most applications do not need to use this constructor. Instead, the  function passes a yield context as an argument to the coroutine function. 
```c
asio::basic_yield_context< Handler >::basic_yield_context(const detail::weak_ptr< callee_type > &coro, caller_type &ca, Handler &handler)
```

!!! summary "引数"
	- constdetail::weak_ptr<  > & `coro` 
	- caller_type& `ca` 
	- Handler & `handler` 



### basic_yield_context()
Construct a yield context from another yield context type.

Requires that OtherHandler be convertible to Handler. 
```c
asio::basic_yield_context< Handler >::basic_yield_context(const basic_yield_context< OtherHandler > &other)
```

!!! summary "引数"
	- const< OtherHandler > & `other` 



### operator[]()
Return a yield context that sets the specified .

 
```c
basic_yield_context asio::basic_yield_context< Handler >::operator[](asio::error_code &ec) const
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	basic_yield_context



