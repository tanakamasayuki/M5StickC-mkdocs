# asio::mutable_buffer

Holds a buffer that can be modified. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1mutable__buffer.html)

## メンバー

### mutable_buffer()
Construct an empty buffer.


```c
asio::mutable_buffer::mutable_buffer() ASIO_NOEXCEPT
```



### mutable_buffer()
Construct a buffer to represent a given memory range.


```c
asio::mutable_buffer::mutable_buffer(void *data, std::size_t size) ASIO_NOEXCEPT
```

!!! summary "引数"
	- void * `data` 
	- std::size_t `size` 



### data()
Get a pointer to the beginning of the memory range.


```c
void* asio::mutable_buffer::data() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	void *



### size()
Get the size of the memory range.


```c
std::size_t asio::mutable_buffer::size() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t



### operator+=()
Move the start of the buffer by the specified number of bytes.


```c
mutable_buffer& asio::mutable_buffer::operator+=(std::size_t n) ASIO_NOEXCEPT
```

!!! summary "引数"
	- std::size_t `n` 

!!! note "戻り値"
	mutable_buffer&



### operator+()
Create a new modifiable buffer that is offset from the start of another.


```c
mutable_buffer operator+(const mutable_buffer &b, std::size_t n) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `b` 
	- std::size_t `n` 

!!! note "戻り値"
	mutable_buffer



### operator+()
Create a new modifiable buffer that is offset from the start of another.


```c
mutable_buffer operator+(std::size_t n, const mutable_buffer &b) ASIO_NOEXCEPT
```

!!! summary "引数"
	- std::size_t `n` 
	- const& `b` 

!!! note "戻り値"
	mutable_buffer



