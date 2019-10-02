# asio::system_context

The executor context for the system executor. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1system__context.html)

## メンバー



### ~system_context()
Destructor shuts down all threads in the system thread pool.


```c
ASIO_DECL asio::system_context::~system_context()
```

!!! note "戻り値"
	ASIO_DECL



### get_executor()
Obtain an executor for the context.


```c
system_context::executor_type asio::system_context::get_executor() ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



### stop()
Signal all threads in the system thread pool to stop.


```c
ASIO_DECL void asio::system_context::stop()
```

!!! note "戻り値"
	ASIO_DECLvoid



### stopped()
Determine whether the system thread pool has been stopped.


```c
ASIO_DECL bool asio::system_context::stopped() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	ASIO_DECL



### join()
Join all threads in the system thread pool.


```c
ASIO_DECL void asio::system_context::join()
```

!!! note "戻り値"
	ASIO_DECLvoid



### system_context()



```c
ASIO_DECL asio::system_context::system_context()
```

!!! note "戻り値"
	ASIO_DECL



