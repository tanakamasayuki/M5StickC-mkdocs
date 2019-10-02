# asio::ip::detail::socket_option::multicast_request



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1detail_1_1socket__option_1_1multicast__request.html)

## メンバー

### multicast_request()



```c
asio::ip::detail::socket_option::multicast_request< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::multicast_request()
```



### multicast_request()



```c
asio::ip::detail::socket_option::multicast_request< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::multicast_request(const address &multicast_address)
```

!!! summary "引数"
	- const& `multicast_address` 



### multicast_request()



```c
asio::ip::detail::socket_option::multicast_request< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::multicast_request(const address_v4 &multicast_address, const address_v4 &network_interface=address_v4::any())
```

!!! summary "引数"
	- const& `multicast_address` 
	- const& `network_interface` 



### multicast_request()



```c
asio::ip::detail::socket_option::multicast_request< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::multicast_request(const address_v6 &multicast_address, unsigned long network_interface=0)
```

!!! summary "引数"
	- const& `multicast_address` 
	- unsigned long `network_interface` 



### level()



```c
int asio::ip::detail::socket_option::multicast_request< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::level(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	int



### name()



```c
int asio::ip::detail::socket_option::multicast_request< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::name(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	int



### data()



```c
const void* asio::ip::detail::socket_option::multicast_request< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::data(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	constvoid *



### size()



```c
std::size_t asio::ip::detail::socket_option::multicast_request< IPv4_Level, IPv4_Name, IPv6_Level, IPv6_Name >::size(const Protocol &protocol) const
```

!!! summary "引数"
	- constProtocol & `protocol` 

!!! note "戻り値"
	std::size_t



