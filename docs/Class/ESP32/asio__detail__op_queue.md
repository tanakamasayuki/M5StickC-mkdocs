# asio::detail::op_queue



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1op__queue.html)

## メンバー

### op_queue()



```c
asio::detail::op_queue< Operation >::op_queue()
```



### ~op_queue()



```c
asio::detail::op_queue< Operation >::~op_queue()
```



### front()



```c
Operation* asio::detail::op_queue< Operation >::front()
```

!!! note "戻り値"
	Operation *



### pop()



```c
void asio::detail::op_queue< Operation >::pop()
```



### push()



```c
void asio::detail::op_queue< Operation >::push(Operation *h)
```

!!! summary "引数"
	- Operation * `h` 



### push()



```c
void asio::detail::op_queue< Operation >::push(op_queue< OtherOperation > &q)
```

!!! summary "引数"
	- op_queue< OtherOperation > & `q` 



### empty()



```c
bool asio::detail::op_queue< Operation >::empty() const
```

!!! note "戻り値"
	bool



### is_enqueued()



```c
bool asio::detail::op_queue< Operation >::is_enqueued(Operation *o) const
```

!!! summary "引数"
	- Operation * `o` 

!!! note "戻り値"
	bool



