# asio::ip::detail::socket_option::unicast_hops



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1detail_1_1socket__option_1_1unicast__hops.html)

## メンバー

### unicast_hops()



```c
asio::ip::detail::socket_option::unicast_hops< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::unicast_hops()
```



### unicast_hops()



```c
asio::ip::detail::socket_option::unicast_hops< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::unicast_hops(int v)
```

!!! summary "引数"
	- int `v` 



### operator=()



```c
unicast_hops& asio::ip::detail::socket_option::unicast_hops< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::operator=(int v)
```

!!! summary "引数"
	- int `v` 

!!! note "戻り値"
	unicast_hops&



### value()



```c
int asio::ip::detail::socket_option::unicast_hops< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::value() const
```

!!! note "戻り値"
	int



### level()



```c
int asio::ip::detail::socket_option::unicast_hops< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::level(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	int



### name()



```c
int asio::ip::detail::socket_option::unicast_hops< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::name(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	int



### data()



```c
int* asio::ip::detail::socket_option::unicast_hops< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::data(const Protocol &)
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	int *



### data()



```c
const int* asio::ip::detail::socket_option::unicast_hops< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::data(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	constint *



### size()



```c
std::size_t asio::ip::detail::socket_option::unicast_hops< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::size(const Protocol &) const
```

!!! summary "引数"
	- constProtocol & `` 

!!! note "戻り値"
	std::size_t



### resize()



```c
void asio::ip::detail::socket_option::unicast_hops< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::resize(const Protocol &, std::size_t s)
```

!!! summary "引数"
	- constProtocol & `` 
	- std::size_t `s` 



