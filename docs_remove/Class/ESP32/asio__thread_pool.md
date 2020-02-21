# asio::thread_pool

A simple fixed-size thread pool. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1thread__pool.html)

## メンバー

### thread_pool()
Constructs a pool with an automatically determined number of threads.


```c
ASIO_DECL asio::thread_pool::thread_pool()
```

!!! note "戻り値"
	ASIO_DECL



### thread_pool()
Constructs a pool with a specified number of threads.


```c
ASIO_DECL asio::thread_pool::thread_pool(std::size_t num_threads)
```

!!! summary "引数"
	- std::size_t `num_threads` 

!!! note "戻り値"
	ASIO_DECL



### ~thread_pool()
Destructor.

Automatically stops and joins the pool, if not explicitly done beforehand. 
```c
ASIO_DECL asio::thread_pool::~thread_pool()
```

!!! note "戻り値"
	ASIO_DECL



### get_executor()
Obtains the executor associated with the pool.


```c
thread_pool::executor_type asio::thread_pool::get_executor() ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



### stop()
Stops the threads.

This function stops the threads as soon as possible. As a result of calling , pending function objects may be never be invoked. 
```c
ASIO_DECL void asio::thread_pool::stop()
```

!!! note "戻り値"
	ASIO_DECLvoid



### join()
Joins the threads.

This function blocks until the threads in the pool have completed. If  is not called prior to , the  call will wait until the pool has no more outstanding work. 
```c
ASIO_DECL void asio::thread_pool::join()
```

!!! note "戻り値"
	ASIO_DECLvoid



