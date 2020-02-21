# asio::detail::recycling_allocator



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1recycling__allocator.html)

## メンバー



### recycling_allocator()



```c
asio::detail::recycling_allocator< T >::recycling_allocator()
```



### recycling_allocator()



```c
asio::detail::recycling_allocator< T >::recycling_allocator(const recycling_allocator< U > &)
```

!!! summary "引数"
	- const< U > & `` 



### allocate()



```c
T* asio::detail::recycling_allocator< T >::allocate(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` 

!!! note "戻り値"
	T*



### deallocate()



```c
void asio::detail::recycling_allocator< T >::deallocate(T *p, std::size_t n)
```

!!! summary "引数"
	- T* `p` 
	- std::size_t `n` 



