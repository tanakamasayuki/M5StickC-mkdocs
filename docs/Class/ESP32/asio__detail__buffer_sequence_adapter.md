# asio::detail::buffer_sequence_adapter



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1buffer__sequence__adapter.html)

## メンバー

### buffer_sequence_adapter()



```c
asio::detail::buffer_sequence_adapter< Buffer, Buffers >::buffer_sequence_adapter(const Buffers &buffer_sequence)
```

!!! summary "引数"
	- constBuffers & `buffer_sequence` 



### buffers()



```c
native_buffer_type* asio::detail::buffer_sequence_adapter< Buffer, Buffers >::buffers()
```

!!! note "戻り値"
	native_buffer_type*



### count()



```c
std::size_t asio::detail::buffer_sequence_adapter< Buffer, Buffers >::count() const
```

!!! note "戻り値"
	std::size_t



### total_size()



```c
std::size_t asio::detail::buffer_sequence_adapter< Buffer, Buffers >::total_size() const
```

!!! note "戻り値"
	std::size_t



### all_empty()



```c
bool asio::detail::buffer_sequence_adapter< Buffer, Buffers >::all_empty() const
```

!!! note "戻り値"
	bool



### all_empty()



```c
static bool asio::detail::buffer_sequence_adapter< Buffer, Buffers >::all_empty(const Buffers &buffer_sequence)
```

!!! summary "引数"
	- constBuffers & `buffer_sequence` 

!!! note "戻り値"
	bool



### validate()



```c
static void asio::detail::buffer_sequence_adapter< Buffer, Buffers >::validate(const Buffers &buffer_sequence)
```

!!! summary "引数"
	- constBuffers & `buffer_sequence` 



### first()



```c
static Buffer asio::detail::buffer_sequence_adapter< Buffer, Buffers >::first(const Buffers &buffer_sequence)
```

!!! summary "引数"
	- constBuffers & `buffer_sequence` 

!!! note "戻り値"
	Buffer



