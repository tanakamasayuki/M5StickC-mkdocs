# WiFiStream



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_wi_fi_stream.html)

## メンバー

### WiFiStream()


constructor for TCP server 
```c
WiFiStream::WiFiStream(uint16_t server_port)
```

!!! summary "引数"
	- uint16_t `server_port` 



### WiFiStream()


constructor for TCP client 
```c
WiFiStream::WiFiStream(IPAddress server_ip, uint16_t server_port)
```

!!! summary "引数"
	- IPAddress `server_ip` 
	- uint16_t `server_port` 



### attach()



```c
void WiFiStream::attach(hostConnectionCallbackFunction newFunction)
```

!!! summary "引数"
	- hostConnectionCallbackFunction `newFunction` 



### config()


configure a static local IP address without defining the local network DHCP will be used as long as local IP address is not defined 
```c
void WiFiStream::config(IPAddress local_ip)
```

!!! summary "引数"
	- IPAddress `local_ip` 



### config()


configure a static local IP address DHCP will be used as long as local IP address is not defined 
```c
void WiFiStream::config(IPAddress local_ip, IPAddress gateway, IPAddress subnet)
```

!!! summary "引数"
	- IPAddress `local_ip` 
	- IPAddress `gateway` 
	- IPAddress `subnet` 



### getLocalIP()




```c
IPAddress WiFiStream::getLocalIP()
```

!!! note "戻り値"
	IPAddress local IP address 



### maintain()


maintain WiFi and TCP connection 

```c
virtual bool WiFiStream::maintain()=0
```

!!! note "戻り値"
	bool true if WiFi and TCP connection are established 



### stop()


close TCP client connection 
```c
virtual void WiFiStream::stop()=0
```



### begin()


initialize WiFi without security (open) and initiate client connection if WiFi connection is already established 

```c
int WiFiStream::begin(char *ssid)
```

!!! summary "引数"
	- char * `ssid` 

!!! note "戻り値"
	int WL_CONNECTED if WiFi connection is established 



### begin()


initialize WiFi with WEP security and initiate client connection if WiFi connection is already established 

```c
int WiFiStream::begin(char *ssid, uint8_t key_idx, const char *key)
```

!!! summary "引数"
	- char * `ssid` 
	- uint8_t `key_idx` 
	- constchar * `key` 

!!! note "戻り値"
	int WL_CONNECTED if WiFi connection is established 



### begin()


initialize WiFi with WPA-PSK security and initiate client connection if WiFi connection is already established 

```c
int WiFiStream::begin(char *ssid, const char *passphrase)
```

!!! summary "引数"
	- char * `ssid` 
	- constchar * `passphrase` 

!!! note "戻り値"
	int WL_CONNECTED if WiFi connection is established 



### available()



```c
int WiFiStream::available()
```

!!! note "戻り値"
	int



### flush()



```c
void WiFiStream::flush()
```



### peek()



```c
int WiFiStream::peek()
```

!!! note "戻り値"
	int



### read()



```c
int WiFiStream::read()
```

!!! note "戻り値"
	int



### write()



```c
size_t WiFiStream::write(uint8_t byte)
```

!!! summary "引数"
	- uint8_t `byte` 

!!! note "戻り値"
	size_t



