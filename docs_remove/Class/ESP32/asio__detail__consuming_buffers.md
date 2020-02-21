# asio::detail::consuming_buffers



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1consuming__buffers.html)

## メンバー



### consuming_buffers()



```c
asio::detail::consuming_buffers< Buffer, Buffers, Buffer_Iterator >::consuming_buffers(const Buffers &buffers)
```

!!! summary "引数"
	- constBuffers & `buffers` 



### empty()



```c
bool asio::detail::consuming_buffers< Buffer, Buffers, Buffer_Iterator >::empty() const
```

!!! note "戻り値"
	bool



### prepare()



```c
prepared_buffers_type asio::detail::consuming_buffers< Buffer, Buffers, Buffer_Iterator >::prepare(std::size_t max_size)
```

!!! summary "引数"
	- std::size_t `max_size` 

!!! note "戻り値"
	prepared_buffers_type



### consume()



```c
void asio::detail::consuming_buffers< Buffer, Buffers, Buffer_Iterator >::consume(std::size_t size)
```

!!! summary "引数"
	- std::size_t `size` 



### total_consumed()



```c
std::size_t asio::detail::consuming_buffers< Buffer, Buffers, Buffer_Iterator >::total_consumed() const
```

!!! note "戻り値"
	std::size_t



