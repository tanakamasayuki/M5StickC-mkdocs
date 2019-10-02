# asio::detail::thread_group



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1thread__group.html)

## メンバー

### thread_group()



```c
asio::detail::thread_group::thread_group()
```



### ~thread_group()



```c
asio::detail::thread_group::~thread_group()
```



### create_thread()



```c
void asio::detail::thread_group::create_thread(Function f)
```

!!! summary "引数"
	- Function `f` 



### create_threads()



```c
void asio::detail::thread_group::create_threads(Function f, std::size_t num_threads)
```

!!! summary "引数"
	- Function `f` 
	- std::size_t `num_threads` 



### join()



```c
void asio::detail::thread_group::join()
```



