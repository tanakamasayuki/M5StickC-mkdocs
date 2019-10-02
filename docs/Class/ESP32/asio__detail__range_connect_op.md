# asio::detail::range_connect_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1range__connect__op.html)

## メンバー

###  socket_

```c
basic_socket<Protocol ASIO_SVC_TARG>& asio::detail::range_connect_op< ASIO_SVC_TPARAM, EndpointSequence, ConnectCondition, RangeConnectHandler >::socket_
```


###  endpoints_

```c
EndpointSequence asio::detail::range_connect_op< ASIO_SVC_TPARAM, EndpointSequence, ConnectCondition, RangeConnectHandler >::endpoints_
```


###  index_

```c
std::size_t asio::detail::range_connect_op< ASIO_SVC_TPARAM, EndpointSequence, ConnectCondition, RangeConnectHandler >::index_
```


###  start_

```c
int asio::detail::range_connect_op< ASIO_SVC_TPARAM, EndpointSequence, ConnectCondition, RangeConnectHandler >::start_
```


###  handler_

```c
RangeConnectHandler asio::detail::range_connect_op< ASIO_SVC_TPARAM, EndpointSequence, ConnectCondition, RangeConnectHandler >::handler_
```


### range_connect_op()



```c
asio::detail::range_connect_op< ASIO_SVC_TPARAM, EndpointSequence, ConnectCondition, RangeConnectHandler >::range_connect_op(basic_socket< Protocol ASIO_SVC_TARG > &sock, const EndpointSequence &endpoints, const ConnectCondition &connect_condition, RangeConnectHandler &handler)
```

!!! summary "引数"
	- basic_socket< Protocol  > & `sock` 
	- constEndpointSequence & `endpoints` 
	- constConnectCondition & `connect_condition` 
	- RangeConnectHandler & `handler` 



### operator()()



```c
void asio::detail::range_connect_op< ASIO_SVC_TPARAM, EndpointSequence, ConnectCondition, RangeConnectHandler >::operator()(asio::error_code ec, int start=0)
```

!!! summary "引数"
	- asio::error_code `ec` 
	- int `start` 



