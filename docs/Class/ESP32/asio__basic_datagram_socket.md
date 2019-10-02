# asio::basic_datagram_socket

Provides datagram-oriented socket functionality. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1basic__datagram__socket.html)

## メンバー







###  flags

```c
socket_base::message_flags asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::flags
```


###  destination

```c
const endpoint_type & asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::destination
```


###  flags

```c
const endpoint_type socket_base::message_flags asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::flags
```


###  sender_endpoint

```c
endpoint_type & asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::sender_endpoint
```


###  flags

```c
endpoint_type socket_base::message_flags asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::flags
```


### basic_datagram_socket()
Construct a  without opening it.

This constructor creates a datagram socket without opening it. The  function must be called before data can be sent or received on the socket.
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::basic_datagram_socket(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### basic_datagram_socket()
Construct and open a .

This constructor creates and opens a datagram socket.
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::basic_datagram_socket(asio::io_context &io_context, const protocol_type &protocol)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `protocol` An object specifying protocol parameters to be used.



### basic_datagram_socket()


Construct a , opening it and binding it to the given local endpoint. This constructor creates a datagram socket and automatically opens it bound to the specified endpoint on the local machine. The protocol used is the protocol associated with the given endpoint.
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::basic_datagram_socket(asio::io_context &io_context, const endpoint_type &endpoint)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `endpoint` An endpoint on the local machine to which the datagram socket will be bound.



### basic_datagram_socket()
Construct a  on an existing native socket.

This constructor creates a datagram socket object to hold an existing native socket.
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::basic_datagram_socket(asio::io_context &io_context, const protocol_type &protocol, const native_handle_type &native_socket)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `protocol` An object specifying protocol parameters to be used.
	- const& `native_socket` The new underlying socket implementation.



### ~basic_datagram_socket()
Destroys the socket.

This function destroys the socket, cancelling any outstanding asynchronous operations associated with the socket as if by calling . 
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::~basic_datagram_socket()
```



### send()
Send some data on a connected socket.

This function is used to send data on the datagram socket. The function call will block until the data has been sent successfully or an error occurs.
```c
std::size_t asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::send(const ConstBufferSequence &buffers)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One ore more data buffers to be sent on the socket.

!!! note "戻り値"
	std::size_t



### send()
Send some data on a connected socket.

This function is used to send data on the datagram socket. The function call will block until the data has been sent successfully or an error occurs.
```c
std::size_t asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::send(const ConstBufferSequence &buffers, socket_base::message_flags flags)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One ore more data buffers to be sent on the socket.
	- socket_base::message_flags `flags` Flags specifying how the send call is to be made.

!!! note "戻り値"
	std::size_t



### send()
Send some data on a connected socket.

This function is used to send data on the datagram socket. The function call will block until the data has been sent successfully or an error occurs.
```c
std::size_t asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::send(const ConstBufferSequence &buffers, socket_base::message_flags flags, asio::error_code &ec)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One or more data buffers to be sent on the socket.
	- socket_base::message_flags `flags` Flags specifying how the send call is to be made.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous send on a connected socket.

This function is used to asynchronously send data on the datagram socket. The function call always returns immediately.
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(WriteHandler, void(asio::error_code, std::size_t)) async_send(const ConstBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(WriteHandler) handler)
```

!!! summary "引数"
	- WriteHandler `` 



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous send on a connected socket.

This function is used to asynchronously send data on the datagram socket. The function call always returns immediately.
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(WriteHandler, void(asio::error_code, std::size_t)) async_send(const ConstBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
socket_base::message_flags asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(WriteHandler) handler)
```

!!! summary "引数"
	- WriteHandler `` 

!!! note "戻り値"
	socket_base::message_flags



### send_to()
Send a datagram to the specified endpoint.

This function is used to send a datagram to the specified remote endpoint. The function call will block until the data has been sent successfully or an error occurs.
```c
std::size_t asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::send_to(const ConstBufferSequence &buffers, const endpoint_type &destination)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One or more data buffers to be sent to the remote endpoint.
	- const& `destination` The remote endpoint to which the data will be sent.

!!! note "戻り値"
	std::size_t



### send_to()
Send a datagram to the specified endpoint.

This function is used to send a datagram to the specified remote endpoint. The function call will block until the data has been sent successfully or an error occurs.
```c
std::size_t asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::send_to(const ConstBufferSequence &buffers, const endpoint_type &destination, socket_base::message_flags flags)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One or more data buffers to be sent to the remote endpoint.
	- const& `destination` The remote endpoint to which the data will be sent.
	- socket_base::message_flags `flags` Flags specifying how the send call is to be made.

!!! note "戻り値"
	std::size_t



### send_to()
Send a datagram to the specified endpoint.

This function is used to send a datagram to the specified remote endpoint. The function call will block until the data has been sent successfully or an error occurs.
```c
std::size_t asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::send_to(const ConstBufferSequence &buffers, const endpoint_type &destination, socket_base::message_flags flags, asio::error_code &ec)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One or more data buffers to be sent to the remote endpoint.
	- const& `destination` The remote endpoint to which the data will be sent.
	- socket_base::message_flags `flags` Flags specifying how the send call is to be made.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous send.

This function is used to asynchronously send a datagram to the specified remote endpoint. The function call always returns immediately.
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(WriteHandler, void(asio::error_code, std::size_t)) async_send_to(const ConstBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
const endpoint_type asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(WriteHandler) handler)
```

!!! summary "引数"
	- WriteHandler `` 

!!! note "戻り値"
	const



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous send.

This function is used to asynchronously send a datagram to the specified remote endpoint. The function call always returns immediately.
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(WriteHandler, void(asio::error_code, std::size_t)) async_send_to(const ConstBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
const endpoint_type socket_base::message_flags asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(WriteHandler) handler)
```

!!! summary "引数"
	- WriteHandler `` 

!!! note "戻り値"
	const



### receive()
Receive some data on a connected socket.

This function is used to receive data on the datagram socket. The function call will block until data has been received successfully or an error occurs.
```c
std::size_t asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::receive(const MutableBufferSequence &buffers)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be received.

!!! note "戻り値"
	std::size_t



### receive()
Receive some data on a connected socket.

This function is used to receive data on the datagram socket. The function call will block until data has been received successfully or an error occurs.
```c
std::size_t asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::receive(const MutableBufferSequence &buffers, socket_base::message_flags flags)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be received.
	- socket_base::message_flags `flags` Flags specifying how the receive call is to be made.

!!! note "戻り値"
	std::size_t



### receive()
Receive some data on a connected socket.

This function is used to receive data on the datagram socket. The function call will block until data has been received successfully or an error occurs.
```c
std::size_t asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::receive(const MutableBufferSequence &buffers, socket_base::message_flags flags, asio::error_code &ec)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be received.
	- socket_base::message_flags `flags` Flags specifying how the receive call is to be made.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous receive on a connected socket.

This function is used to asynchronously receive data from the datagram socket. The function call always returns immediately.
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ReadHandler, void(asio::error_code, std::size_t)) async_receive(const MutableBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ReadHandler) handler)
```

!!! summary "引数"
	- ReadHandler `` 



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous receive on a connected socket.

This function is used to asynchronously receive data from the datagram socket. The function call always returns immediately.
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ReadHandler, void(asio::error_code, std::size_t)) async_receive(const MutableBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
socket_base::message_flags asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ReadHandler) handler)
```

