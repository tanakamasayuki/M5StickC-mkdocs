# asio::const_buffer

Holds a buffer that cannot be modified. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1const__buffer.html)

## メンバー

### const_buffer()
Construct an empty buffer.


```c
asio::const_buffer::const_buffer() ASIO_NOEXCEPT
```



### const_buffer()
Construct a buffer to represent a given memory range.


```c
asio::const_buffer::const_buffer(const void *data, std::size_t size) ASIO_NOEXCEPT
```

!!! summary "引数"
	- constvoid * `data` 
	- std::size_t `size` 



### const_buffer()
Construct a non-modifiable buffer from a modifiable one.


```c
asio::const_buffer::const_buffer(const mutable_buffer &b) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `b` 



### data()
Get a pointer to the beginning of the memory range.


```c
const void* asio::const_buffer::data() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	constvoid *



### size()
Get the size of the memory range.


```c
std::size_t asio::const_buffer::size() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t



### operator+=()
Move the start of the buffer by the specified number of bytes.


```c
const_buffer& asio::const_buffer::operator+=(std::size_t n) ASIO_NOEXCEPT
```

!!! summary "引数"
	- std::size_t `n` 

!!! note "戻り値"
	const_buffer&



### operator+()
Create a new non-modifiable buffer that is offset from the start of another.


```c
const_buffer operator+(const const_buffer &b, std::size_t n) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `b` 
	- std::size_t `n` 

!!! note "戻り値"
	const_buffer



### operator+()
Create a new non-modifiable buffer that is offset from the start of another.


```c
const_buffer operator+(std::size_t n, const const_buffer &b) ASIO_NOEXCEPT
```

!!! summary "引数"
	- std::size_t `n` 
	- const& `b` 

!!! note "戻り値"
	const_buffer



