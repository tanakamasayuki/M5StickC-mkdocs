# asio::const_buffers_1



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1const__buffers__1.html)

## メンバー





### const_buffers_1()
Construct to represent a given memory range.


```c
asio::const_buffers_1::const_buffers_1(const void *data, std::size_t size) ASIO_NOEXCEPT
```

!!! summary "引数"
	- constvoid * `data` 
	- std::size_t `size` 



### const_buffers_1()
Construct to represent a single non-modifiable buffer.


```c
asio::const_buffers_1::const_buffers_1(const const_buffer &b) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `b` 



### begin()
Get a random-access iterator to the first element.


```c
const_iterator asio::const_buffers_1::begin() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	const_iterator



### end()
Get a random-access iterator for one past the last element.


```c
const_iterator asio::const_buffers_1::end() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	const_iterator



