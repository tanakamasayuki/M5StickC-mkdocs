# TembooMQTTIPStack



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_temboo_m_q_t_t_i_p_stack.html)

## メンバー

### TembooMQTTIPStack()



```c
TembooMQTTIPStack::TembooMQTTIPStack(Client &client)
```

!!! summary "引数"
	- Client& `client` 



### connect()



```c
int TembooMQTTIPStack::connect(const char *hostname, int port)
```

!!! summary "引数"
	- constchar * `hostname` 
	- int `port` 

!!! note "戻り値"
	int



### isConnected()



```c
bool TembooMQTTIPStack::isConnected()
```

!!! note "戻り値"
	bool



### disconnect()



```c
int TembooMQTTIPStack::disconnect()
```

!!! note "戻り値"
	int



### read()



```c
int TembooMQTTIPStack::read(unsigned char *buffer, int len, int timeoutMillis)
```

!!! summary "引数"
	- unsigned char * `buffer` 
	- int `len` 
	- int `timeoutMillis` 

!!! note "戻り値"
	int



### write()



```c
int TembooMQTTIPStack::write(unsigned char *buffer, int len, int timeout)
```

!!! summary "引数"
	- unsigned char * `buffer` 
	- int `len` 
	- int `timeout` 

!!! note "戻り値"
	int



