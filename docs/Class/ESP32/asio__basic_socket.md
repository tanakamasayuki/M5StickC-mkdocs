# asio::basic_socket

Provides socket functionality. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1basic__socket.html)

## メンバー











### basic_socket()
Construct a  without opening it.

This constructor creates a socket without opening it.
```c
asio::basic_socket< ASIO_SVC_TPARAM >::basic_socket(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### basic_socket()
Construct and open a .

This constructor creates and opens a socket.
```c
asio::basic_socket< ASIO_SVC_TPARAM >::basic_socket(asio::io_context &io_context, const protocol_type &protocol)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `protocol` An object specifying protocol parameters to be used.



### basic_socket()


Construct a , opening it and binding it to the given local endpoint. This constructor creates a socket and automatically opens it bound to the specified endpoint on the local machine. The protocol used is the protocol associated with the given endpoint.
```c
asio::basic_socket< ASIO_SVC_TPARAM >::basic_socket(asio::io_context &io_context, const endpoint_type &endpoint)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `endpoint` An endpoint on the local machine to which the socket will be bound.



### basic_socket()
Construct a  on an existing native socket.

This constructor creates a socket object to hold an existing native socket.
```c
asio::basic_socket< ASIO_SVC_TPARAM >::basic_socket(asio::io_context &io_context, const protocol_type &protocol, const native_handle_type &native_socket)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `protocol` An object specifying protocol parameters to be used.
	- const& `native_socket` A native socket.



### get_io_context()




```c
asio::io_context& asio::basic_socket< ASIO_SVC_TPARAM >::get_io_context()
```

!!! note "戻り値"
	asio::io_context&



### get_io_service()




```c
asio::io_context& asio::basic_socket< ASIO_SVC_TPARAM >::get_io_service()
```

!!! note "戻り値"
	asio::io_context&



### get_executor()
Get the executor associated with the object.


