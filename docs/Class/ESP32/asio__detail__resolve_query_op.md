# asio::detail::resolve_query_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1resolve__query__op.html)

## メンバー





### ASIO_DEFINE_HANDLER_PTR()



```c
asio::detail::resolve_query_op< Protocol, Handler >::ASIO_DEFINE_HANDLER_PTR(resolve_query_op)
```

!!! summary "引数"
	- resolve_query_op `` 



### resolve_query_op()



```c
asio::detail::resolve_query_op< Protocol, Handler >::resolve_query_op(socket_ops::weak_cancel_token_type cancel_token, const query_type &query, io_context_impl &ioc, Handler &handler)
```

!!! summary "引数"
	- socket_ops::weak_cancel_token_type `cancel_token` 
	- const& `query` 
	- io_context_impl& `ioc` 
	- Handler & `handler` 



### ~resolve_query_op()



```c
asio::detail::resolve_query_op< Protocol, Handler >::~resolve_query_op()
```



### do_complete()



```c
static void asio::detail::resolve_query_op< Protocol, Handler >::do_complete(void *owner, operation *base, const asio::error_code &, std::size_t)
```

!!! summary "引数"
	- void * `owner` 
	- operation* `base` 
	- std::size_t `` 



