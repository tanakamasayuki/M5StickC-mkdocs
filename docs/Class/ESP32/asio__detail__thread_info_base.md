# asio::detail::thread_info_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1thread__info__base.html)

## メンバー

### thread_info_base()



```c
asio::detail::thread_info_base::thread_info_base()
```



### ~thread_info_base()



```c
asio::detail::thread_info_base::~thread_info_base()
```



### allocate()



```c
static void* asio::detail::thread_info_base::allocate(thread_info_base *this_thread, std::size_t size)
```

!!! summary "引数"
	- thread_info_base* `this_thread` 
	- std::size_t `size` 

!!! note "戻り値"
	void *



### deallocate()



```c
static void asio::detail::thread_info_base::deallocate(thread_info_base *this_thread, void *pointer, std::size_t size)
```

!!! summary "引数"
	- thread_info_base* `this_thread` 
	- void * `pointer` 
	- std::size_t `size` 



### allocate()



```c
static void* asio::detail::thread_info_base::allocate(Purpose, thread_info_base *this_thread, std::size_t size)
```

!!! summary "引数"
	- Purpose `` 
	- thread_info_base* `this_thread` 
	- std::size_t `size` 

!!! note "戻り値"
	void *



### deallocate()



```c
static void asio::detail::thread_info_base::deallocate(Purpose, thread_info_base *this_thread, void *pointer, std::size_t size)
```

!!! summary "引数"
	- Purpose `` 
	- thread_info_base* `this_thread` 
	- void * `pointer` 
	- std::size_t `size` 



