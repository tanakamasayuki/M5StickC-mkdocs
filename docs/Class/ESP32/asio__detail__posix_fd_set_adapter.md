# asio::detail::posix_fd_set_adapter



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1posix__fd__set__adapter.html)

## メンバー

### posix_fd_set_adapter()



```c
asio::detail::posix_fd_set_adapter::posix_fd_set_adapter()
```



### reset()



```c
void asio::detail::posix_fd_set_adapter::reset()
```



### set()



```c
bool asio::detail::posix_fd_set_adapter::set(socket_type descriptor)
```

!!! summary "引数"
	- socket_type `descriptor` 

!!! note "戻り値"
	bool



### set()



```c
void asio::detail::posix_fd_set_adapter::set(reactor_op_queue< socket_type > &operations, op_queue< operation > &ops)
```

!!! summary "引数"
	- reactor_op_queue<  > & `operations` 
	- op_queue<  > & `ops` 



### is_set()



```c
bool asio::detail::posix_fd_set_adapter::is_set(socket_type descriptor) const
```

!!! summary "引数"
	- socket_type `descriptor` 

!!! note "戻り値"
	bool



### operator fd_set *()



```c
asio::detail::posix_fd_set_adapter::operator fd_set *()
```



### max_descriptor()



```c
socket_type asio::detail::posix_fd_set_adapter::max_descriptor() const
```

!!! note "戻り値"
	socket_type



### perform()



```c
void asio::detail::posix_fd_set_adapter::perform(reactor_op_queue< socket_type > &operations, op_queue< operation > &ops) const
```

!!! summary "引数"
	- reactor_op_queue<  > & `operations` 
	- op_queue<  > & `ops` 



