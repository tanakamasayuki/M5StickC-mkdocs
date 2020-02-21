# asio::basic_stream_socket

Provides stream-oriented socket functionality. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1basic__stream__socket.html)

## メンバー







###  flags

```c
socket_base::message_flags asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::flags
```


### basic_stream_socket()
Construct a  without opening it.

This constructor creates a stream socket without opening it. The socket needs to be opened and then connected or accepted before data can be sent or received on it.
```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::basic_stream_socket(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### basic_stream_socket()
Construct and open a .

This constructor creates and opens a stream socket. The socket needs to be connected or accepted before data can be sent or received on it.
```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::basic_stream_socket(asio::io_context &io_context, const protocol_type &protocol)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `protocol` An object specifying protocol parameters to be used.



### basic_stream_socket()


Construct a , opening it and binding it to the given local endpoint. This constructor creates a stream socket and automatically opens it bound to the specified endpoint on the local machine. The protocol used is the protocol associated with the given endpoint.
```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::basic_stream_socket(asio::io_context &io_context, const endpoint_type &endpoint)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `endpoint` An endpoint on the local machine to which the stream socket will be bound.



### basic_stream_socket()
Construct a  on an existing native socket.

This constructor creates a stream socket object to hold an existing native socket.
```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::basic_stream_socket(asio::io_context &io_context, const protocol_type &protocol, const native_handle_type &native_socket)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `protocol` An object specifying protocol parameters to be used.
	- const& `native_socket` The new underlying socket implementation.



### ~basic_stream_socket()
Destroys the socket.

This function destroys the socket, cancelling any outstanding asynchronous operations associated with the socket as if by calling . 
```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::~basic_stream_socket()
```



### send()
Send some data on the socket.

This function is used to send data on the stream socket. The function call will block until one or more bytes of the data has been sent successfully, or an until error occurs.
```c
std::size_t asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::send(const ConstBufferSequence &buffers)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One or more data buffers to be sent on the socket.

!!! note "戻り値"
	std::size_t



### send()
Send some data on the socket.

This function is used to send data on the stream socket. The function call will block until one or more bytes of the data has been sent successfully, or an until error occurs.
```c
std::size_t asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::send(const ConstBufferSequence &buffers, socket_base::message_flags flags)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One or more data buffers to be sent on the socket.
	- socket_base::message_flags `flags` Flags specifying how the send call is to be made.

!!! note "戻り値"
	std::size_t



### send()
Send some data on the socket.

This function is used to send data on the stream socket. The function call will block until one or more bytes of the data has been sent successfully, or an until error occurs.
```c
std::size_t asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::send(const ConstBufferSequence &buffers, socket_base::message_flags flags, asio::error_code &ec)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One or more data buffers to be sent on the socket.
	- socket_base::message_flags `flags` Flags specifying how the send call is to be made.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous send.

This function is used to asynchronously send data on the stream socket. The function call always returns immediately.
```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(WriteHandler, void(asio::error_code, std::size_t)) async_send(const ConstBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(WriteHandler) handler)
```

!!! summary "引数"
	- WriteHandler `` 



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous send.

This function is used to asynchronously send data on the stream socket. The function call always returns immediately.
```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(WriteHandler, void(asio::error_code, std::size_t)) async_send(const ConstBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
socket_base::message_flags asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(WriteHandler) handler)
```

!!! summary "引数"
	- WriteHandler `` 

!!! note "戻り値"
	socket_base::message_flags



### receive()
Receive some data on the socket.

This function is used to receive data on the stream socket. The function call will block until one or more bytes of data has been received successfully, or until an error occurs.
```c
std::size_t asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::receive(const MutableBufferSequence &buffers)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be received.

!!! note "戻り値"
	std::size_t



### receive()
Receive some data on the socket.

This function is used to receive data on the stream socket. The function call will block until one or more bytes of data has been received successfully, or until an error occurs.
```c
std::size_t asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::receive(const MutableBufferSequence &buffers, socket_base::message_flags flags)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be received.
	- socket_base::message_flags `flags` Flags specifying how the receive call is to be made.

!!! note "戻り値"
	std::size_t



### receive()
Receive some data on a connected socket.

This function is used to receive data on the stream socket. The function call will block until one or more bytes of data has been received successfully, or until an error occurs.
```c
std::size_t asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::receive(const MutableBufferSequence &buffers, socket_base::message_flags flags, asio::error_code &ec)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be received.
	- socket_base::message_flags `flags` Flags specifying how the receive call is to be made.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous receive.

This function is used to asynchronously receive data from the stream socket. The function call always returns immediately.
```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ReadHandler, void(asio::error_code, std::size_t)) async_receive(const MutableBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ReadHandler) handler)
```

!!! summary "引数"
	- ReadHandler `` 



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous receive.

This function is used to asynchronously receive data from the stream socket. The function call always returns immediately.
```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ReadHandler, void(asio::error_code, std::size_t)) async_receive(const MutableBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
socket_base::message_flags asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ReadHandler) handler)
```

!!! summary "引数"
	- ReadHandler `` 

!!! note "戻り値"
	socket_base::message_flags



### write_some()
Write some data to the socket.

This function is used to write data to the stream socket. The function call will block until one or more bytes of the data has been written successfully, or until an error occurs.
```c
std::size_t asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::write_some(const ConstBufferSequence &buffers)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One or more data buffers to be written to the socket.

!!! note "戻り値"
	std::size_t



### write_some()
Write some data to the socket.

This function is used to write data to the stream socket. The function call will block until one or more bytes of the data has been written successfully, or until an error occurs.
```c
std::size_t asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::write_some(const ConstBufferSequence &buffers, asio::error_code &ec)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One or more data buffers to be written to the socket.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous write.

This function is used to asynchronously write data to the stream socket. The function call always returns immediately.
```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(WriteHandler, void(asio::error_code, std::size_t)) async_write_some(const ConstBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(WriteHandler) handler)
```

!!! summary "引数"
	- WriteHandler `` 



### read_some()
Read some data from the socket.

This function is used to read data from the stream socket. The function call will block until one or more bytes of data has been read successfully, or until an error occurs.
```c
std::size_t asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::read_some(const MutableBufferSequence &buffers)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be read.

!!! note "戻り値"
	std::size_t



### read_some()
Read some data from the socket.

This function is used to read data from the stream socket. The function call will block until one or more bytes of data has been read successfully, or until an error occurs.
```c
std::size_t asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::read_some(const MutableBufferSequence &buffers, asio::error_code &ec)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be read.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous read.

This function is used to asynchronously read data from the stream socket. The function call always returns immediately.
```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ReadHandler, void(asio::error_code, std::size_t)) async_read_some(const MutableBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
asio::basic_stream_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ReadHandler) handler)
```

!!! summary "引数"
	- ReadHandler `` 



