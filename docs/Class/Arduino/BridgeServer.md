# BridgeServer



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_bridge_server.html)

## メンバー

### BridgeServer()



```c
BridgeServer::BridgeServer(uint16_t port=5555, BridgeClass &_b=Bridge)
```

!!! summary "引数"
	- uint16_t `port` 
	- BridgeClass& `_b` 



### begin()



```c
void BridgeServer::begin()
```



### accept()



```c
BridgeClient BridgeServer::accept()
```

!!! note "戻り値"
	BridgeClient



### write()



```c
size_t BridgeServer::write(uint8_t c)
```

!!! summary "引数"
	- uint8_t `c` 

!!! note "戻り値"
	size_t



### listenOnLocalhost()



```c
void BridgeServer::listenOnLocalhost()
```



### noListenOnLocalhost()



```c
void BridgeServer::noListenOnLocalhost()
```



