# asio::detail::socket_option::boolean



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1socket__option_1_1boolean.html)

## メンバー

### boolean()



```c
asio::detail::socket_option::boolean< Level, Name >::boolean()
```



### boolean()



```c
asio::detail::socket_option::boolean< Level, Name >::boolean(bool v)
```

!!! summary "引数"
	- bool `v` 



### operator=()



```c
boolean& asio::detail::socket_option::boolean< Level, Name >::operator=(bool v)
```

!!! summary "引数"
	- bool `v` 

!!! note "戻り値"
	boolean&



### value()



```c
bool asio::detail::socket_option::boolean< Level, Name >::value() const
```

!!! note "戻り値"
	bool



### operator bool()



```c
asio::detail::socket_option::boolean< Level, Name >::operator bool() const
```



### operator!()



```c
bool asio::detail::socket_option::boolean< Level, Name >::operator!() const
```

!!! note "戻り値"
	bool



### level()



```c
int asio::detail::socket_option::boolean< Level, Name >::level(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	int



### name()



```c
int asio::detail::socket_option::boolean< Level, Name >::name(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	int



### data()



```c
int* asio::detail::socket_option::boolean< Level, Name >::data(const Protocol &)
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	int *



### data()



```c
const int* asio::detail::socket_option::boolean< Level, Name >::data(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	constint *



### size()



```c
std::size_t asio::detail::socket_option::boolean< Level, Name >::size(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	std::size_t



### resize()



```c
void asio::detail::socket_option::boolean< Level, Name >::resize(const Protocol &, std::size_t s)
```

!!! summary "引数"
	- constProtocol & `` 
	- std::size_t `s` 



