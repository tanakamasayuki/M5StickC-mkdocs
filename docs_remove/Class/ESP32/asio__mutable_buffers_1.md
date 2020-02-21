# asio::mutable_buffers_1



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1mutable__buffers__1.html)

## メンバー





### mutable_buffers_1()
Construct to represent a given memory range.


```c
asio::mutable_buffers_1::mutable_buffers_1(void *data, std::size_t size) ASIO_NOEXCEPT
```

!!! summary "引数"
	- void * `data` 
	- std::size_t `size` 



### mutable_buffers_1()
Construct to represent a single modifiable buffer.


```c
asio::mutable_buffers_1::mutable_buffers_1(const mutable_buffer &b) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `b` 



### begin()
Get a random-access iterator to the first element.


```c
const_iterator asio::mutable_buffers_1::begin() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	const_iterator



### end()
Get a random-access iterator for one past the last element.


```c
const_iterator asio::mutable_buffers_1::end() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	const_iterator



