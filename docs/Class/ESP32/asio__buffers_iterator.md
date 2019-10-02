# asio::buffers_iterator

A random access iterator over the bytes in a buffer sequence. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1buffers__iterator.html)

## メンバー











### buffers_iterator()
Default constructor. Creates an iterator in an undefined state.


```c
asio::buffers_iterator< BufferSequence, ByteType >::buffers_iterator()
```



### operator *()
Dereference an iterator.


```c
reference asio::buffers_iterator< BufferSequence, ByteType >::operator *() const
```

!!! note "戻り値"
	reference



### operator->()
Dereference an iterator.


```c
pointer asio::buffers_iterator< BufferSequence, ByteType >::operator->() const
```

!!! note "戻り値"
	pointer



### operator[]()
Access an individual element.


```c
reference asio::buffers_iterator< BufferSequence, ByteType >::operator[](std::ptrdiff_t difference) const
```

!!! summary "引数"
	- std::ptrdiff_t `difference` 

!!! note "戻り値"
	reference



### operator++()
Increment operator (prefix).


```c
buffers_iterator& asio::buffers_iterator< BufferSequence, ByteType >::operator++()
```

!!! note "戻り値"
	buffers_iterator&



### operator++()
Increment operator (postfix).


```c
buffers_iterator asio::buffers_iterator< BufferSequence, ByteType >::operator++(int)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	buffers_iterator



### operator--()
Decrement operator (prefix).


```c
buffers_iterator& asio::buffers_iterator< BufferSequence, ByteType >::operator--()
```

!!! note "戻り値"
	buffers_iterator&



### operator--()
Decrement operator (postfix).


```c
buffers_iterator asio::buffers_iterator< BufferSequence, ByteType >::operator--(int)
```

!!! summary "引数"
	- int `` 

!!! note "戻り値"
	buffers_iterator



### operator+=()
Addition operator.


```c
buffers_iterator& asio::buffers_iterator< BufferSequence, ByteType >::operator+=(std::ptrdiff_t difference)
```

!!! summary "引数"
	- std::ptrdiff_t `difference` 

!!! note "戻り値"
	buffers_iterator&



### operator-=()
Subtraction operator.


```c
buffers_iterator& asio::buffers_iterator< BufferSequence, ByteType >::operator-=(std::ptrdiff_t difference)
```

!!! summary "引数"
	- std::ptrdiff_t `difference` 

!!! note "戻り値"
	buffers_iterator&



### begin()
Construct an iterator representing the beginning of the buffers' data.


```c
static buffers_iterator asio::buffers_iterator< BufferSequence, ByteType >::begin(const BufferSequence &buffers)
```

!!! summary "引数"
	- constBufferSequence & `buffers` 

!!! note "戻り値"
	buffers_iterator



### end()
Construct an iterator representing the end of the buffers' data.


```c
static buffers_iterator asio::buffers_iterator< BufferSequence, ByteType >::end(const BufferSequence &buffers)
```

!!! summary "引数"
	- constBufferSequence & `buffers` 

!!! note "戻り値"
	buffers_iterator























