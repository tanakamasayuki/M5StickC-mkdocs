# asio::basic_socket_acceptor

Provides the ability to accept new connections. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1basic__socket__acceptor.html)

## メンバー









### basic_socket_acceptor()
Construct an acceptor without opening it.

This constructor creates an acceptor without opening it to listen for new connections. The  function must be called before the acceptor can accept new socket connections.
```c
asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::basic_socket_acceptor(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### basic_socket_acceptor()
Construct an open acceptor.

This constructor creates an acceptor and automatically opens it.
```c
asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::basic_socket_acceptor(asio::io_context &io_context, const protocol_type &protocol)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `protocol` An object specifying protocol parameters to be used.



### basic_socket_acceptor()
Construct an acceptor opened on the given endpoint.

This constructor creates an acceptor and automatically opens it to listen for new connections on the specified endpoint.
```c
asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::basic_socket_acceptor(asio::io_context &io_context, const endpoint_type &endpoint, bool reuse_addr=true)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `endpoint` An endpoint on the local machine on which the acceptor will listen for new connections.
	- bool `reuse_addr` Whether the constructor should set the socket option .



### basic_socket_acceptor()
Construct a  on an existing native acceptor.

This constructor creates an acceptor object to hold an existing native acceptor.
```c
asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::basic_socket_acceptor(asio::io_context &io_context, const protocol_type &protocol, const native_handle_type &native_acceptor)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `protocol` An object specifying protocol parameters to be used.
	- const& `native_acceptor` A native acceptor.



### ~basic_socket_acceptor()
Destroys the acceptor.

This function destroys the acceptor, cancelling any outstanding asynchronous operations associated with the acceptor as if by calling . 
```c
asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::~basic_socket_acceptor()
```



### get_io_context()




```c
asio::io_context& asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::get_io_context()
```

!!! note "戻り値"
	asio::io_context&



### get_io_service()




```c
asio::io_context& asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::get_io_service()
```

!!! note "戻り値"
	asio::io_context&



### get_executor()
Get the executor associated with the object.


