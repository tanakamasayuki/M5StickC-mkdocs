# asio::io_context::work



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1io__context_1_1work.html)

## メンバー

### work()
Constructor notifies the  that work is starting.

The constructor is used to inform the  that some work has begun. This ensures that the  object's  function will not exit while the work is underway. 
```c
asio::io_context::work::work(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### work()
Copy constructor notifies the  that work is starting.

The constructor is used to inform the  that some work has begun. This ensures that the  object's  function will not exit while the work is underway. 
```c
asio::io_context::work::work(const work &other)
```

!!! summary "引数"
	- const& `other` 



### ~work()
Destructor notifies the  that the work is complete.

The destructor is used to inform the  that some work has finished. Once the count of unfinished work reaches zero, the  object's  function is permitted to exit. 
```c
asio::io_context::work::~work()
```



### get_io_context()
Get the  associated with the work.


```c
asio::io_context & asio::io_context::work::get_io_context()
```

!!! note "戻り値"
	asio::io_context&



### get_io_service()


(Deprecated: Use .) Get the  associated with the work. 
```c
asio::io_context & asio::io_context::work::get_io_service()
```

!!! note "戻り値"
	asio::io_context&



