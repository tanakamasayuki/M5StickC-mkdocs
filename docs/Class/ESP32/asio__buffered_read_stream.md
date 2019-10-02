# asio::buffered_read_stream

Adds buffering to the read-related operations of a stream. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1buffered__read__stream.html)

## メンバー







### ASIO_STATIC_CONSTANT()



```c
asio::buffered_read_stream< Stream >::ASIO_STATIC_CONSTANT(std::size_t, default_buffer_size=1024)
```

!!! summary "引数"
	- default_buffer_size `` 



### buffered_read_stream()
Construct, passing the specified argument to initialise the next layer.


```c
asio::buffered_read_stream< Stream >::buffered_read_stream(Arg &a)
```

!!! summary "引数"
	- Arg & `a` 



### buffered_read_stream()
Construct, passing the specified argument to initialise the next layer.


```c
asio::buffered_read_stream< Stream >::buffered_read_stream(Arg &a, std::size_t buffer_size)
```

!!! summary "引数"
	- Arg & `a` 
	- std::size_t `buffer_size` 



### next_layer()
Get a reference to the next layer.


```c
next_layer_type& asio::buffered_read_stream< Stream >::next_layer()
```

!!! note "戻り値"
	next_layer_type&



### lowest_layer()
Get a reference to the lowest layer.


```c
lowest_layer_type& asio::buffered_read_stream< Stream >::lowest_layer()
```

!!! note "戻り値"
	lowest_layer_type&



### lowest_layer()
Get a const reference to the lowest layer.


```c
const lowest_layer_type& asio::buffered_read_stream< Stream >::lowest_layer() const
```

!!! note "戻り値"
	const&



### get_executor()
Get the executor associated with the object.


```c
executor_type asio::buffered_read_stream< Stream >::get_executor() ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



### get_io_context()


(Deprecated: Use .) Get the  associated with the object. 
```c
asio::io_context& asio::buffered_read_stream< Stream >::get_io_context()
```

!!! note "戻り値"
	asio::io_context&



### get_io_service()


(Deprecated: Use .) Get the  associated with the object. 
```c
asio::io_context& asio::buffered_read_stream< Stream >::get_io_service()
```

!!! note "戻り値"
	asio::io_context&



### close()
Close the stream.


```c
void asio::buffered_read_stream< Stream >::close()
```



### close()
Close the stream.


```c
ASIO_SYNC_OP_VOID asio::buffered_read_stream< Stream >::close(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### write_some()


Write the given data to the stream. Returns the number of bytes written. Throws an exception on failure. 
```c
std::size_t asio::buffered_read_stream< Stream >::write_some(const ConstBufferSequence &buffers)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` 

!!! note "戻り値"
	std::size_t



### write_some()


Write the given data to the stream. Returns the number of bytes written, or 0 if an error occurred. 
```c
std::size_t asio::buffered_read_stream< Stream >::write_some(const ConstBufferSequence &buffers, asio::error_code &ec)
```

!!! summary "引数"
	- constConstBufferSequence & `buffers` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()


Start an asynchronous write. The data being written must be valid for the lifetime of the asynchronous operation. 
```c
asio::buffered_read_stream< Stream >::ASIO_INITFN_RESULT_TYPE(WriteHandler, void(asio::error_code, std::size_t)) async_write_some(const ConstBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
asio::buffered_read_stream< Stream >::ASIO_MOVE_ARG(WriteHandler) handler)
```

!!! summary "引数"
	- WriteHandler `` 



### fill()


Fill the buffer with some data. Returns the number of bytes placed in the buffer as a result of the operation. Throws an exception on failure. 
```c
std::size_t asio::buffered_read_stream< Stream >::fill()
```

!!! note "戻り値"
	std::size_t



### fill()


Fill the buffer with some data. Returns the number of bytes placed in the buffer as a result of the operation, or 0 if an error occurred. 
```c
std::size_t asio::buffered_read_stream< Stream >::fill(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous fill.


```c
asio::buffered_read_stream< Stream >::ASIO_INITFN_RESULT_TYPE(ReadHandler, void(asio::error_code, std::size_t)) async_fill(ASIO_MOVE_ARG(ReadHandler) handler)
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### read_some()


Read some data from the stream. Returns the number of bytes read. Throws an exception on failure. 
```c
std::size_t asio::buffered_read_stream< Stream >::read_some(const MutableBufferSequence &buffers)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` 

!!! note "戻り値"
	std::size_t



### read_some()


Read some data from the stream. Returns the number of bytes read or 0 if an error occurred. 
```c
std::size_t asio::buffered_read_stream< Stream >::read_some(const MutableBufferSequence &buffers, asio::error_code &ec)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	std::size_t



### ASIO_INITFN_RESULT_TYPE()


Start an asynchronous read. The buffer into which the data will be read must be valid for the lifetime of the asynchronous operation. 
```c
asio::buffered_read_stream< Stream >::ASIO_INITFN_RESULT_TYPE(ReadHandler, void(asio::error_code, std::size_t)) async_read_some(const MutableBufferSequence &buffers
```

!!! summary "引数"
	- asio::error_codevoid(, std::size_t) `` 



### ASIO_MOVE_ARG()



```c
asio::buffered_read_stream< Stream >::ASIO_MOVE_ARG(ReadHandler) handler)
```

!!! summary "引数"
	- ReadHandler `` 



### peek()


Peek at the incoming data on the stream. Returns the number of bytes read. Throws an exception on failure. 
```c
std::size_t asio::buffered_read_stream< Stream >::peek(const MutableBufferSequence &buffers)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` 

!!! note "戻り値"
	std::size_t



### peek()


Peek at the incoming data on the stream. Returns the number of bytes read, or 0 if an error occurred. 
```c
std::size_t asio::buffered_read_stream< Stream >::peek(const MutableBufferSequence &buffers, asio::error_code &ec)
```

!!! summary "引数"
	- constMutableBufferSequence & `buffers` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	std::size_t



### in_avail()
Determine the amount of data that may be read without blocking.


```c
std::size_t asio::buffered_read_stream< Stream >::in_avail()
```

!!! note "戻り値"
	std::size_t



### in_avail()
Determine the amount of data that may be read without blocking.


```c
std::size_t asio::buffered_read_stream< Stream >::in_avail(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` 

!!! note "戻り値"
	std::size_t



