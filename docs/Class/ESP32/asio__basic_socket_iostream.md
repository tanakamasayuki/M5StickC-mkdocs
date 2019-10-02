# asio::basic_socket_iostream

Iostream interface for a socket. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1basic__socket__iostream.html)

## メンバー















### basic_socket_iostream()
Construct a  without establishing a connection.


```c
asio::basic_socket_iostream< ASIO_SVC_TPARAM, Clock, ASIO_SVC_TPARAM1 >::basic_socket_iostream()
```



### close()
Close the connection.


```c
void asio::basic_socket_iostream< ASIO_SVC_TPARAM, Clock, ASIO_SVC_TPARAM1 >::close()
```



### rdbuf()
Return a pointer to the underlying streambuf.


```c
basic_socket_streambuf<Protocol ASIO_SVC_TARG, Clock, WaitTraits ASIO_SVC_TARG1>* asio::basic_socket_iostream< ASIO_SVC_TPARAM, Clock, ASIO_SVC_TPARAM1 >::rdbuf() const
```

!!! note "戻り値"
	basic_socket_streambuf< Protocol , Clock, WaitTraits  > *



### socket()
Get a reference to the underlying socket.


```c
basic_socket<Protocol ASIO_SVC_TARG>& asio::basic_socket_iostream< ASIO_SVC_TPARAM, Clock, ASIO_SVC_TPARAM1 >::socket()
```

!!! note "戻り値"
	basic_socket< Protocol  > &



### error()
Get the last error associated with the stream.




```c
const asio::error_code& asio::basic_socket_iostream< ASIO_SVC_TPARAM, Clock, ASIO_SVC_TPARAM1 >::error() const
```

!!! note "戻り値"
	const& An  corresponding to the last error from the stream.



### expires_at()


(Deprecated: Use .) Get the stream's expiry time as an absolute time. 

```c
time_point asio::basic_socket_iostream< ASIO_SVC_TPARAM, Clock, ASIO_SVC_TPARAM1 >::expires_at() const
```

!!! note "戻り値"
	time_point An absolute time value representing the stream's expiry time. 



### expiry()
Get the stream's expiry time as an absolute time.



```c
time_point asio::basic_socket_iostream< ASIO_SVC_TPARAM, Clock, ASIO_SVC_TPARAM1 >::expiry() const
```

!!! note "戻り値"
	time_point An absolute time value representing the stream's expiry time. 



### expires_at()
Set the stream's expiry time as an absolute time.

This function sets the expiry time associated with the stream.  operations performed after this time (where the operations cannot be completed using the internal buffers) will fail with the error .
```c
void asio::basic_socket_iostream< ASIO_SVC_TPARAM, Clock, ASIO_SVC_TPARAM1 >::expires_at(const time_point &expiry_time)
```

!!! summary "引数"
	- const& `expiry_time` The expiry time to be used for the stream. 



### expires_after()
Set the stream's expiry time relative to now.

This function sets the expiry time associated with the stream.  operations performed after this time (where the operations cannot be completed using the internal buffers) will fail with the error .
```c
void asio::basic_socket_iostream< ASIO_SVC_TPARAM, Clock, ASIO_SVC_TPARAM1 >::expires_after(const duration &expiry_time)
```

!!! summary "引数"
	- const& `expiry_time` The expiry time to be used for the timer. 



### expires_from_now()
(Deprecated: Use .) Get the stream's expiry time relative to now.



```c
duration asio::basic_socket_iostream< ASIO_SVC_TPARAM, Clock, ASIO_SVC_TPARAM1 >::expires_from_now() const
```

!!! note "戻り値"
	duration A relative time value representing the stream's expiry time. 



### expires_from_now()


(Deprecated: Use .) Set the stream's expiry time relative to now. This function sets the expiry time associated with the stream.  operations performed after this time (where the operations cannot be completed using the internal buffers) will fail with the error .
```c
void asio::basic_socket_iostream< ASIO_SVC_TPARAM, Clock, ASIO_SVC_TPARAM1 >::expires_from_now(const duration &expiry_time)
```

!!! summary "引数"
	- const& `expiry_time` The expiry time to be used for the timer. 



