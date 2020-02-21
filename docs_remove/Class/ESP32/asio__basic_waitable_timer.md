# asio::basic_waitable_timer

Provides waitable timer functionality. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1basic__waitable__timer.html)

## メンバー











### basic_waitable_timer()
Constructor.

This constructor creates a timer without setting an expiry time. The  or  functions must be called to set an expiry time before the timer can be waited on.
```c
asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::basic_waitable_timer(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### basic_waitable_timer()
Constructor to set a particular expiry time as an absolute time.

This constructor creates a timer and sets the expiry time.
```c
asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::basic_waitable_timer(asio::io_context &io_context, const time_point &expiry_time)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `expiry_time` The expiry time to be used for the timer, expressed as an absolute time. 



### basic_waitable_timer()
Constructor to set a particular expiry time relative to now.

This constructor creates a timer and sets the expiry time.
```c
asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::basic_waitable_timer(asio::io_context &io_context, const duration &expiry_time)
```

!!! summary "引数"
	- asio::io_context& `io_context` 
	- const& `expiry_time` The expiry time to be used for the timer, relative to now. 



### ~basic_waitable_timer()
Destroys the timer.

This function destroys the timer, cancelling any outstanding asynchronous wait operations associated with the timer as if by calling . 
```c
asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::~basic_waitable_timer()
```



### get_io_context()




```c
asio::io_context& asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::get_io_context()
```

!!! note "戻り値"
	asio::io_context&



### get_io_service()




```c
asio::io_context& asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::get_io_service()
```

!!! note "戻り値"
	asio::io_context&



### get_executor()
Get the executor associated with the object.


```c
executor_type asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::get_executor() ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



### cancel()
Cancel any asynchronous operations that are waiting on the timer.

Cancelling the timer does not change the expiry time.
```c
std::size_t asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::cancel()
```

!!! note "戻り値"
	std::size_t



### cancel()


Cancelling the timer does not change the expiry time.
```c
std::size_t asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::cancel(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### cancel_one()
Cancels one asynchronous operation that is waiting on the timer.

Cancelling the timer does not change the expiry time.
```c
std::size_t asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::cancel_one()
```

!!! note "戻り値"
	std::size_t



### cancel_one()


Cancelling the timer does not change the expiry time.
```c
std::size_t asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::cancel_one(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### expires_at()


(Deprecated: Use .) Get the timer's expiry time as an absolute time. This function may be used to obtain the timer's current expiry time. Whether the timer has expired or not does not affect this value. 
```c
time_point asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::expires_at() const
```

!!! note "戻り値"
	time_point



### expiry()
Get the timer's expiry time as an absolute time.

This function may be used to obtain the timer's current expiry time. Whether the timer has expired or not does not affect this value. 
```c
time_point asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::expiry() const
```

!!! note "戻り値"
	time_point



### expires_at()
Set the timer's expiry time as an absolute time.

This function sets the expiry time. Any pending asynchronous wait operations will be cancelled. The handler for each cancelled operation will be invoked with the  error code.
```c
std::size_t asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::expires_at(const time_point &expiry_time)
```

!!! summary "引数"
	- const& `expiry_time` The expiry time to be used for the timer.

!!! note "戻り値"
	std::size_t



### expires_at()


(Deprecated: Use non-error_code overload.) Set the timer's expiry time as an absolute time. This function sets the expiry time. Any pending asynchronous wait operations will be cancelled. The handler for each cancelled operation will be invoked with the  error code.
```c
std::size_t asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::expires_at(const time_point &expiry_time, asio::error_code &ec)
```

!!! summary "引数"
	- const& `expiry_time` The expiry time to be used for the timer.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### expires_after()
Set the timer's expiry time relative to now.

This function sets the expiry time. Any pending asynchronous wait operations will be cancelled. The handler for each cancelled operation will be invoked with the  error code.
```c
std::size_t asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::expires_after(const duration &expiry_time)
```

!!! summary "引数"
	- const& `expiry_time` The expiry time to be used for the timer.

!!! note "戻り値"
	std::size_t



### expires_from_now()
(Deprecated: Use .) Get the timer's expiry time relative to now.

This function may be used to obtain the timer's current expiry time. Whether the timer has expired or not does not affect this value. 
```c
duration asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::expires_from_now() const
```

!!! note "戻り値"
	duration



### expires_from_now()


(Deprecated: Use .) Set the timer's expiry time relative to now. This function sets the expiry time. Any pending asynchronous wait operations will be cancelled. The handler for each cancelled operation will be invoked with the  error code.
```c
std::size_t asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::expires_from_now(const duration &expiry_time)
```

!!! summary "引数"
	- const& `expiry_time` The expiry time to be used for the timer.

!!! note "戻り値"
	std::size_t



### expires_from_now()


(Deprecated: Use .) Set the timer's expiry time relative to now. This function sets the expiry time. Any pending asynchronous wait operations will be cancelled. The handler for each cancelled operation will be invoked with the  error code.
```c
std::size_t asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::expires_from_now(const duration &expiry_time, asio::error_code &ec)
```

!!! summary "引数"
	- const& `expiry_time` The expiry time to be used for the timer.
	- asio::error_code& `ec` Set to indicate what error occurred, if any.

!!! note "戻り値"
	std::size_t



### wait()
Perform a blocking wait on the timer.

This function is used to wait for the timer to expire. This function blocks and does not return until the timer has expired.
```c
void asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::wait()
```



### wait()
Perform a blocking wait on the timer.

This function is used to wait for the timer to expire. This function blocks and does not return until the timer has expired.
```c
void asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::wait(asio::error_code &ec)
```

!!! summary "引数"
	- asio::error_code& `ec` Set to indicate what error occurred, if any. 



### ASIO_INITFN_RESULT_TYPE()
Start an asynchronous wait on the timer.

For each call to async_wait(), the supplied handler will be called exactly once. The handler will be called when:
```c
asio::basic_waitable_timer< Clock, ASIO_SVC_TPARAM >::ASIO_INITFN_RESULT_TYPE(WaitHandler, void(asio::error_code)) async_wait(ASIO_MOVE_ARG(WaitHandler) handler)
```

!!! summary "引数"
	- asio::error_codevoid() `` 



