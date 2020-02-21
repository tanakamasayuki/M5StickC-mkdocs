# asio::ssl::detail::io_op



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1detail_1_1io__op.html)

## メンバー

###  next_layer_

```c
Stream& asio::ssl::detail::io_op< Stream, Operation, Handler >::next_layer_
```


###  core_

```c
stream_core& asio::ssl::detail::io_op< Stream, Operation, Handler >::core_
```


###  op_

```c
Operation asio::ssl::detail::io_op< Stream, Operation, Handler >::op_
```


###  start_

```c
int asio::ssl::detail::io_op< Stream, Operation, Handler >::start_
```


###  want_

```c
engine::want asio::ssl::detail::io_op< Stream, Operation, Handler >::want_
```


###  ec_

```c
asio::error_code asio::ssl::detail::io_op< Stream, Operation, Handler >::ec_
```


###  bytes_transferred_

```c
std::size_t asio::ssl::detail::io_op< Stream, Operation, Handler >::bytes_transferred_
```


###  handler_

```c
Handler asio::ssl::detail::io_op< Stream, Operation, Handler >::handler_
```


### io_op()



```c
asio::ssl::detail::io_op< Stream, Operation, Handler >::io_op(Stream &next_layer, stream_core &core, const Operation &op, Handler &handler)
```

!!! summary "引数"
	- Stream& `next_layer` 
	- stream_core& `core` 
	- constOperation & `op` 
	- Handler & `handler` 



### operator()()



```c
void asio::ssl::detail::io_op< Stream, Operation, Handler >::operator()(asio::error_code ec, std::size_t bytes_transferred=~std::size_t(0), int start=0)
```

!!! summary "引数"
	- asio::error_code `ec` 
	- std::size_t `bytes_transferred` 
	- int `start` 



