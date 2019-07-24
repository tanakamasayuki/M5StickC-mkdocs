# WiFiClientRxBuffer



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_wi_fi_client_rx_buffer.html)

## メンバー

### WiFiClientRxBuffer()



```c
WiFiClientRxBuffer::WiFiClientRxBuffer(int fd, size_t size=1436)
```

!!! summary "引数"
	- int `fd` 
	- size_t `size` 



### ~WiFiClientRxBuffer()



```c
WiFiClientRxBuffer::~WiFiClientRxBuffer()
```



### failed()



```c
bool WiFiClientRxBuffer::failed()
```

!!! note "戻り値"
	bool



### read()



```c
int WiFiClientRxBuffer::read(uint8_t *dst, size_t len)
```

!!! summary "引数"
	- uint8_t* `dst` 
	- size_t `len` 

!!! note "戻り値"
	int



### peek()



```c
int WiFiClientRxBuffer::peek()
```

!!! note "戻り値"
	int



### available()



```c
size_t WiFiClientRxBuffer::available()
```

!!! note "戻り値"
	size_t



