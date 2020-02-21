# asio::detail::call_stack::context



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1call__stack_1_1context.html)

## メンバー

### context()



```c
asio::detail::call_stack< Key, Value >::context::context(Key *k)
```

!!! summary "引数"
	- Key * `k` 



### context()



```c
asio::detail::call_stack< Key, Value >::context::context(Key *k, Value &v)
```

!!! summary "引数"
	- Key * `k` 
	- Value & `v` 



### ~context()



```c
asio::detail::call_stack< Key, Value >::context::~context()
```



### next_by_key()



```c
Value* asio::detail::call_stack< Key, Value >::context::next_by_key() const
```

!!! note "戻り値"
	Value *