!!! summary "引数"
	- ReadHandler `` 

!!! note "戻り値"
	socket_base::message_flags



### receive_from()
Receive a datagram with the endpoint of the sender.

This function is used to receive a datagram. The function call will block until data has been received successfully or an error occurs.
```c
std::size_t asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::receive_from(const MutableBufferSequence &buffers, endpoint_type &sender_endpoint)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be received.
	- endpoint_type& `sender_endpoint` An endpoint object that receives the endpoint of the remote sender of the datagram.

!!! note "戻り値"
	std::size_t



### receive_from()
Receive a datagram with the endpoint of the sender.

This function is used to receive a datagram. The function call will block until data has been received successfully or an error occurs.
```c
std::size_t asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::receive_from(const MutableBufferSequence &buffers, endpoint_type &sender_endpoint, socket_base::message_flags flags)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be received.
	- endpoint_type& `sender_endpoint` An endpoint object that receives the endpoint of the remote sender of the datagram.
	- socket_base::message_flags `flags` Flags specifying how the receive call is to be made.

!!! note "戻り値"
	std::size_t



### receive_from()
Receive a datagram with the endpoint of the sender.

This function is used to receive a datagram. The function call will block until data has been received successfully or an error occurs.
```c
std::size_t asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::receive_from(const MutableBufferSequence &buffers, endpoint_type &sender_endpoint, socket_base::message_flags flags, asio::error_code &ec)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be received.
	- endpoint_type& `sender_endpoint` An endpoint object that receives the endpoint of the remote sender of the datagram.
	- socket_base::message_flags `flags` Flags specifying how the receive call is to be made.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous receive.

This function is used to asynchronously receive a datagram. The function call always returns immediately.
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ReadHandler, void(asio::error_code, std::size_t)) async_receive_from(const MutableBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
endpoint_type asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ReadHandler) handler)
```

!!! summary "引数"
	- ReadHandler `` 

!!! note "戻り値"
	endpoint_type



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous receive.

This function is used to asynchronously receive a datagram. The function call always returns immediately.
```c
asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ReadHandler, void(asio::error_code, std::size_t)) async_receive_from(const MutableBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
endpoint_type socket_base::message_flags asio::basic_datagram_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ReadHandler) handler)
```

!!! summary "引数"
	- ReadHandler `` 

!!! note "戻り値"
	endpoint_type



