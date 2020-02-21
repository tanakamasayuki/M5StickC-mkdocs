# asio::detail::consuming_single_buffer



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1consuming__single__buffer.html)

## メンバー

### consuming_single_buffer()



```c
asio::detail::consuming_single_buffer< Buffer >::consuming_single_buffer(const Buffer1 &buffer)
```

!!! summary "引数"
	- constBuffer1 & `buffer` 



### empty()



```c
bool asio::detail::consuming_single_buffer< Buffer >::empty() const
```

!!! note "戻り値"
	bool



### prepare()



```c
Buffer asio::detail::consuming_single_buffer< Buffer >::prepare(std::size_t max_size)
```

!!! summary "引数"
	- std::size_t `max_size` 

!!! note "戻り値"
	Buffer



### consume()



```c
void asio::detail::consuming_single_buffer< Buffer >::consume(std::size_t size)
```

!!! summary "引数"
	- std::size_t `size` 



### total_consumed()



```c
std::size_t asio::detail::consuming_single_buffer< Buffer >::total_consumed() const
```

!!! note "戻り値"
	std::size_t



