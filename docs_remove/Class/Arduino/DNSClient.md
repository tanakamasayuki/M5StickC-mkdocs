# DNSClient



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_d_n_s_client.html)

## メンバー

### begin()



```c
void DNSClient::begin(const IPAddress &aDNSServer)
```

!!! summary "引数"
	- const& `aDNSServer` 



### inet_aton()



```c
int DNSClient::inet_aton(const char *aIPAddrString, IPAddress &aResult)
```

!!! summary "引数"
	- constchar * `aIPAddrString` IP address to convert 
	- IPAddress& `aResult`  structure to store the returned IP address 

!!! note "戻り値"
	int 1 if aIPAddrString was successfully converted to an IP address, else error code 



### getHostByName()



```c
int DNSClient::getHostByName(const char *aHostname, IPAddress &aResult, uint16_t timeout=5000)
```

!!! summary "引数"
	- constchar * `aHostname` Name to be resolved 
	- IPAddress& `aResult`  structure to store the returned IP address 
	- uint16_t `timeout` 

!!! note "戻り値"
	int 1 if aIPAddrString was successfully converted to an IP address, else error code 