```c
executor_type asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::get_executor() ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



### open()
Open the acceptor using the specified protocol.

This function opens the socket acceptor so that it will use the specified protocol.
```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::open(const protocol_type &protocol=protocol_type())
```

!!! summary "引数"
	- const& `protocol` An object specifying which protocol is to be used.



### open()
Open the acceptor using the specified protocol.

This function opens the socket acceptor so that it will use the specified protocol.
```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::open(const protocol_type &protocol, asio::error_code &ec)
```

!!! summary "引数"
	- const& `protocol` An object specifying which protocol is to be used.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### assign()
Assigns an existing native acceptor to the acceptor.


```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::assign(const protocol_type &protocol, const native_handle_type &native_acceptor)
```

!!! summary "引数"
	- const& `protocol` 
	- const& `native_acceptor` 



### assign()
Assigns an existing native acceptor to the acceptor.


```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::assign(const protocol_type &protocol, const native_handle_type &native_acceptor, asio::error_code &ec)
```

!!! summary "引数"
	- const& `protocol` 
	- const& `native_acceptor` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### is_open()
Determine whether the acceptor is open.


```c
bool asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::is_open() const
```

!!! note "戻り値"
	bool



### bind()
Bind the acceptor to the given local endpoint.

This function binds the socket acceptor to the specified endpoint on the local machine.
```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::bind(const endpoint_type &endpoint)
```

!!! summary "引数"
	- const& `endpoint` An endpoint on the local machine to which the socket acceptor will be bound.



### bind()
Bind the acceptor to the given local endpoint.

This function binds the socket acceptor to the specified endpoint on the local machine.
```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::bind(const endpoint_type &endpoint, asio::error_code &ec)
```

!!! summary "引数"
	- const& `endpoint` An endpoint on the local machine to which the socket acceptor will be bound.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### listen()


Place the acceptor into the state where it will listen for new connections. This function puts the socket acceptor into the state where it may accept new connections.
```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::listen(int backlog=socket_base::max_listen_connections)
```

!!! summary "引数"
	- int `backlog` The maximum length of the queue of pending connections.



### listen()


Place the acceptor into the state where it will listen for new connections. This function puts the socket acceptor into the state where it may accept new connections.
```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::listen(int backlog, asio::error_code &ec)
```

!!! summary "引数"
	- int `backlog` The maximum length of the queue of pending connections.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### close()
Close the acceptor.

A subsequent call to  is required before the acceptor can again be used to again perform socket accept operations.
```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::close()
```



### close()
Close the acceptor.

A subsequent call to  is required before the acceptor can again be used to again perform socket accept operations.
```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::close(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### release()
Release ownership of the underlying native acceptor.

This function causes all outstanding asynchronous accept operations to finish immediately, and the handlers for cancelled operations will be passed the  error. Ownership of the native acceptor is then transferred to the caller.
```c
native_handle_type asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::release()
```

!!! note "戻り値"
	native_handle_type



### release()
Release ownership of the underlying native acceptor.

This function causes all outstanding asynchronous accept operations to finish immediately, and the handlers for cancelled operations will be passed the  error. Ownership of the native acceptor is then transferred to the caller.
```c
native_handle_type asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::release(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	native_handle_type



### native_handle()
Get the native acceptor representation.

This function may be used to obtain the underlying representation of the acceptor. This is intended to allow access to native acceptor functionality that is not otherwise provided. 
```c
native_handle_type asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::native_handle()
```

!!! note "戻り値"
	native_handle_type



### cancel()
Cancel all asynchronous operations associated with the acceptor.

This function causes all outstanding asynchronous connect, send and receive operations to finish immediately, and the handlers for cancelled operations will be passed the  error.
```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::cancel()
```



### cancel()
Cancel all asynchronous operations associated with the acceptor.

This function causes all outstanding asynchronous connect, send and receive operations to finish immediately, and the handlers for cancelled operations will be passed the  error.
```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::cancel(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any. 

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### set_option()
Set an option on the acceptor.

This function is used to set an option on the acceptor.
```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::set_option(const SettableSocketOption &option)
```

!!! summary "引数"
	- constSettableSocketOption & `option` The new option value to be set on the acceptor.



### set_option()
Set an option on the acceptor.

This function is used to set an option on the acceptor.
```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::set_option(const SettableSocketOption &option, asio::error_code &ec)
```

!!! summary "引数"
	- constSettableSocketOption & `option` The new option value to be set on the acceptor.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### get_option()
Get an option from the acceptor.

This function is used to get the current value of an option on the acceptor.
```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::get_option(GettableSocketOption &option) const
```

!!! summary "引数"
	- GettableSocketOption & `option` The option value to be obtained from the acceptor.



### get_option()
Get an option from the acceptor.

This function is used to get the current value of an option on the acceptor.
```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::get_option(GettableSocketOption &option, asio::error_code &ec) const
```

!!! summary "引数"
	- GettableSocketOption & `option` The option value to be obtained from the acceptor.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### io_control()
Perform an IO control command on the acceptor.

This function is used to execute an IO control command on the acceptor.
```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::io_control(IoControlCommand &command)
```

!!! summary "引数"
	- IoControlCommand & `command` The IO control command to be performed on the acceptor.



### io_control()
Perform an IO control command on the acceptor.

This function is used to execute an IO control command on the acceptor.
```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::io_control(IoControlCommand &command, asio::error_code &ec)
```

!!! summary "引数"
	- IoControlCommand & `command` The IO control command to be performed on the acceptor.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### non_blocking()
Gets the non-blocking mode of the acceptor.




```c
bool asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::non_blocking() const
```

!!! note "戻り値"
	bool  if the acceptor's synchronous operations will fail with  if they are unable to perform the requested operation immediately. If , synchronous operations will block until complete.



### non_blocking()
Sets the non-blocking mode of the acceptor.


```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::non_blocking(bool mode)
```

!!! summary "引数"
	- bool `mode` If , the acceptor's synchronous operations will fail with  if they are unable to perform the requested operation immediately. If , synchronous operations will block until complete.



### non_blocking()
Sets the non-blocking mode of the acceptor.


```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::non_blocking(bool mode, asio::error_code &ec)
```

!!! summary "引数"
	- bool `mode` If , the acceptor's synchronous operations will fail with  if they are unable to perform the requested operation immediately. If , synchronous operations will block until complete.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### native_non_blocking()
Gets the non-blocking mode of the native acceptor implementation.




```c
bool asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::native_non_blocking() const
```

!!! note "戻り値"
	bool



### native_non_blocking()
Sets the non-blocking mode of the native acceptor implementation.

This function is used to modify the non-blocking mode of the underlying native acceptor. It has no effect on the behaviour of the acceptor object's synchronous operations.
```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::native_non_blocking(bool mode)
```

!!! summary "引数"
	- bool `mode` If , the underlying acceptor is put into non-blocking mode and direct system calls may fail with  (or the equivalent system error).



### native_non_blocking()
Sets the non-blocking mode of the native acceptor implementation.

This function is used to modify the non-blocking mode of the underlying native acceptor. It has no effect on the behaviour of the acceptor object's synchronous operations.
```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::native_non_blocking(bool mode, asio::error_code &ec)
```

!!! summary "引数"
	- bool `mode` If , the underlying acceptor is put into non-blocking mode and direct system calls may fail with  (or the equivalent system error).
	- asio::error_code& `ec` Set to indicate what error occurred, if any. If the  is , but the current value of  is , this function fails with , as the combination does not make sense. 

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### local_endpoint()
Get the local endpoint of the acceptor.

This function is used to obtain the locally bound endpoint of the acceptor.
```c
endpoint_type asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::local_endpoint() const
```

!!! note "戻り値"
	endpoint_type



### local_endpoint()
Get the local endpoint of the acceptor.

This function is used to obtain the locally bound endpoint of the acceptor.
```c
endpoint_type asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::local_endpoint(asio::error_code &ec) const
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	endpoint_type



### wait()


Wait for the acceptor to become ready to read, ready to write, or to have pending error conditions. This function is used to perform a blocking wait for an acceptor to enter a ready to read, write or error condition state.
```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::wait(wait_type w)
```

!!! summary "引数"
	- wait_type `w` Specifies the desired acceptor state.



### wait()


Wait for the acceptor to become ready to read, ready to write, or to have pending error conditions. This function is used to perform a blocking wait for an acceptor to enter a ready to read, write or error condition state.
```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::wait(wait_type w, asio::error_code &ec)
```

!!! summary "引数"
	- wait_type `w` Specifies the desired acceptor state.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### ASIO_INITFN_RESULT_TYPE()


Asynchronously wait for the acceptor to become ready to read, ready to write, or to have pending error conditions. This function is used to perform an asynchronous wait for an acceptor to enter a ready to read, write or error condition state.
```c
asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(WaitHandler, void(asio::error_code)) async_wait(wait_type w
```

!!! summary "引数"
	- asio::error_codevoid() `` 



### ASIO_MOVE_ARG()



```c
asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(WaitHandler) handler)
```

!!! summary "引数"
	- WaitHandler `` 



### accept()
Accept a new connection.

This function is used to accept a new connection from a peer into the given socket. The function call will block until a new connection has been accepted successfully or an error occurs.
```c
void asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::accept(basic_socket< Protocol1 > &peer, typename enable_if< is_convertible< Protocol, Protocol1 >::value >::type *=0)
```

!!! summary "引数"
	- basic_socket< Protocol1 > & `peer` The socket into which the new connection will be accepted.
	- enable_iftypename < is_convertible< Protocol, Protocol1 >:: >::type * `` 



### accept()
Accept a new connection.

This function is used to accept a new connection from a peer into the given socket. The function call will block until a new connection has been accepted successfully or an error occurs.
```c
ASIO_SYNC_OP_VOID asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::accept(basic_socket< Protocol1 > &peer, asio::error_code &ec, typename enable_if< is_convertible< Protocol, Protocol1 >::value >::type *=0)
```

!!! summary "引数"
	- basic_socket< Protocol1 > & `peer` The socket into which the new connection will be accepted.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.
	- enable_iftypename < is_convertible< Protocol, Protocol1 >:: >::type * `` 

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous accept.

This function is used to asynchronously accept a new connection into a socket. The function call always returns immediately.
```c
asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::ASIO_INITFN_RESULT_TYPE(AcceptHandler, void(asio::error_code)) async_accept(basic_socket< Protocol1 > &peer
```

!!! summary "引数"
	- asio::error_codevoid() `` 



### ASIO_MOVE_ARG()



```c
asio::basic_socket_acceptor< ASIO_SVC_TPARAM_DEF1 >::ASIO_MOVE_ARG(AcceptHandler) handler
```

!!! summary "引数"
	- AcceptHandler `` 



