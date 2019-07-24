# DNSServer



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_d_n_s_server.html)

## メンバー

### DNSServer()



```c
DNSServer::DNSServer()
```



### processNextRequest()



```c
void DNSServer::processNextRequest()
```



### setErrorReplyCode()



```c
void DNSServer::setErrorReplyCode(const DNSReplyCode &replyCode)
```

!!! summary "引数"
	- const& `replyCode` 



### setTTL()



```c
void DNSServer::setTTL(const uint32_t &ttl)
```

!!! summary "引数"
	- const& `ttl` 



### start()



```c
bool DNSServer::start(const uint16_t &port, const String &domainName, const IPAddress &resolvedIP)
```

!!! summary "引数"
	- const& `port` 
	- constString & `domainName` 
	- const& `resolvedIP` 

!!! note "戻り値"
	bool



### stop()



```c
void DNSServer::stop()
```



