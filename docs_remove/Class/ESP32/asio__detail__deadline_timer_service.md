# asio::detail::deadline_timer_service



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1deadline__timer__service.html)

## メンバー





### deadline_timer_service()



```c
asio::detail::deadline_timer_service< Time_Traits >::deadline_timer_service(asio::io_context &io_context)
```

!!! summary "引数"
	- asio::io_context& `io_context` 



### ~deadline_timer_service()



```c
asio::detail::deadline_timer_service< Time_Traits >::~deadline_timer_service()
```



### shutdown()
Destroy all user-defined handler objects owned by the service.


```c
void asio::detail::deadline_timer_service< Time_Traits >::shutdown()
```



### construct()



```c
void asio::detail::deadline_timer_service< Time_Traits >::construct(implementation_type &impl)
```

!!! summary "引数"
	- implementation_type& `impl` 



### destroy()



```c
void asio::detail::deadline_timer_service< Time_Traits >::destroy(implementation_type &impl)
```

!!! summary "引数"
	- implementation_type& `impl` 



### move_construct()



```c
void asio::detail::deadline_timer_service< Time_Traits >::move_construct(implementation_type &impl, implementation_type &other_impl)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- implementation_type& `other_impl` 



### move_assign()



```c
void asio::detail::deadline_timer_service< Time_Traits >::move_assign(implementation_type &impl, deadline_timer_service &other_service, implementation_type &other_impl)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- deadline_timer_service& `other_service` 
	- implementation_type& `other_impl` 



### cancel()



```c
std::size_t asio::detail::deadline_timer_service< Time_Traits >::cancel(implementation_type &impl, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	std::size_t



### cancel_one()



```c
std::size_t asio::detail::deadline_timer_service< Time_Traits >::cancel_one(implementation_type &impl, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	std::size_t



### expiry()



```c
time_type asio::detail::deadline_timer_service< Time_Traits >::expiry(const implementation_type &impl) const
```

!!! summary "引数"
	- const& `impl` 

!!! note "戻り値"
	time_type



### expires_at()



```c
time_type asio::detail::deadline_timer_service< Time_Traits >::expires_at(const implementation_type &impl) const
```

!!! summary "引数"
	- const& `impl` 

!!! note "戻り値"
	time_type



### expires_from_now()



```c
duration_type asio::detail::deadline_timer_service< Time_Traits >::expires_from_now(const implementation_type &impl) const
```

!!! summary "引数"
	- const& `impl` 

!!! note "戻り値"
	duration_type



### expires_at()



```c
std::size_t asio::detail::deadline_timer_service< Time_Traits >::expires_at(implementation_type &impl, const time_type &expiry_time, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `expiry_time` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	std::size_t



### expires_after()



```c
std::size_t asio::detail::deadline_timer_service< Time_Traits >::expires_after(implementation_type &impl, const duration_type &expiry_time, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `expiry_time` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	std::size_t



### expires_from_now()



```c
std::size_t asio::detail::deadline_timer_service< Time_Traits >::expires_from_now(implementation_type &impl, const duration_type &expiry_time, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- const& `expiry_time` 
	- asio::error_code& `ec` 

!!! note "戻り値"
	std::size_t



### wait()



```c
void asio::detail::deadline_timer_service< Time_Traits >::wait(implementation_type &impl, asio::error_code &ec)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- asio::error_code& `ec` 



### async_wait()



```c
void asio::detail::deadline_timer_service< Time_Traits >::async_wait(implementation_type &impl, Handler &handler)
```

!!! summary "引数"
	- implementation_type& `impl` 
	- Handler & `handler` 



