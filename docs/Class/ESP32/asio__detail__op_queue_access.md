# asio::detail::op_queue_access



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1op__queue__access.html)

## メンバー

### next()



```c
static Operation* asio::detail::op_queue_access::next(Operation *o)
```

!!! summary "引数"
	- Operation * `o` 

!!! note "戻り値"
	Operation *



### next()



```c
static void asio::detail::op_queue_access::next(Operation1 *&o1, Operation2 *o2)
```

!!! summary "引数"
	- Operation1 *& `o1` 
	- Operation2 * `o2` 



### destroy()



```c
static void asio::detail::op_queue_access::destroy(Operation *o)
```

!!! summary "引数"
	- Operation * `o` 



### front()



```c
static Operation*& asio::detail::op_queue_access::front(op_queue< Operation > &q)
```

!!! summary "引数"
	- op_queue< Operation > & `q` 

!!! note "戻り値"
	Operation *&



### back()



```c
static Operation*& asio::detail::op_queue_access::back(op_queue< Operation > &q)
```

!!! summary "引数"
	- op_queue< Operation > & `q` 

!!! note "戻り値"
	Operation *&



