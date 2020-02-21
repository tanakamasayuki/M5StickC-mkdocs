# asio::detail::socket_holder



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1socket__holder.html)

## メンバー

### socket_holder()



```c
asio::detail::socket_holder::socket_holder()
```



### socket_holder()



```c
asio::detail::socket_holder::socket_holder(socket_type s)
```

!!! summary "引数"
	- socket_type `s` 



### ~socket_holder()



```c
asio::detail::socket_holder::~socket_holder()
```



### get()



```c
socket_type asio::detail::socket_holder::get() const
```

!!! note "戻り値"
	socket_type



### reset()



```c
void asio::detail::socket_holder::reset()
```



### reset()



```c
void asio::detail::socket_holder::reset(socket_type s)
```

!!! summary "引数"
	- socket_type `s` 



### release()



```c
socket_type asio::detail::socket_holder::release()
```

!!! note "戻り値"
	socket_type



