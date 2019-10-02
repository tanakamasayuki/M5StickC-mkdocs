# asio::ip::detail::socket_option::network_interface



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1detail_1_1socket__option_1_1network__interface.html)

## メンバー

### network_interface()



```c
asio::ip::detail::socket_option::network_interface< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::network_interface()
```



### network_interface()



```c
asio::ip::detail::socket_option::network_interface< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::network_interface(const address_v4 &ipv4_interface)
```

!!! summary "引数"
	- const& `ipv4_interface` 



### network_interface()



```c
asio::ip::detail::socket_option::network_interface< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::network_interface(unsigned int ipv6_interface)
```

!!! summary "引数"
	- unsigned int `ipv6_interface` 



### level()



```c
int asio::ip::detail::socket_option::network_interface< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::level(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	int



### name()



```c
int asio::ip::detail::socket_option::network_interface< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::name(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	int



### data()



```c
const void* asio::ip::detail::socket_option::network_interface< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::data(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	constvoid *



### size()



```c
std::size_t asio::ip::detail::socket_option::network_interface< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::size(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	std::size_t



