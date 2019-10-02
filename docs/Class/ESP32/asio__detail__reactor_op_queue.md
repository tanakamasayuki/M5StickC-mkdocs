# asio::detail::reactor_op_queue



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1reactor__op__queue.html)

## メンバー







### reactor_op_queue()



```c
asio::detail::reactor_op_queue< Descriptor >::reactor_op_queue()
```



### begin()



```c
iterator asio::detail::reactor_op_queue< Descriptor >::begin()
```

!!! note "戻り値"
	iterator



### end()



```c
iterator asio::detail::reactor_op_queue< Descriptor >::end()
```

!!! note "戻り値"
	iterator



### enqueue_operation()



```c
bool asio::detail::reactor_op_queue< Descriptor >::enqueue_operation(Descriptor descriptor, reactor_op *op)
```

!!! summary "引数"
	- Descriptor `descriptor` 
	- reactor_op* `op` 

!!! note "戻り値"
	bool



### cancel_operations()



```c
bool asio::detail::reactor_op_queue< Descriptor >::cancel_operations(iterator i, op_queue< operation > &ops, const asio::error_code &ec=asio::error::operation_aborted)
```

!!! summary "引数"
	- iterator `i` 
	- op_queue<  > & `ops` 
	- const& `ec` 

!!! note "戻り値"
	bool



### cancel_operations()



```c
bool asio::detail::reactor_op_queue< Descriptor >::cancel_operations(Descriptor descriptor, op_queue< operation > &ops, const asio::error_code &ec=asio::error::operation_aborted)
```

!!! summary "引数"
	- Descriptor `descriptor` 
	- op_queue<  > & `ops` 
	- const& `ec` 

!!! note "戻り値"
	bool



### empty()



```c
bool asio::detail::reactor_op_queue< Descriptor >::empty() const
```

!!! note "戻り値"
	bool



### has_operation()



```c
bool asio::detail::reactor_op_queue< Descriptor >::has_operation(Descriptor descriptor) const
```

!!! summary "引数"
	- Descriptor `descriptor` 

!!! note "戻り値"
	bool



### perform_operations()



```c
bool asio::detail::reactor_op_queue< Descriptor >::perform_operations(iterator i, op_queue< operation > &ops)
```

!!! summary "引数"
	- iterator `i` 
	- op_queue<  > & `ops` 

!!! note "戻り値"
	bool



### perform_operations()



```c
bool asio::detail::reactor_op_queue< Descriptor >::perform_operations(Descriptor descriptor, op_queue< operation > &ops)
```

!!! summary "引数"
	- Descriptor `descriptor` 
	- op_queue<  > & `ops` 

!!! note "戻り値"
	bool



### get_all_operations()



```c
void asio::detail::reactor_op_queue< Descriptor >::get_all_operations(op_queue< operation > &ops)
```

!!! summary "引数"
	- op_queue<  > & `ops` 



