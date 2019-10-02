# asio::ssl::stream

Provides stream-oriented functionality using SSL. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ssl_1_1stream.html)

## メンバー









###  buffers

```c
const ConstBufferSequence& asio::ssl::stream< Stream >::buffers
```


### stream()



```c
asio::ssl::stream< Stream >::stream(Arg &arg, context &ctx)
```

!!! summary "引数"
	- Arg & `arg` 
	- context& `ctx` 



### ~stream()
Destructor.



```c
asio::ssl::stream< Stream >::~stream()
```



### get_executor()
Get the executor associated with the object.



```c
executor_type asio::ssl::stream< Stream >::get_executor() ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



### get_io_context()


(Deprecated: Use .) Get the  associated with the object. 
```c
asio::io_context& asio::ssl::stream< Stream >::get_io_context()
```

!!! note "戻り値"
	asio::io_context&



### get_io_service()


(Deprecated: Use .) Get the  associated with the object. 
```c
asio::io_context& asio::ssl::stream< Stream >::get_io_service()
```

!!! note "戻り値"
	asio::io_context&



### native_handle()
Get the underlying implementation in the native type.



```c
native_handle_type asio::ssl::stream< Stream >::native_handle()
```

!!! note "戻り値"
	native_handle_type



### next_layer()
Get a reference to the next layer.



```c
const next_layer_type& asio::ssl::stream< Stream >::next_layer() const
```

!!! note "戻り値"
	const&



### next_layer()
Get a reference to the next layer.



```c
next_layer_type& asio::ssl::stream< Stream >::next_layer()
```

!!! note "戻り値"
	next_layer_type&



### lowest_layer()
Get a reference to the lowest layer.



```c
lowest_layer_type& asio::ssl::stream< Stream >::lowest_layer()
```

!!! note "戻り値"
	lowest_layer_type&



### lowest_layer()
Get a reference to the lowest layer.



```c
const lowest_layer_type& asio::ssl::stream< Stream >::lowest_layer() const
```

!!! note "戻り値"
	const&



### set_verify_mode()
Set the peer verification mode.

This function may be used to configure the peer verification mode used by the stream. The new mode will override the mode inherited from the context.
```c
void asio::ssl::stream< Stream >::set_verify_mode(verify_mode v)
```

!!! summary "引数"
	- verify_mode `v` A bitmask of peer verification modes. See  for available values.



### set_verify_mode()
Set the peer verification mode.

This function may be used to configure the peer verification mode used by the stream. The new mode will override the mode inherited from the context.
```c
ASIO_SYNC_OP_VOID asio::ssl::stream< Stream >::set_verify_mode(verify_mode v, asio::error_code &ec)
```

!!! summary "引数"
	- verify_mode `v` A bitmask of peer verification modes. See  for available values.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### set_verify_depth()
Set the peer verification depth.

This function may be used to configure the maximum verification depth allowed by the stream.
```c
void asio::ssl::stream< Stream >::set_verify_depth(int depth)
```

!!! summary "引数"
	- int `depth` Maximum depth for the certificate chain verification that shall be allowed.



### set_verify_depth()
Set the peer verification depth.

This function may be used to configure the maximum verification depth allowed by the stream.
```c
ASIO_SYNC_OP_VOID asio::ssl::stream< Stream >::set_verify_depth(int depth, asio::error_code &ec)
```

!!! summary "引数"
	- int `depth` Maximum depth for the certificate chain verification that shall be allowed.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### set_verify_callback()
Set the callback used to verify peer certificates.

This function is used to specify a callback function that will be called by the implementation when it needs to verify a peer certificate.
```c
void asio::ssl::stream< Stream >::set_verify_callback(VerifyCallback callback)
```

!!! summary "引数"
	- VerifyCallback `callback` The function object to be used for verifying a certificate. The function signature of the handler must be:  The return value of the callback is true if the certificate has passed verification, false otherwise.



### set_verify_callback()
Set the callback used to verify peer certificates.

This function is used to specify a callback function that will be called by the implementation when it needs to verify a peer certificate.
```c
ASIO_SYNC_OP_VOID asio::ssl::stream< Stream >::set_verify_callback(VerifyCallback callback, asio::error_code &ec)
```

!!! summary "引数"
	- VerifyCallback `callback` The function object to be used for verifying a certificate. The function signature of the handler must be:  The return value of the callback is true if the certificate has passed verification, false otherwise.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### handshake()
Perform SSL handshaking.

This function is used to perform SSL handshaking on the stream. The function call will block until handshaking is complete or an error occurs.
```c
void asio::ssl::stream< Stream >::handshake(handshake_type type)
```

!!! summary "引数"
	- handshake_type `type` The type of handshaking to be performed, i.e. as a client or as a server.



### handshake()
Perform SSL handshaking.

This function is used to perform SSL handshaking on the stream. The function call will block until handshaking is complete or an error occurs.
```c
ASIO_SYNC_OP_VOID asio::ssl::stream< Stream >::handshake(handshake_type type, asio::error_code &ec)
```

!!! summary "引数"
	- handshake_type `type` The type of handshaking to be performed, i.e. as a client or as a server.
	- asio::error_code& `ec` Set to indicate what error occurred, if any. 

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### handshake()
Perform SSL handshaking.

This function is used to perform SSL handshaking on the stream. The function call will block until handshaking is complete or an error occurs.
```c
void asio::ssl::stream< Stream >::handshake(handshake_type type, const ConstBufferSequence &buffers)
```

!!! summary "引数"
	- handshake_type `type` The type of handshaking to be performed, i.e. as a client or as a server.
	- constConstBufferSequence & `buffers` The buffered data to be reused for the handshake.



### handshake()
Perform SSL handshaking.

This function is used to perform SSL handshaking on the stream. The function call will block until handshaking is complete or an error occurs.
```c
ASIO_SYNC_OP_VOID asio::ssl::stream< Stream >::handshake(handshake_type type, const ConstBufferSequence &buffers, asio::error_code &ec)
```

!!! summary "引数"
	- handshake_type `type` The type of handshaking to be performed, i.e. as a client or as a server.
	- constConstBufferSequence & `buffers` The buffered data to be reused for the handshake.
	- asio::error_code& `ec` Set to indicate what error occurred, if any. 

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous SSL handshake.

This function is used to asynchronously perform an SSL handshake on the stream. This function call always returns immediately.
```c
asio::ssl::stream< Stream >::ASIO_INITFN_RESULT_TYPE(HandshakeHandler, void(asio::error_code)) async_handshake(handshake_type type
```

!!! summary "引数"
	- asio::error_codevoid() `` 



### ASIO_MOVE_ARG()



```c
asio::ssl::stream< Stream >::ASIO_MOVE_ARG(HandshakeHandler) handler)
```

!!! summary "引数"
	- HandshakeHandler `` 



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous SSL handshake.

This function is used to asynchronously perform an SSL handshake on the stream. This function call always returns immediately.
```c
asio::ssl::stream< Stream >::ASIO_INITFN_RESULT_TYPE(BufferedHandshakeHandler, void(asio::error_code, std::size_t)) async_handshake(handshake_type type
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
const ConstBufferSequence asio::ssl::stream< Stream >::ASIO_MOVE_ARG(BufferedHandshakeHandler) handler)
```

!!! summary "引数"
	- BufferedHandshakeHandler `` 

!!! note "戻り値"
	constConstBufferSequence



### shutdown()
Shut down SSL on the stream.

This function is used to shut down SSL on the stream. The function call will block until SSL has been shut down or an error occurs.
```c
void asio::ssl::stream< Stream >::shutdown()
```



### shutdown()
Shut down SSL on the stream.

This function is used to shut down SSL on the stream. The function call will block until SSL has been shut down or an error occurs.
```c
ASIO_SYNC_OP_VOID asio::ssl::stream< Stream >::shutdown(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any. 

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### ASIO_INITFN_RESULT_TYPE()
Asynchronously shut down SSL on the stream.

This function is used to asynchronously shut down SSL on the stream. This function call always returns immediately.
```c
asio::ssl::stream< Stream >::ASIO_INITFN_RESULT_TYPE(ShutdownHandler, void(asio::error_code)) async_shutdown(ASIO_MOVE_ARG(ShutdownHandler) handler)
```

!!! summary "引数"
	- asio::error_codevoid() `` 



### write_some()
Write some data to the stream.

This function is used to write data on the stream. The function call will block until one or more bytes of data has been written successfully, or until an error occurs.
```c
std::size_t asio::ssl::stream< Stream >::write_some(const ConstBufferSequence &buffers)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` The data to be written.

!!! note "戻り値"
	std::size_t



### write_some()
Write some data to the stream.

This function is used to write data on the stream. The function call will block until one or more bytes of data has been written successfully, or until an error occurs.
```c
std::size_t asio::ssl::stream< Stream >::write_some(const ConstBufferSequence &buffers, asio::error_code &ec)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` The data to be written to the stream.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous write.

This function is used to asynchronously write one or more bytes of data to the stream. The function call always returns immediately.
```c
asio::ssl::stream< Stream >::ASIO_INITFN_RESULT_TYPE(WriteHandler, void(asio::error_code, std::size_t)) async_write_some(const ConstBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
asio::ssl::stream< Stream >::ASIO_MOVE_ARG(WriteHandler) handler)
```

!!! summary "引数"
	- WriteHandler `` 



### read_some()
Read some data from the stream.

This function is used to read data from the stream. The function call will block until one or more bytes of data has been read successfully, or until an error occurs.
```c
std::size_t asio::ssl::stream< Stream >::read_some(const MutableBufferSequence &buffers)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` The buffers into which the data will be read.

!!! note "戻り値"
	std::size_t



### read_some()
Read some data from the stream.

This function is used to read data from the stream. The function call will block until one or more bytes of data has been read successfully, or until an error occurs.
```c
std::size_t asio::ssl::stream< Stream >::read_some(const MutableBufferSequence &buffers, asio::error_code &ec)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` The buffers into which the data will be read.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous read.

This function is used to asynchronously read one or more bytes of data from the stream. The function call always returns immediately.
```c
asio::ssl::stream< Stream >::ASIO_INITFN_RESULT_TYPE(ReadHandler, void(asio::error_code, std::size_t)) async_read_some(const MutableBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
asio::ssl::stream< Stream >::ASIO_MOVE_ARG(ReadHandler) handler)
```

!!! summary "引数"
	- ReadHandler `` 



