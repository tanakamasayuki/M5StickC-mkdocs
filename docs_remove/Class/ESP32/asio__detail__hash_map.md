# asio::detail::hash_map



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1hash__map.html)

## メンバー







### hash_map()



```c
asio::detail::hash_map< K, V >::hash_map()
```



### ~hash_map()



```c
asio::detail::hash_map< K, V >::~hash_map()
```



### begin()



```c
iterator asio::detail::hash_map< K, V >::begin()
```

!!! note "戻り値"
	iterator



### begin()



```c
const_iterator asio::detail::hash_map< K, V >::begin() const
```

!!! note "戻り値"
	const_iterator



### end()



```c
iterator asio::detail::hash_map< K, V >::end()
```

!!! note "戻り値"
	iterator



### end()



```c
const_iterator asio::detail::hash_map< K, V >::end() const
```

!!! note "戻り値"
	const_iterator



### empty()



```c
bool asio::detail::hash_map< K, V >::empty() const
```

!!! note "戻り値"
	bool



### find()



```c
iterator asio::detail::hash_map< K, V >::find(const K &k)
```

!!! summary "引数"
	- constK & `k` 

!!! note "戻り値"
	iterator



### find()



```c
const_iterator asio::detail::hash_map< K, V >::find(const K &k) const
```

!!! summary "引数"
	- constK & `k` 

!!! note "戻り値"
	const_iterator



### insert()



```c
std::pair<iterator, bool> asio::detail::hash_map< K, V >::insert(const value_type &v)
```

!!! summary "引数"
	- const& `v` 

!!! note "戻り値"
	iteratorstd::pair< ,  >



### erase()



```c
void asio::detail::hash_map< K, V >::erase(iterator it)
```

!!! summary "引数"
	- iterator `it` 



### erase()



```c
void asio::detail::hash_map< K, V >::erase(const K &k)
```

!!! summary "引数"
	- constK & `k` 



### clear()



```c
void asio::detail::hash_map< K, V >::clear()
```



