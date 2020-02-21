# asio::detail::executor_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1executor__op.html)

## メンバー

### ASIO_DEFINE_HANDLER_ALLOCATOR_PTR()



```c
asio::detail::executor_op< Handler, Alloc, Operation >::ASIO_DEFINE_HANDLER_ALLOCATOR_PTR(executor_op)
```

!!! summary "引数"
	- executor_op `` 



### executor_op()



```c
asio::detail::executor_op< Handler, Alloc, Operation >::executor_op(ASIO_MOVE_ARG(H) h, const Alloc &allocator)
```

!!! summary "引数"
	- ASIO_MOVE_ARG(H) `h` 
	- constAlloc & `allocator` 



### do_complete()



```c
static void asio::detail::executor_op< Handler, Alloc, Operation >::do_complete(void *owner, Operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- Operation * `base` 
	- std::size_t `` 



