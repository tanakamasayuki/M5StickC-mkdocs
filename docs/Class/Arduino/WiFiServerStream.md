# WiFiServerStream



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_wi_fi_server_stream.html)

## メンバー

### WiFiServerStream()


create a WiFi stream with a TCP server 
```c
WiFiServerStream::WiFiServerStream(uint16_t server_port)
```

!!! summary "引数"
	- uint16_t `server_port` 



### maintain()


maintain WiFi and TCP connection 

```c
virtual bool WiFiServerStream::maintain()
```

!!! note "戻り値"
	bool true if WiFi and TCP connection are established 



### stop()


stop client connection 
```c
virtual void WiFiServerStream::stop()
```



