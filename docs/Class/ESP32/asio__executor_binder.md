# asio::executor_binder



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1executor__binder.html)

## メンバー







### executor_binder()
Construct an executor wrapper for the specified object.

This constructor is only valid if the type  is constructible from type . 
```c
asio::executor_binder< T, Executor >::executor_binder(executor_arg_t, const executor_type &e, ASIO_MOVE_ARG(U) u)
```

!!! summary "引数"
	- executor_arg_t `` 
	- const& `e` 
	- ASIO_MOVE_ARG(U) `u` 



### executor_binder()
Copy constructor.


```c
asio::executor_binder< T, Executor >::executor_binder(const executor_binder &other)
```

!!! summary "引数"
	- const& `other` 



### executor_binder()
Construct a copy, but specify a different executor.


```c
asio::executor_binder< T, Executor >::executor_binder(executor_arg_t, const executor_type &e, const executor_binder &other)
```

!!! summary "引数"
	- executor_arg_t `` 
	- const& `e` 
	- const& `other` 



### executor_binder()
Construct a copy of a different executor wrapper type.

This constructor is only valid if the  type is constructible from type , and the type  is constructible from type . 
```c
asio::executor_binder< T, Executor >::executor_binder(const executor_binder< U, OtherExecutor > &other)
```

!!! summary "引数"
	- const< U, OtherExecutor > & `other` 



### executor_binder()


Construct a copy of a different executor wrapper type, but specify a different executor. This constructor is only valid if the type  is constructible from type . 
```c
asio::executor_binder< T, Executor >::executor_binder(executor_arg_t, const executor_type &e, const executor_binder< U, OtherExecutor > &other)
```

!!! summary "引数"
	- executor_arg_t `` 
	- const& `e` 
	- const< U, OtherExecutor > & `other` 



### ~executor_binder()
Destructor.


```c
asio::executor_binder< T, Executor >::~executor_binder()
```



### get()
Obtain a reference to the target object.


```c
target_type& asio::executor_binder< T, Executor >::get() ASIO_NOEXCEPT
```

!!! note "戻り値"
	target_type&



### get()
Obtain a reference to the target object.


```c
const target_type& asio::executor_binder< T, Executor >::get() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	const&



### get_executor()
Obtain the associated executor.


```c
executor_type asio::executor_binder< T, Executor >::get_executor() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



### operator()()



```c
result_type_or_void asio::executor_binder< T, Executor >::operator()()
```

!!! note "戻り値"
	result_type_or_void



### operator()()



```c
result_type_or_void asio::executor_binder< T, Executor >::operator()() const
```

!!! note "戻り値"
	result_type_or_void



