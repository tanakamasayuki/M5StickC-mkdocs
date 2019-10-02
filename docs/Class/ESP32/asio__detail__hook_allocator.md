# asio::detail::hook_allocator



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1hook__allocator.html)

## メンバー



###  handler_

```c
Handler& asio::detail::hook_allocator< Handler, T >::handler_
```


### hook_allocator()



```c
asio::detail::hook_allocator< Handler, T >::hook_allocator(Handler &h)
```

!!! summary "引数"
	- Handler & `h` 



### hook_allocator()



```c
asio::detail::hook_allocator< Handler, T >::hook_allocator(const hook_allocator< Handler, U > &a)
```

!!! summary "引数"
	- const< Handler, U > & `a` 



### allocate()



```c
T* asio::detail::hook_allocator< Handler, T >::allocate(std::size_t n)
```

!!! summary "引数"
	- std::size_t `n` 

!!! note "戻り値"
	T*



### deallocate()



```c
void asio::detail::hook_allocator< Handler, T >::deallocate(T *p, std::size_t n)
```

!!! summary "引数"
	- T* `p` 
	- std::size_t `n` 



