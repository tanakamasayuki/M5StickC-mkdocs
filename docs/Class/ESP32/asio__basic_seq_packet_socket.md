# asio::basic_seq_packet_socket

Provides sequenced packet socket functionality. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1basic__seq__packet__socket.html)

## メンバー







###  flags

```c
socket_base::message_flags asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::flags
```


###  out_flags

```c
socket_base::message_flags& asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::out_flags
```


###  in_flags

```c
socket_base::message_flags asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::in_flags
```


###  out_flags

```c
socket_base::message_flags socket_base::message_flags& asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::out_flags
```


### basic_seq_packet_socket()
Construct a  without opening it.

This constructor creates a sequenced packet socket without opening it. The socket needs to be opened and then connected or accepted before data can be sent or received on it.
```c
asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::basic_seq_packet_socket(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### basic_seq_packet_socket()
Construct and open a .

This constructor creates and opens a sequenced_packet socket. The socket needs to be connected or accepted before data can be sent or received on it.
```c
asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::basic_seq_packet_socket(asio::io_context &io_context, const protocol_type &protocol)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `protocol` An object specifying protocol parameters to be used.



### basic_seq_packet_socket()


Construct a , opening it and binding it to the given local endpoint. This constructor creates a sequenced packet socket and automatically opens it bound to the specified endpoint on the local machine. The protocol used is the protocol associated with the given endpoint.
```c
asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::basic_seq_packet_socket(asio::io_context &io_context, const endpoint_type &endpoint)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `endpoint` An endpoint on the local machine to which the sequenced packet socket will be bound.



### basic_seq_packet_socket()
Construct a  on an existing native socket.

This constructor creates a sequenced packet socket object to hold an existing native socket.
```c
asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::basic_seq_packet_socket(asio::io_context &io_context, const protocol_type &protocol, const native_handle_type &native_socket)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `protocol` An object specifying protocol parameters to be used.
	- const& `native_socket` The new underlying socket implementation.



### ~basic_seq_packet_socket()
Destroys the socket.

This function destroys the socket, cancelling any outstanding asynchronous operations associated with the socket as if by calling . 
```c
asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::~basic_seq_packet_socket()
```



### send()
Send some data on the socket.

This function is used to send data on the sequenced packet socket. The function call will block until the data has been sent successfully, or an until error occurs.
```c
std::size_t asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::send(const ConstBufferSequence &buffers, socket_base::message_flags flags)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One or more data buffers to be sent on the socket.
	- socket_base::message_flags `flags` Flags specifying how the send call is to be made.

!!! note "戻り値"
	std::size_t



### send()
Send some data on the socket.

This function is used to send data on the sequenced packet socket. The function call will block the data has been sent successfully, or an until error occurs.
```c
std::size_t asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::send(const ConstBufferSequence &buffers, socket_base::message_flags flags, asio::error_code &ec)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` One or more data buffers to be sent on the socket.
	- socket_base::message_flags `flags` Flags specifying how the send call is to be made.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous send.

This function is used to asynchronously send data on the sequenced packet socket. The function call always returns immediately.
```c
asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(WriteHandler, void(asio::error_code, std::size_t)) async_send(const ConstBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
socket_base::message_flags asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(WriteHandler) handler)
```

!!! summary "引数"
	- WriteHandler `` 

!!! note "戻り値"
	socket_base::message_flags



### receive()
Receive some data on the socket.

This function is used to receive data on the sequenced packet socket. The function call will block until data has been received successfully, or until an error occurs.
```c
std::size_t asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::receive(const MutableBufferSequence &buffers, socket_base::message_flags &out_flags)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be received.
	- socket_base::message_flags& `out_flags` After the receive call completes, contains flags associated with the received data. For example, if the socket_base::message_end_of_record bit is set then the received data marks the end of a record.

!!! note "戻り値"
	std::size_t



### receive()
Receive some data on the socket.

This function is used to receive data on the sequenced packet socket. The function call will block until data has been received successfully, or until an error occurs.
```c
std::size_t asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::receive(const MutableBufferSequence &buffers, socket_base::message_flags in_flags, socket_base::message_flags &out_flags)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be received.
	- socket_base::message_flags `in_flags` Flags specifying how the receive call is to be made.
	- socket_base::message_flags& `out_flags` After the receive call completes, contains flags associated with the received data. For example, if the socket_base::message_end_of_record bit is set then the received data marks the end of a record.

!!! note "戻り値"
	std::size_t



### receive()
Receive some data on a connected socket.

This function is used to receive data on the sequenced packet socket. The function call will block until data has been received successfully, or until an error occurs.
```c
std::size_t asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::receive(const MutableBufferSequence &buffers, socket_base::message_flags in_flags, socket_base::message_flags &out_flags, asio::error_code &ec)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` One or more buffers into which the data will be received.
	- socket_base::message_flags `in_flags` Flags specifying how the receive call is to be made.
	- socket_base::message_flags& `out_flags` After the receive call completes, contains flags associated with the received data. For example, if the socket_base::message_end_of_record bit is set then the received data marks the end of a record.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous receive.

This function is used to asynchronously receive data from the sequenced packet socket. The function call always returns immediately.
```c
asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ReadHandler, void(asio::error_code, std::size_t)) async_receive(const MutableBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
socket_base::message_flags asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ReadHandler) handler)
```

!!! summary "引数"
	- ReadHandler `` 

!!! note "戻り値"
	socket_base::message_flags



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous receive.

This function is used to asynchronously receive data from the sequenced data socket. The function call always returns immediately.
```c
asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(ReadHandler, void(asio::error_code, std::size_t)) async_receive(const MutableBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
socket_base::message_flags socket_base::message_flags asio::basic_seq_packet_socket< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(ReadHandler) handler)
```

!!! summary "引数"
	- ReadHandler `` 

!!! note "戻り値"
	socket_base::message_flags



