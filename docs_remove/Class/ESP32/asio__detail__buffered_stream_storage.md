# asio::detail::buffered_stream_storage



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1buffered__stream__storage.html)

## メンバー





### buffered_stream_storage()



```c
asio::detail::buffered_stream_storage::buffered_stream_storage(std::size_t buffer_capacity)
```

!!! summary "引数"
	- std::size_t `buffer_capacity` 



### clear()
Clear the buffer.


```c
void asio::detail::buffered_stream_storage::clear()
```



### data()



```c
mutable_buffer asio::detail::buffered_stream_storage::data()
```

!!! note "戻り値"
	mutable_buffer



### data()



```c
const_buffer asio::detail::buffered_stream_storage::data() const
```

!!! note "戻り値"
	const_buffer



### empty()



```c
bool asio::detail::buffered_stream_storage::empty() const
```

!!! note "戻り値"
	bool



### size()



```c
size_type asio::detail::buffered_stream_storage::size() const
```

!!! note "戻り値"
	size_type



### resize()



```c
void asio::detail::buffered_stream_storage::resize(size_type length)
```

!!! summary "引数"
	- size_type `length` 



### capacity()



```c
size_type asio::detail::buffered_stream_storage::capacity() const
```

!!! note "戻り値"
	size_type



### consume()



```c
void asio::detail::buffered_stream_storage::consume(size_type count)
```

!!! summary "引数"
	- size_type `count` 



