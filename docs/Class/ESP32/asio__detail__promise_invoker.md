# asio::detail::promise_invoker



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1promise__invoker.html)

## メンバー

### promise_invoker()



```c
asio::detail::promise_invoker< T, F >::promise_invoker(const shared_ptr< std::promise< T > > &p, ASIO_MOVE_ARG(F) f)
```

!!! summary "引数"
	- constshared_ptr< std::promise<  > > & `p` 
	- ASIO_MOVE_ARG(F) `f` 



### operator()()



```c
void asio::detail::promise_invoker< T, F >::operator()()
```



