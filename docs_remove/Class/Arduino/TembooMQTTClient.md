# TembooMQTTClient



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_temboo_m_q_t_t_client.html)

## メンバー

### TembooMQTTClient()



```c
TembooMQTTClient::TembooMQTTClient(TembooMQTTIPStack &ipStack, unsigned int commandTimeoutMs=30000)
```

!!! summary "引数"
	- TembooMQTTIPStack& `ipStack` 
	- unsigned int `commandTimeoutMs` 



### ~TembooMQTTClient()



```c
TembooMQTTClient::~TembooMQTTClient()
```



### connect()



```c
int TembooMQTTClient::connect(const char *hostname, int port=1883)
```

!!! summary "引数"
	- constchar * `hostname` 
	- int `port` 

!!! note "戻り値"
	int



### isConnected()



```c
bool TembooMQTTClient::isConnected()
```

!!! note "戻り値"
	bool



### sendChoreoRequest()



```c
int TembooMQTTClient::sendChoreoRequest(const char *request, size_t len)
```

!!! summary "引数"
	- constchar * `request` 
	- size_t `len` 

!!! note "戻り値"
	int



### setDeviceId()



```c
int TembooMQTTClient::setDeviceId(char *id)
```

!!! summary "引数"
	- char * `id` 

!!! note "戻り値"
	int



### setDeviceIdFromMac()



```c
int TembooMQTTClient::setDeviceIdFromMac(byte(&mac)[6])
```

!!! summary "引数"
	- byte(&) `mac` 

!!! note "戻り値"
	int



### connect()


 Connect - send an  connect packet down the network and wait for a Connack The nework object must be connected to the network endpoint before calling this Default connect options are used 

```c
int Client::connect()
```

!!! note "戻り値"
	int success code - 



### connect()



```c
int Client::connect(MQTTPacket_connectData &options)
```

!!! note "戻り値"
	int success code - 



### isConnected()


Is the client connected? 

```c
bool MQTT::Client< Network, Timer, MAX_MQTT_PACKET_SIZE, MAX_MESSAGE_HANDLERS >::isConnected()
```

!!! note "戻り値"
	bool flag - is the client connected or not? 



