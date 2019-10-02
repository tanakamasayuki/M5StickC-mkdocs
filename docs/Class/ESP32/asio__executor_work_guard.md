# asio::executor_work_guard



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1executor__work__guard.html)

## メンバー



### executor_work_guard()
Constructs a  object for the specified executor.

Stores a copy of  and calls  on it. 
```c
asio::executor_work_guard< Executor >::executor_work_guard(const executor_type &e) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `e` 



### executor_work_guard()
Copy constructor.


```c
asio::executor_work_guard< Executor >::executor_work_guard(const executor_work_guard &other) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `other` 



### ~executor_work_guard()
Destructor.

Unless the object has already been reset, or is in a moved-from state, calls  on the stored executor. 
```c
asio::executor_work_guard< Executor >::~executor_work_guard()
```



### get_executor()
Obtain the associated executor.


```c
executor_type asio::executor_work_guard< Executor >::get_executor() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



### owns_work()
Whether the  object owns some outstanding work.


```c
bool asio::executor_work_guard< Executor >::owns_work() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	bool



### reset()
Indicate that the work is no longer outstanding.


```c
void asio::executor_work_guard< Executor >::reset() ASIO_NOEXCEPT
```



