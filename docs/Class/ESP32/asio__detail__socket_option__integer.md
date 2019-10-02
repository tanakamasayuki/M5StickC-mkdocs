# asio::detail::socket_option::integer



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1socket__option_1_1integer.html)

## メンバー

### integer()



```c
asio::detail::socket_option::integer< Level, Name >::integer()
```



### integer()



```c
asio::detail::socket_option::integer< Level, Name >::integer(int v)
```

!!! summary "引数"
	- int `v` 



### operator=()



```c
integer& asio::detail::socket_option::integer< Level, Name >::operator=(int v)
```

!!! summary "引数"
	- int `v` 

!!! note "戻り値"
	integer&



### value()



```c
int asio::detail::socket_option::integer< Level, Name >::value() const
```

!!! note "戻り値"
	int



### level()



```c
int asio::detail::socket_option::integer< Level, Name >::level(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	int



### name()



```c
int asio::detail::socket_option::integer< Level, Name >::name(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	int



### data()



```c
int* asio::detail::socket_option::integer< Level, Name >::data(const Protocol &)
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	int *



### data()



```c
const int* asio::detail::socket_option::integer< Level, Name >::data(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	constint *



### size()



```c
std::size_t asio::detail::socket_option::integer< Level, Name >::size(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	std::size_t



### resize()



```c
void asio::detail::socket_option::integer< Level, Name >::resize(const Protocol &, std::size_t s)
```

!!! summary "引数"
	- constProtocol & `` 
	- std::size_t `s` 



