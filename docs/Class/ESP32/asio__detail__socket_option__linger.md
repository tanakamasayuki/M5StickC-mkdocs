# asio::detail::socket_option::linger



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1socket__option_1_1linger.html)

## メンバー

### linger()



```c
asio::detail::socket_option::linger< Level, Name >::linger()
```



### linger()



```c
asio::detail::socket_option::linger< Level, Name >::linger(bool e, int t)
```

!!! summary "引数"
	- bool `e` 
	- int `t` 



### enabled()



```c
void asio::detail::socket_option::linger< Level, Name >::enabled(bool value)
```

!!! summary "引数"
	- bool `value` 



### enabled()



```c
bool asio::detail::socket_option::linger< Level, Name >::enabled() const
```

!!! note "戻り値"
	bool



### ASIO_PREVENT_MACRO_SUBSTITUTION()



```c
void timeout asio::detail::socket_option::linger< Level, Name >::ASIO_PREVENT_MACRO_SUBSTITUTION(int value)
```

!!! summary "引数"
	- int `value` 

!!! note "戻り値"
	void timeout



### ASIO_PREVENT_MACRO_SUBSTITUTION()



```c
int timeout asio::detail::socket_option::linger< Level, Name >::ASIO_PREVENT_MACRO_SUBSTITUTION() const
```

!!! note "戻り値"
	int timeout



### level()



```c
int asio::detail::socket_option::linger< Level, Name >::level(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	int



### name()



```c
int asio::detail::socket_option::linger< Level, Name >::name(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	int



### data()



```c
detail::linger_type* asio::detail::socket_option::linger< Level, Name >::data(const Protocol &)
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	detail::linger_type*



### data()



```c
const detail::linger_type* asio::detail::socket_option::linger< Level, Name >::data(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	const*



### size()



```c
std::size_t asio::detail::socket_option::linger< Level, Name >::size(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	std::size_t



### resize()



```c
void asio::detail::socket_option::linger< Level, Name >::resize(const Protocol &, std::size_t s)
```

!!! summary "引数"
	- constProtocol & `` 
	- std::size_t `s` 



