# asio::ip::detail::socket_option::multicast_enable_loopback



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1detail_1_1socket__option_1_1multicast__enable__loopback.html)

## メンバー





### multicast_enable_loopback()



```c
asio::ip::detail::socket_option::multicast_enable_loopback< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::multicast_enable_loopback()
```



### multicast_enable_loopback()



```c
asio::ip::detail::socket_option::multicast_enable_loopback< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::multicast_enable_loopback(bool v)
```

!!! summary "引数"
	- bool `v` 



### operator=()



```c
multicast_enable_loopback& asio::ip::detail::socket_option::multicast_enable_loopback< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::operator=(bool v)
```

!!! summary "引数"
	- bool `v` 

!!! note "戻り値"
	multicast_enable_loopback&



### value()



```c
bool asio::ip::detail::socket_option::multicast_enable_loopback< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::value() const
```

!!! note "戻り値"
	bool



### operator bool()



```c
asio::ip::detail::socket_option::multicast_enable_loopback< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::operator bool() const
```



### operator!()



```c
bool asio::ip::detail::socket_option::multicast_enable_loopback< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::operator!() const
```

!!! note "戻り値"
	bool



### level()



```c
int asio::ip::detail::socket_option::multicast_enable_loopback< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::level(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	int



### name()



```c
int asio::ip::detail::socket_option::multicast_enable_loopback< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::name(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	int



### data()



```c
void* asio::ip::detail::socket_option::multicast_enable_loopback< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::data(const Protocol &protocol)
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	void *



### data()



```c
const void* asio::ip::detail::socket_option::multicast_enable_loopback< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::data(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	constvoid *



### size()



```c
std::size_t asio::ip::detail::socket_option::multicast_enable_loopback< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::size(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	std::size_t



### resize()



```c
void asio::ip::detail::socket_option::multicast_enable_loopback< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::resize(const Protocol &protocol, std::size_t s)
```

!!! summary "引数"
	- constProtocol & `protocol` 
	- std::size_t `s` 



