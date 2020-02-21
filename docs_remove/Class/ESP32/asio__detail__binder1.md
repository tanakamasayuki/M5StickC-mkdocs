# asio::detail::binder1



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1binder1.html)

## メンバー

###  handler_

```c
Handler asio::detail::binder1< Handler, Arg1 >::handler_
```


###  arg1_

```c
Arg1 asio::detail::binder1< Handler, Arg1 >::arg1_
```


### binder1()



```c
asio::detail::binder1< Handler, Arg1 >::binder1(int, ASIO_MOVE_ARG(T) handler, const Arg1 &arg1)
```

!!! summary "引数"
	- int `` 
	- ASIO_MOVE_ARG() `handler` 
	- constArg1 & `arg1` 



### binder1()



```c
asio::detail::binder1< Handler, Arg1 >::binder1(Handler &handler, const Arg1 &arg1)
```

!!! summary "引数"
	- Handler & `handler` 
	- constArg1 & `arg1` 



### operator()()



```c
void asio::detail::binder1< Handler, Arg1 >::operator()()
```



### operator()()



```c
void asio::detail::binder1< Handler, Arg1 >::operator()() const
```



