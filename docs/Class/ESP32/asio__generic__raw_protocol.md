# asio::generic::raw_protocol

Encapsulates the flags needed for a generic raw socket. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1generic_1_1raw__protocol.html)

## メンバー





### raw_protocol()
Construct a protocol object for a specific address family and protocol.


```c
asio::generic::raw_protocol::raw_protocol(int address_family, int socket_protocol)
```

!!! summary "引数"
	- int `address_family` 
	- int `socket_protocol` 



### raw_protocol()
Construct a generic protocol object from a specific protocol.


```c
asio::generic::raw_protocol::raw_protocol(const Protocol &source_protocol)
```

!!! summary "引数"
	- constProtocol & `source_protocol` 



### type()
Obtain an identifier for the type of the protocol.


```c
int asio::generic::raw_protocol::type() const
```

!!! note "戻り値"
	int



### protocol()
Obtain an identifier for the protocol.


```c
int asio::generic::raw_protocol::protocol() const
```

!!! note "戻り値"
	int



### family()
Obtain an identifier for the protocol family.


```c
int asio::generic::raw_protocol::family() const
```

!!! note "戻り値"
	int







