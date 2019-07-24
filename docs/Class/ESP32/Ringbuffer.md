# Ringbuffer

. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/1.0.2/class_ringbuffer.html)

## メンバー

### Ringbuffer()
Create a ring buffer.


```c
Ringbuffer::Ringbuffer(size_t length, ringbuf_type_t type=RINGBUF_TYPE_NOSPLIT)
```

!!! summary "引数"
	- size_t `length` The amount of storage to allocate for the ring buffer. 
	- ringbuf_type_t `type` The type of buffer. One of RINGBUF_TYPE_NOSPLIT, RINGBUF_TYPE_ALLOWSPLIT, RINGBUF_TYPE_BYTEBUF. 



### ~Ringbuffer()



```c
Ringbuffer::~Ringbuffer()
```



### receive()
Receive data from the buffer.


```c
void * Ringbuffer::receive(size_t *size, TickType_t wait=portMAX_DELAY)
```

!!! summary "引数"
	- size_t * `size` On return, the size of data returned. 
	- TickType_t `wait` How long to wait. 

!!! note "戻り値"
	void * A pointer to the storage retrieved. 



### returnItem()
Return an item.


```c
void Ringbuffer::returnItem(void *item)
```

!!! summary "引数"
	- void * `item` The item to be returned/released. 



### send()
Send data to the buffer.


```c
bool Ringbuffer::send(void *data, size_t length, TickType_t wait=portMAX_DELAY)
```

!!! summary "引数"
	- void * `data` The data to place into the buffer. 
	- size_t `length` The length of data to place into the buffer. 
	- TickType_t `wait` How long to wait before giving up. The default is to wait indefinitely. 

!!! note "戻り値"
	bool 



