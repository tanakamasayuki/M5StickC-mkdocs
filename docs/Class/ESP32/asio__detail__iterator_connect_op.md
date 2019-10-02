# asio::detail::iterator_connect_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1iterator__connect__op.html)

## メンバー

###  socket_

```c
basic_socket<Protocol ASIO_SVC_TARG>& asio::detail::iterator_connect_op< ASIO_SVC_TPARAM, Iterator, ConnectCondition, IteratorConnectHandler >::socket_
```


###  iter_

```c
Iterator asio::detail::iterator_connect_op< ASIO_SVC_TPARAM, Iterator, ConnectCondition, IteratorConnectHandler >::iter_
```


###  end_

```c
Iterator asio::detail::iterator_connect_op< ASIO_SVC_TPARAM, Iterator, ConnectCondition, IteratorConnectHandler >::end_
```


###  start_

```c
int asio::detail::iterator_connect_op< ASIO_SVC_TPARAM, Iterator, ConnectCondition, IteratorConnectHandler >::start_
```


###  handler_

```c
IteratorConnectHandler asio::detail::iterator_connect_op< ASIO_SVC_TPARAM, Iterator, ConnectCondition, IteratorConnectHandler >::handler_
```


### iterator_connect_op()



```c
asio::detail::iterator_connect_op< ASIO_SVC_TPARAM, Iterator, ConnectCondition, IteratorConnectHandler >::iterator_connect_op(basic_socket< Protocol ASIO_SVC_TARG > &sock, const Iterator &begin, const Iterator &end, const ConnectCondition &connect_condition, IteratorConnectHandler &handler)
```

!!! summary "引数"
	- basic_socket< Protocol  > & `sock` 
	- constIterator & `begin` 
	- constIterator & `end` 
	- constConnectCondition & `connect_condition` 
	- IteratorConnectHandler & `handler` 



### operator()()



```c
void asio::detail::iterator_connect_op< ASIO_SVC_TPARAM, Iterator, ConnectCondition, IteratorConnectHandler >::operator()(asio::error_code ec, int start=0)
```

!!! summary "引数"
	- asio::error_code `ec` 
	- int `start` 



