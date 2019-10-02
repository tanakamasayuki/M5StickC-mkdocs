# MQTT::Client

blocking, non-threaded  client API 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_m_q_t_t_1_1_client.html)

## メンバー



### Client()



```c
Client::Client(Network &network, unsigned int command_timeout_ms=30000)
```

!!! summary "引数"
	- Network & `network` - pointer to an instance of the Network class - must be connected to the endpoint before calling  connect 
	- unsigned int `command_timeout_ms` 



### setDefaultMessageHandler()



```c
void MQTT::Client< Network, Timer, MAX_MQTT_PACKET_SIZE, MAX_MESSAGE_HANDLERS >::setDefaultMessageHandler(messageHandler mh)
```

!!! summary "引数"
	- messageHandler `mh` - pointer to the callback function 



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

!!! summary "引数"
	- MQTTPacket_connectData& `options` - connect options 

!!! note "戻り値"
	int success code - 



### publish()



```c
int Client::publish(const char *topicName, Message &message)
```

!!! summary "引数"
	- constchar * `topicName` 
	- Message& `message` - the message to send 

!!! note "戻り値"
	int success code - 



### publish()



```c
int Client::publish(const char *topicName, void *payload, size_t payloadlen, enum QoS qos=QOS0, bool retained=false)
```

!!! summary "引数"
	- constchar * `topicName` 
	- void * `payload` - the data to send 
	- size_t `payloadlen` - the length of the data 
	- QoSenum `qos` - the QoS to send the publish at 
	- bool `retained` - whether the message should be retained 

!!! note "戻り値"
	int success code - 



### publish()



```c
int Client::publish(const char *topicName, void *payload, size_t payloadlen, unsigned short &id, enum QoS qos=QOS1, bool retained=false)
```

!!! summary "引数"
	- constchar * `topicName` 
	- void * `payload` - the data to send 
	- size_t `payloadlen` - the length of the data 
	- unsigned short & `id` - the packet id used - returned 
	- QoSenum `qos` - the QoS to send the publish at 
	- bool `retained` - whether the message should be retained 

!!! note "戻り値"
	int success code - 



### subscribe()



```c
int Client::subscribe(const char *topicFilter, enum QoS qos, messageHandler mh)
```

!!! summary "引数"
	- constchar * `topicFilter` - a topic pattern which can include wildcards 
	- QoSenum `qos` - the  QoS to subscribe at 
	- messageHandler `mh` - the callback function to be invoked when a message is received for this subscription 

!!! note "戻り値"
	int success code - 



### unsubscribe()



```c
int Client::unsubscribe(const char *topicFilter)
```

!!! summary "引数"
	- constchar * `topicFilter` - a topic pattern which can include wildcards 

!!! note "戻り値"
	int success code - 



### disconnect()


 Disconnect - send an  disconnect packet, and clean up any state 

```c
int Client::disconnect()
```

!!! note "戻り値"
	int success code - 



### yield()



```c
int Client::yield(unsigned long timeout_ms=1000L)
```

!!! summary "引数"
	- unsigned long `timeout_ms` the time to wait, in milliseconds 

!!! note "戻り値"
	int success code - on failure, this means the client has disconnected 



### isConnected()


Is the client connected? 

```c
bool MQTT::Client< Network, Timer, MAX_MQTT_PACKET_SIZE, MAX_MESSAGE_HANDLERS >::isConnected()
```

!!! note "戻り値"
	bool flag - is the client connected or not? 



