# asio::ip::udp

Encapsulates the flags needed for . 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1udp.html)

## メンバー







### v4()
Construct to represent the IPv4  protocol.


```c
static udp asio::ip::udp::v4()
```

!!! note "戻り値"
	udp



### v6()
Construct to represent the IPv6  protocol.


```c
static udp asio::ip::udp::v6()
```

!!! note "戻り値"
	udp



### type()
Obtain an identifier for the type of the protocol.


```c
int asio::ip::udp::type() const
```

!!! note "戻り値"
	int



### protocol()
Obtain an identifier for the protocol.


```c
int asio::ip::udp::protocol() const
```

!!! note "戻り値"
	int



### family()
Obtain an identifier for the protocol family.


```c
int asio::ip::udp::family() const
```

!!! note "戻り値"
	int







