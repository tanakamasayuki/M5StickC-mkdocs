# EthernetServerStream



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_ethernet_server_stream.html)

## メンバー

### EthernetServerStream()



```c
EthernetServerStream::EthernetServerStream(IPAddress localip, uint16_t port)
```

!!! summary "引数"
	- IPAddress `localip` 
	- uint16_t `port` 



### available()



```c
int EthernetServerStream::available()
```

!!! note "戻り値"
	int



### read()



```c
int EthernetServerStream::read()
```

!!! note "戻り値"
	int



### peek()



```c
int EthernetServerStream::peek()
```

!!! note "戻り値"
	int



### flush()



```c
void EthernetServerStream::flush()
```



### write()



```c
size_t EthernetServerStream::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### maintain()



```c
void EthernetServerStream::maintain(IPAddress localip)
```

!!! summary "引数"
	- IPAddress `localip` 



