# asio::detail::packaged_handler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1packaged__handler.html)

## メンバー





### packaged_handler()



```c
asio::detail::packaged_handler< Function, Allocator, Result >::packaged_handler(packaged_token< Function, Allocator > t)
```

!!! summary "引数"
	- packaged_token< Function, Allocator > `t` 



### get_allocator()



```c
allocator_type asio::detail::packaged_handler< Function, Allocator, Result >::get_allocator() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	allocator_type



### operator()()



```c
void asio::detail::packaged_handler< Function, Allocator, Result >::operator()()
```



