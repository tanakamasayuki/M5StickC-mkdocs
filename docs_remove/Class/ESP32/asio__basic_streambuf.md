# asio::basic_streambuf

Automatically resizable buffer class based on std::streambuf. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1basic__streambuf.html)

## メンバー





### basic_streambuf()
Construct a  object.

Constructs a streambuf with the specified maximum size. The initial size of the streambuf's input sequence is 0. 
```c
asio::basic_streambuf< Allocator >::basic_streambuf(std::size_t maximum_size=(std::numeric_limits< std::size_t >::max)(), const Allocator &allocator=Allocator())
```

!!! summary "引数"
	- std::size_t `maximum_size` 
	- constAllocator & `allocator` 



### size()
Get the size of the input sequence.



```c
std::size_t asio::basic_streambuf< Allocator >::size() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t The size of the input sequence. The value is equal to that calculated for  in the following code:  



### max_size()
Get the maximum size of the .



```c
std::size_t asio::basic_streambuf< Allocator >::max_size() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t The allowed maximum of the sum of the sizes of the input sequence and output sequence. 



### capacity()
Get the current capacity of the .



```c
std::size_t asio::basic_streambuf< Allocator >::capacity() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t The current total capacity of the streambuf, i.e. for both the input sequence and output sequence. 



### data()
Get a list of buffers that represents the input sequence.




```c
const_buffers_type asio::basic_streambuf< Allocator >::data() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	const_buffers_type An object of type  that satisfies ConstBufferSequence requirements, representing all character arrays in the input sequence.



### prepare()


Get a list of buffers that represents the output sequence, with the given size. Ensures that the output sequence can accommodate  characters, reallocating character array objects as necessary.
```c
mutable_buffers_type asio::basic_streambuf< Allocator >::prepare(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` 

!!! note "戻り値"
	mutable_buffers_type



### commit()
Move characters from the output sequence to the input sequence.



```c
void asio::basic_streambuf< Allocator >::commit(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` 



### consume()
Remove characters from the input sequence.



```c
void asio::basic_streambuf< Allocator >::consume(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` 



