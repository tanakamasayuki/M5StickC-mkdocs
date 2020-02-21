# asio::ip::tcp

Encapsulates the flags needed for TCP. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1ip_1_1tcp.html)

## メンバー













### v4()
Construct to represent the IPv4 TCP protocol.


```c
static tcp asio::ip::tcp::v4()
```

!!! note "戻り値"
	tcp



### v6()
Construct to represent the IPv6 TCP protocol.


```c
static tcp asio::ip::tcp::v6()
```

!!! note "戻り値"
	tcp



### type()
Obtain an identifier for the type of the protocol.


```c
int asio::ip::tcp::type() const
```

!!! note "戻り値"
	int



### protocol()
Obtain an identifier for the protocol.


```c
int asio::ip::tcp::protocol() const
```

!!! note "戻り値"
	int



### family()
Obtain an identifier for the protocol family.


```c
int asio::ip::tcp::family() const
```

!!! note "戻り値"
	int







