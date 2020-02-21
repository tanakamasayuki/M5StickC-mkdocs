# asio::dynamic_vector_buffer

Adapt a vector to the DynamicBuffer requirements. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1dynamic__vector__buffer.html)

## メンバー





### dynamic_vector_buffer()
Construct a dynamic buffer from a string.


```c
asio::dynamic_vector_buffer< Elem, Allocator >::dynamic_vector_buffer(std::vector< Elem, Allocator > &v, std::size_t maximum_size=(std::numeric_limits< std::size_t >::max)()) ASIO_NOEXCEPT
```

!!! summary "引数"
	- std::vector< Elem, Allocator > & `v` The vector to be used as backing storage for the dynamic buffer. Any existing data in the vector is treated as the dynamic buffer's input sequence. The object stores a reference to the vector and the user is responsible for ensuring that the vector object remains valid until the  object is destroyed.
	- std::size_t `maximum_size` Specifies a maximum size for the buffer, in bytes. 



### size()
Get the size of the input sequence.


```c
std::size_t asio::dynamic_vector_buffer< Elem, Allocator >::size() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t



### max_size()
Get the maximum size of the dynamic buffer.



```c
std::size_t asio::dynamic_vector_buffer< Elem, Allocator >::max_size() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t The allowed maximum of the sum of the sizes of the input sequence and output sequence. 



### capacity()
Get the current capacity of the dynamic buffer.



```c
std::size_t asio::dynamic_vector_buffer< Elem, Allocator >::capacity() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	std::size_t The current total capacity of the buffer, i.e. for both the input sequence and output sequence. 



### data()
Get a list of buffers that represents the input sequence.




```c
const_buffers_type asio::dynamic_vector_buffer< Elem, Allocator >::data() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	const_buffers_type An object of type  that satisfies ConstBufferSequence requirements, representing the basic_string memory in input sequence.



### prepare()


Get a list of buffers that represents the output sequence, with the given size. Ensures that the output sequence can accommodate  bytes, resizing the basic_string object as necessary.
```c
mutable_buffers_type asio::dynamic_vector_buffer< Elem, Allocator >::prepare(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` 

!!! note "戻り値"
	mutable_buffers_type



### commit()
Move bytes from the output sequence to the input sequence.



```c
void asio::dynamic_vector_buffer< Elem, Allocator >::commit(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` The number of bytes to append from the start of the output sequence to the end of the input sequence. The remainder of the output sequence is discarded.



### consume()
Remove characters from the input sequence.



```c
void asio::dynamic_vector_buffer< Elem, Allocator >::consume(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` 



