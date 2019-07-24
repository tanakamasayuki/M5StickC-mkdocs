# WiFiClientStream



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_wi_fi_client_stream.html)

## メンバー

### WiFiClientStream()


create a WiFi stream with a TCP client 
```c
WiFiClientStream::WiFiClientStream(IPAddress server_ip, uint16_t server_port)
```

!!! summary "引数"
	- IPAddress `server_ip` 
	- uint16_t `server_port` 



### maintain()


maintain WiFi and TCP connection 

```c
virtual bool WiFiClientStream::maintain()
```

!!! note "戻り値"
	bool true if WiFi and TCP connection are established 



### stop()


stop client connection 
```c
virtual void WiFiClientStream::stop()
```



