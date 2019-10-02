# asio::basic_streambuf_ref

Adapts  to the dynamic buffer sequence type requirements. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1basic__streambuf__ref.html)

## メンバー





### basic_streambuf_ref()
Construct a  for the given  object.


```c
asio::basic_streambuf_ref< Allocator >::basic_streambuf_ref(basic_streambuf< Allocator > &sb)
```

!!! summary "引数"
	- basic_streambuf< Allocator > & `sb` 



### basic_streambuf_ref()
Copy construct a .


```c
asio::basic_streambuf_ref< Allocator >::basic_streambuf_ref(const basic_streambuf_ref &other) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `other` 



### size()
Get the size of the input sequence.


```c
std::size_t asio::basic_streambuf_ref< Allocator >::size() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t



### max_size()
Get the maximum size of the dynamic buffer.


```c
std::size_t asio::basic_streambuf_ref< Allocator >::max_size() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t



### capacity()
Get the current capacity of the dynamic buffer.


```c
std::size_t asio::basic_streambuf_ref< Allocator >::capacity() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t



### data()
Get a list of buffers that represents the input sequence.


```c
const_buffers_type asio::basic_streambuf_ref< Allocator >::data() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	const_buffers_type



### prepare()


Get a list of buffers that represents the output sequence, with the given size. 
```c
mutable_buffers_type asio::basic_streambuf_ref< Allocator >::prepare(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` 

!!! note "戻り値"
	mutable_buffers_type



### commit()
Move bytes from the output sequence to the input sequence.


```c
void asio::basic_streambuf_ref< Allocator >::commit(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` 



### consume()
Remove characters from the input sequence.


```c
void asio::basic_streambuf_ref< Allocator >::consume(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` 