```c
executor_type asio::basic_socket< ASIO_SVC_TPARAM >::get_executor() ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



### lowest_layer()
Get a reference to the lowest layer.



```c
lowest_layer_type& asio::basic_socket< ASIO_SVC_TPARAM >::lowest_layer()
```

!!! note "戻り値"
	lowest_layer_type&



### lowest_layer()
Get a const reference to the lowest layer.



```c
const lowest_layer_type& asio::basic_socket< ASIO_SVC_TPARAM >::lowest_layer() const
```

!!! note "戻り値"
	const&



### open()
Open the socket using the specified protocol.

This function opens the socket so that it will use the specified protocol.
```c
void asio::basic_socket< ASIO_SVC_TPARAM >::open(const protocol_type &protocol=protocol_type())
```

!!! summary "引数"
	- const& `protocol` An object specifying protocol parameters to be used.



### open()
Open the socket using the specified protocol.

This function opens the socket so that it will use the specified protocol.
```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::open(const protocol_type &protocol, asio::error_code &ec)
```

!!! summary "引数"
	- const& `protocol` An object specifying which protocol is to be used.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### assign()
Assign an existing native socket to the socket.


```c
void asio::basic_socket< ASIO_SVC_TPARAM >::assign(const protocol_type &protocol, const native_handle_type &native_socket)
```

!!! summary "引数"
	- const& `protocol` 
	- const& `native_socket` 



### assign()
Assign an existing native socket to the socket.


```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::assign(const protocol_type &protocol, const native_handle_type &native_socket, asio::error_code &ec)
```

!!! summary "引数"
	- const& `protocol` 
	- const& `native_socket` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### is_open()
Determine whether the socket is open.


```c
bool asio::basic_socket< ASIO_SVC_TPARAM >::is_open() const
```

!!! note "戻り値"
	bool



### close()
Close the socket.

This function is used to close the socket. Any asynchronous send, receive or connect operations will be cancelled immediately, and will complete with the  error.
```c
void asio::basic_socket< ASIO_SVC_TPARAM >::close()
```



### close()
Close the socket.

This function is used to close the socket. Any asynchronous send, receive or connect operations will be cancelled immediately, and will complete with the  error.
```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::close(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any. Note that, even if the function indicates an error, the underlying descriptor is closed.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### release()
Release ownership of the underlying native socket.

This function causes all outstanding asynchronous connect, send and receive operations to finish immediately, and the handlers for cancelled operations will be passed the  error. Ownership of the native socket is then transferred to the caller.
```c
native_handle_type asio::basic_socket< ASIO_SVC_TPARAM >::release()
```

!!! note "戻り値"
	native_handle_type



### release()
Release ownership of the underlying native socket.

This function causes all outstanding asynchronous connect, send and receive operations to finish immediately, and the handlers for cancelled operations will be passed the  error. Ownership of the native socket is then transferred to the caller.
```c
native_handle_type asio::basic_socket< ASIO_SVC_TPARAM >::release(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	native_handle_type



### native_handle()
Get the native socket representation.

This function may be used to obtain the underlying representation of the socket. This is intended to allow access to native socket functionality that is not otherwise provided. 
```c
native_handle_type asio::basic_socket< ASIO_SVC_TPARAM >::native_handle()
```

!!! note "戻り値"
	native_handle_type



### cancel()
Cancel all asynchronous operations associated with the socket.



When running on Windows Vista, Windows  2008, and later, the CancelIoEx function is always used. This function does not have the problems described above. 
```c
void asio::basic_socket< ASIO_SVC_TPARAM >::cancel()
```



### cancel()
Cancel all asynchronous operations associated with the socket.



When running on Windows Vista, Windows  2008, and later, the CancelIoEx function is always used. This function does not have the problems described above. 
```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::cancel(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### at_mark()
Determine whether the socket is at the out-of-band data mark.

This function is used to check whether the socket input is currently positioned at the out-of-band data mark.
```c
bool asio::basic_socket< ASIO_SVC_TPARAM >::at_mark() const
```

!!! note "戻り値"
	bool



### at_mark()
Determine whether the socket is at the out-of-band data mark.

This function is used to check whether the socket input is currently positioned at the out-of-band data mark.
```c
bool asio::basic_socket< ASIO_SVC_TPARAM >::at_mark(asio::error_code &ec) const
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	bool



### available()
Determine the number of bytes available for reading.

This function is used to determine the number of bytes that may be read without blocking.
```c
std::size_t asio::basic_socket< ASIO_SVC_TPARAM >::available() const
```

!!! note "戻り値"
	std::size_t



### available()
Determine the number of bytes available for reading.

This function is used to determine the number of bytes that may be read without blocking.
```c
std::size_t asio::basic_socket< ASIO_SVC_TPARAM >::available(asio::error_code &ec) const
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### bind()
Bind the socket to the given local endpoint.

This function binds the socket to the specified endpoint on the local machine.
```c
void asio::basic_socket< ASIO_SVC_TPARAM >::bind(const endpoint_type &endpoint)
```

!!! summary "引数"
	- const& `endpoint` An endpoint on the local machine to which the socket will be bound.



### bind()
Bind the socket to the given local endpoint.

This function binds the socket to the specified endpoint on the local machine.
```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::bind(const endpoint_type &endpoint, asio::error_code &ec)
```

!!! summary "引数"
	- const& `endpoint` An endpoint on the local machine to which the socket will be bound.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### connect()
Connect the socket to the specified endpoint.

The socket is automatically opened if it is not already open. If the connect fails, and the socket was automatically opened, the socket is not returned to the closed state.
```c
void asio::basic_socket< ASIO_SVC_TPARAM >::connect(const endpoint_type &peer_endpoint)
```

!!! summary "引数"
	- const& `peer_endpoint` The remote endpoint to which the socket will be connected.



### connect()
Connect the socket to the specified endpoint.

The socket is automatically opened if it is not already open. If the connect fails, and the socket was automatically opened, the socket is not returned to the closed state.
```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::connect(const endpoint_type &peer_endpoint, asio::error_code &ec)
```

!!! summary "引数"
	- const& `peer_endpoint` The remote endpoint to which the socket will be connected.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous connect.

The socket is automatically opened if it is not already open. If the connect fails, and the socket was automatically opened, the socket is not returned to the closed state.
```c
asio::basic_socket< ASIO_SVC_TPARAM >::ASIO_INITFN_RESULT_TYPE(ConnectHandler, void(asio::error_code)) async_connect(const endpoint_type &peer_endpoint
```

!!! summary "引数"
	- asio::error_codevoid() `` 



### ASIO_MOVE_ARG()



```c
asio::basic_socket< ASIO_SVC_TPARAM >::ASIO_MOVE_ARG(ConnectHandler) handler)
```

!!! summary "引数"
	- ConnectHandler `` 



### set_option()
Set an option on the socket.

This function is used to set an option on the socket.
```c
void asio::basic_socket< ASIO_SVC_TPARAM >::set_option(const SettableSocketOption &option)
```

!!! summary "引数"
	- constSettableSocketOption & `option` The new option value to be set on the socket.



### set_option()
Set an option on the socket.

This function is used to set an option on the socket.
```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::set_option(const SettableSocketOption &option, asio::error_code &ec)
```

!!! summary "引数"
	- constSettableSocketOption & `option` The new option value to be set on the socket.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### get_option()
Get an option from the socket.

This function is used to get the current value of an option on the socket.
```c
void asio::basic_socket< ASIO_SVC_TPARAM >::get_option(GettableSocketOption &option) const
```

!!! summary "引数"
	- GettableSocketOption & `option` The option value to be obtained from the socket.



### get_option()
Get an option from the socket.

This function is used to get the current value of an option on the socket.
```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::get_option(GettableSocketOption &option, asio::error_code &ec) const
```

!!! summary "引数"
	- GettableSocketOption & `option` The option value to be obtained from the socket.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### io_control()
Perform an IO control command on the socket.

This function is used to execute an IO control command on the socket.
```c
void asio::basic_socket< ASIO_SVC_TPARAM >::io_control(IoControlCommand &command)
```

!!! summary "引数"
	- IoControlCommand & `command` The IO control command to be performed on the socket.



### io_control()
Perform an IO control command on the socket.

This function is used to execute an IO control command on the socket.
```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::io_control(IoControlCommand &command, asio::error_code &ec)
```

!!! summary "引数"
	- IoControlCommand & `command` The IO control command to be performed on the socket.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### non_blocking()
Gets the non-blocking mode of the socket.




```c
bool asio::basic_socket< ASIO_SVC_TPARAM >::non_blocking() const
```

!!! note "戻り値"
	bool  if the socket's synchronous operations will fail with  if they are unable to perform the requested operation immediately. If , synchronous operations will block until complete.



### non_blocking()
Sets the non-blocking mode of the socket.


```c
void asio::basic_socket< ASIO_SVC_TPARAM >::non_blocking(bool mode)
```

!!! summary "引数"
	- bool `mode` If , the socket's synchronous operations will fail with  if they are unable to perform the requested operation immediately. If , synchronous operations will block until complete.



### non_blocking()
Sets the non-blocking mode of the socket.


```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::non_blocking(bool mode, asio::error_code &ec)
```

!!! summary "引数"
	- bool `mode` If , the socket's synchronous operations will fail with  if they are unable to perform the requested operation immediately. If , synchronous operations will block until complete.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### native_non_blocking()
Gets the non-blocking mode of the native socket implementation.





```c
bool asio::basic_socket< ASIO_SVC_TPARAM >::native_non_blocking() const
```

!!! note "戻り値"
	bool



### native_non_blocking()
Sets the non-blocking mode of the native socket implementation.

This function is used to modify the non-blocking mode of the underlying native socket. It has no effect on the behaviour of the socket object's synchronous operations.
```c
void asio::basic_socket< ASIO_SVC_TPARAM >::native_non_blocking(bool mode)
```

!!! summary "引数"
	- bool `mode` If , the underlying socket is put into non-blocking mode and direct system calls may fail with  (or the equivalent system error).



### native_non_blocking()
Sets the non-blocking mode of the native socket implementation.

This function is used to modify the non-blocking mode of the underlying native socket. It has no effect on the behaviour of the socket object's synchronous operations.
```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::native_non_blocking(bool mode, asio::error_code &ec)
```

!!! summary "引数"
	- bool `mode` If , the underlying socket is put into non-blocking mode and direct system calls may fail with  (or the equivalent system error).
	- asio::error_code& `ec` Set to indicate what error occurred, if any. If the  is , but the current value of  is , this function fails with , as the combination does not make sense.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### local_endpoint()
Get the local endpoint of the socket.

This function is used to obtain the locally bound endpoint of the socket.
```c
endpoint_type asio::basic_socket< ASIO_SVC_TPARAM >::local_endpoint() const
```

!!! note "戻り値"
	endpoint_type



### local_endpoint()
Get the local endpoint of the socket.

This function is used to obtain the locally bound endpoint of the socket.
```c
endpoint_type asio::basic_socket< ASIO_SVC_TPARAM >::local_endpoint(asio::error_code &ec) const
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	endpoint_type



### remote_endpoint()
Get the remote endpoint of the socket.

This function is used to obtain the remote endpoint of the socket.
```c
endpoint_type asio::basic_socket< ASIO_SVC_TPARAM >::remote_endpoint() const
```

!!! note "戻り値"
	endpoint_type



### remote_endpoint()
Get the remote endpoint of the socket.

This function is used to obtain the remote endpoint of the socket.
```c
endpoint_type asio::basic_socket< ASIO_SVC_TPARAM >::remote_endpoint(asio::error_code &ec) const
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	endpoint_type



### shutdown()
Disable sends or receives on the socket.

This function is used to disable send operations, receive operations, or both.
```c
void asio::basic_socket< ASIO_SVC_TPARAM >::shutdown(shutdown_type what)
```

!!! summary "引数"
	- shutdown_type `what` Determines what types of operation will no longer be allowed.



### shutdown()
Disable sends or receives on the socket.

This function is used to disable send operations, receive operations, or both.
```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::shutdown(shutdown_type what, asio::error_code &ec)
```

!!! summary "引数"
	- shutdown_type `what` Determines what types of operation will no longer be allowed.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### wait()


Wait for the socket to become ready to read, ready to write, or to have pending error conditions. This function is used to perform a blocking wait for a socket to enter a ready to read, write or error condition state.
```c
void asio::basic_socket< ASIO_SVC_TPARAM >::wait(wait_type w)
```

!!! summary "引数"
	- wait_type `w` Specifies the desired socket state.



### wait()


Wait for the socket to become ready to read, ready to write, or to have pending error conditions. This function is used to perform a blocking wait for a socket to enter a ready to read, write or error condition state.
```c
ASIO_SYNC_OP_VOID asio::basic_socket< ASIO_SVC_TPARAM >::wait(wait_type w, asio::error_code &ec)
```

!!! summary "引数"
	- wait_type `w` Specifies the desired socket state.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### ASIO_INITFN_RESULT_TYPE()


Asynchronously wait for the socket to become ready to read, ready to write, or to have pending error conditions. This function is used to perform an asynchronous wait for a socket to enter a ready to read, write or error condition state.
```c
asio::basic_socket< ASIO_SVC_TPARAM >::ASIO_INITFN_RESULT_TYPE(WaitHandler, void(asio::error_code)) async_wait(wait_type w
```

!!! summary "引数"
	- asio::error_codevoid() `` 



### ASIO_MOVE_ARG()



```c
asio::basic_socket< ASIO_SVC_TPARAM >::ASIO_MOVE_ARG(WaitHandler) handler)
```

!!! summary "引数"
	- WaitHandler `` 



