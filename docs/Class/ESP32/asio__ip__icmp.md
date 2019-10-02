# asio::ip::icmp

Encapsulates the flags needed for ICMP. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1icmp.html)

## メンバー







### v4()
Construct to represent the IPv4 ICMP protocol.


```c
static icmp asio::ip::icmp::v4()
```

!!! note "戻り値"
	icmp



### v6()
Construct to represent the IPv6 ICMP protocol.


```c
static icmp asio::ip::icmp::v6()
```

!!! note "戻り値"
	icmp



### type()
Obtain an identifier for the type of the protocol.


```c
int asio::ip::icmp::type() const
```

!!! note "戻り値"
	int



### protocol()
Obtain an identifier for the protocol.


```c
int asio::ip::icmp::protocol() const
```

!!! note "戻り値"
	int



### family()
Obtain an identifier for the protocol family.


```c
int asio::ip::icmp::family() const
```

!!! note "戻り値"
	int







