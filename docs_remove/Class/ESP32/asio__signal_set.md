# asio::signal_set

Provides signal functionality. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1signal__set.html)

## メンバー



### signal_set()
Construct a signal set without adding any signals.

This constructor creates a signal set without registering for any signals.
```c
asio::signal_set::signal_set(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### signal_set()
Construct a signal set and add one signal.

This constructor creates a signal set and registers for one signal.
```c
asio::signal_set::signal_set(asio::io_context &io_context, int signal_number_1)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- int `signal_number_1` The signal number to be added.



### signal_set()
Construct a signal set and add two signals.

This constructor creates a signal set and registers for two signals.
```c
asio::signal_set::signal_set(asio::io_context &io_context, int signal_number_1, int signal_number_2)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- int `signal_number_1` The first signal number to be added.
	- int `signal_number_2` The second signal number to be added.



### signal_set()
Construct a signal set and add three signals.

This constructor creates a signal set and registers for three signals.
```c
asio::signal_set::signal_set(asio::io_context &io_context, int signal_number_1, int signal_number_2, int signal_number_3)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- int `signal_number_1` The first signal number to be added.
	- int `signal_number_2` The second signal number to be added.
	- int `signal_number_3` The third signal number to be added.



### ~signal_set()
Destroys the signal set.

This function destroys the signal set, cancelling any outstanding asynchronous wait operations associated with the signal set as if by calling . 
```c
asio::signal_set::~signal_set()
```



### get_io_context()




```c
asio::io_context& asio::signal_set::get_io_context()
```

!!! note "戻り値"
	asio::io_context&



### get_io_service()




```c
asio::io_context& asio::signal_set::get_io_service()
```

!!! note "戻り値"
	asio::io_context&



### get_executor()
Get the executor associated with the object.


```c
executor_type asio::signal_set::get_executor() ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



### add()
Add a signal to a .

This function adds the specified signal to the set. It has no effect if the signal is already in the set.
```c
void asio::signal_set::add(int signal_number)
```

!!! summary "引数"
	- int `signal_number` The signal to be added to the set.



### add()
Add a signal to a .

This function adds the specified signal to the set. It has no effect if the signal is already in the set.
```c
ASIO_SYNC_OP_VOID asio::signal_set::add(int signal_number, asio::error_code &ec)
```

!!! summary "引数"
	- int `signal_number` The signal to be added to the set.
	- asio::error_code& `ec` Set to indicate what error occurred, if any. 

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### remove()
Remove a signal from a .

This function removes the specified signal from the set. It has no effect if the signal is not in the set.
```c
void asio::signal_set::remove(int signal_number)
```

!!! summary "引数"
	- int `signal_number` The signal to be removed from the set.



### remove()
Remove a signal from a .

This function removes the specified signal from the set. It has no effect if the signal is not in the set.
```c
ASIO_SYNC_OP_VOID asio::signal_set::remove(int signal_number, asio::error_code &ec)
```

!!! summary "引数"
	- int `signal_number` The signal to be removed from the set.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### clear()
Remove all signals from a .

This function removes all signals from the set. It has no effect if the set is already empty.
```c
void asio::signal_set::clear()
```



### clear()
Remove all signals from a .

This function removes all signals from the set. It has no effect if the set is already empty.
```c
ASIO_SYNC_OP_VOID asio::signal_set::clear(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### cancel()
Cancel all operations associated with the signal set.

Cancellation does not alter the set of registered signals.
```c
void asio::signal_set::cancel()
```



### cancel()
Cancel all operations associated with the signal set.

Cancellation does not alter the set of registered signals.
```c
ASIO_SYNC_OP_VOID asio::signal_set::cancel(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	ASIO_SYNC_OP_VOID



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous operation to wait for a signal to be delivered.

For each call to async_wait(), the supplied handler will be called exactly once. The handler will be called when:
```c
asio::signal_set::ASIO_INITFN_RESULT_TYPE(SignalHandler, void(asio::error_code, int)) async_wait(ASIO_MOVE_ARG(SignalHandler) handler)
```

!!! summary "引数"
	- asio::error_codevoid(, int) `` 



