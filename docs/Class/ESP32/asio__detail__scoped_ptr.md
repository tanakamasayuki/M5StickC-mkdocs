# asio::detail::scoped_ptr



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1scoped__ptr.html)

## メンバー

### scoped_ptr()



```c
asio::detail::scoped_ptr< T >::scoped_ptr(T *p=0)
```

!!! summary "引数"
	- T* `p` 



### ~scoped_ptr()



```c
asio::detail::scoped_ptr< T >::~scoped_ptr()
```



### get()



```c
T* asio::detail::scoped_ptr< T >::get()
```

!!! note "戻り値"
	T*



### operator->()



```c
T* asio::detail::scoped_ptr< T >::operator->()
```

!!! note "戻り値"
	T*



### operator *()



```c
T& asio::detail::scoped_ptr< T >::operator *()
```

!!! note "戻り値"
	T&



### reset()



```c
void asio::detail::scoped_ptr< T >::reset(T *p=0)
```

!!! summary "引数"
	- T* `p` 



### release()



```c
T* asio::detail::scoped_ptr< T >::release()
```

!!! note "戻り値"
	T*



