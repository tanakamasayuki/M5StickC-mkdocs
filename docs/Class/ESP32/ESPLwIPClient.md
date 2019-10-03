# ESPLwIPClient



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/class_e_s_p_lw_i_p_client.html)

## メンバー

### connect()



```c
virtual int ESPLwIPClient::connect(IPAddress ip, uint16_t port, int32_t timeout)=0
```

!!! summary "引数"
	- IPAddress `ip` 
	- uint16_t `port` 
	- int32_t `timeout` 

!!! note "戻り値"
	int



### connect()



```c
virtual int ESPLwIPClient::connect(const char *host, uint16_t port, int32_t timeout)=0
```

!!! summary "引数"
	- constchar * `host` 
	- uint16_t `port` 
	- int32_t `timeout` 

!!! note "戻り値"
	int



### setTimeout()



```c
virtual int ESPLwIPClient::setTimeout(uint32_t seconds)=0
```

!!! summary "引数"
	- uint32_t `seconds` 

!!! note "戻り値"
	int



