# AsyncUDPMessage



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_async_u_d_p_message.html)

## メンバー

### AsyncUDPMessage()



```c
AsyncUDPMessage::AsyncUDPMessage(size_t size=CONFIG_TCP_MSS)
```

!!! summary "引数"
	- size_t `size` 



### ~AsyncUDPMessage()



```c
AsyncUDPMessage::~AsyncUDPMessage()
```



### write()



```c
size_t AsyncUDPMessage::write(const uint8_t *data, size_t len)
```

!!! summary "引数"
	- const* `data` 
	- size_t `len` 

!!! note "戻り値"
	size_t



### write()



```c
size_t AsyncUDPMessage::write(uint8_t data)
```

!!! summary "引数"
	- uint8_t `data` 

!!! note "戻り値"
	size_t



### space()



```c
size_t AsyncUDPMessage::space()
```

!!! note "戻り値"
	size_t



### data()



```c
uint8_t * AsyncUDPMessage::data()
```

!!! note "戻り値"
	uint8_t*



### length()



```c
size_t AsyncUDPMessage::length()
```

!!! note "戻り値"
	size_t



### flush()



```c
void AsyncUDPMessage::flush()
```



### operator bool()



```c
AsyncUDPMessage::operator bool()
```



