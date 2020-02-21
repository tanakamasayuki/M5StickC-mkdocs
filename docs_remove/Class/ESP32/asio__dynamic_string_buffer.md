# asio::dynamic_string_buffer

Adapt a basic_string to the DynamicBuffer requirements. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1dynamic__string__buffer.html)

## メンバー





### dynamic_string_buffer()
Construct a dynamic buffer from a string.


```c
asio::dynamic_string_buffer< Elem, Traits, Allocator >::dynamic_string_buffer(std::basic_string< Elem, Traits, Allocator > &s, std::size_t maximum_size=(std::numeric_limits< std::size_t >::max)()) ASIO_NOEXCEPT
```

!!! summary "引数"
	- std::basic_string< Elem, Traits, Allocator > & `s` The string to be used as backing storage for the dynamic buffer. Any existing data in the string is treated as the dynamic buffer's input sequence. The object stores a reference to the string and the user is responsible for ensuring that the string object remains valid until the  object is destroyed.
	- std::size_t `maximum_size` Specifies a maximum size for the buffer, in bytes. 



### size()
Get the size of the input sequence.


```c
std::size_t asio::dynamic_string_buffer< Elem, Traits, Allocator >::size() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t



### max_size()
Get the maximum size of the dynamic buffer.



```c
std::size_t asio::dynamic_string_buffer< Elem, Traits, Allocator >::max_size() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t The allowed maximum of the sum of the sizes of the input sequence and output sequence. 



### capacity()
Get the current capacity of the dynamic buffer.



```c
std::size_t asio::dynamic_string_buffer< Elem, Traits, Allocator >::capacity() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t The current total capacity of the buffer, i.e. for both the input sequence and output sequence. 



### data()
Get a list of buffers that represents the input sequence.




```c
const_buffers_type asio::dynamic_string_buffer< Elem, Traits, Allocator >::data() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	const_buffers_type An object of type  that satisfies ConstBufferSequence requirements, representing the basic_string memory in input sequence.



### prepare()


Get a list of buffers that represents the output sequence, with the given size. Ensures that the output sequence can accommodate  bytes, resizing the basic_string object as necessary.
```c
mutable_buffers_type asio::dynamic_string_buffer< Elem, Traits, Allocator >::prepare(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` 

!!! note "戻り値"
	mutable_buffers_type



### commit()
Move bytes from the output sequence to the input sequence.



```c
void asio::dynamic_string_buffer< Elem, Traits, Allocator >::commit(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` The number of bytes to append from the start of the output sequence to the end of the input sequence. The remainder of the output sequence is discarded.



### consume()
Remove characters from the input sequence.



```c
void asio::dynamic_string_buffer< Elem, Traits, Allocator >::consume(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` 



