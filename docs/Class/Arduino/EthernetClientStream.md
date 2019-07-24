# EthernetClientStream



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_ethernet_client_stream.html)

## メンバー

### EthernetClientStream()



```c
EthernetClientStream::EthernetClientStream(Client &client, IPAddress localip, IPAddress ip, const char *host, uint16_t port)
```

!!! summary "引数"
	- Client& `client` 
	- IPAddress `localip` 
	- IPAddress `ip` 
	- constchar * `host` 
	- uint16_t `port` 



### available()



```c
int EthernetClientStream::available()
```

!!! note "戻り値"
	int



### read()



```c
int EthernetClientStream::read()
```

!!! note "戻り値"
	int



### peek()



```c
int EthernetClientStream::peek()
```

!!! note "戻り値"
	int



### flush()



```c
void EthernetClientStream::flush()
```



### write()



```c
size_t EthernetClientStream::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### maintain()



```c
void EthernetClientStream::maintain(IPAddress localip)
```

!!! summary "引数"
	- IPAddress `localip` 



