# asio::detail::promise_executor



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1promise__executor.html)

## メンバー

### promise_executor()



```c
asio::detail::promise_executor< T >::promise_executor(const shared_ptr< std::promise< T > > &p)
```

!!! summary "引数"
	- constshared_ptr< std::promise<  > > & `p` 



### context()



```c
execution_context& asio::detail::promise_executor< T >::context() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	execution_context&



### on_work_started()



```c
void asio::detail::promise_executor< T >::on_work_started() const ASIO_NOEXCEPT
```



### on_work_finished()



```c
void asio::detail::promise_executor< T >::on_work_finished() const ASIO_NOEXCEPT
```



### dispatch()



```c
void asio::detail::promise_executor< T >::dispatch(ASIO_MOVE_ARG(F) f, const A &) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(F) `f` 
	- constA & `` 



### post()



```c
void asio::detail::promise_executor< T >::post(ASIO_MOVE_ARG(F) f, const A &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(F) `f` 
	- constA & `a` 



### defer()



```c
void asio::detail::promise_executor< T >::defer(ASIO_MOVE_ARG(F) f, const A &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(F) `f` 
	- constA & `a` 







