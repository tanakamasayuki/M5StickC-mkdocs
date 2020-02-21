# asio::detail::binder3



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1binder3.html)

## メンバー

###  handler_

```c
Handler asio::detail::binder3< Handler, Arg1, Arg2, Arg3 >::handler_
```


###  arg1_

```c
Arg1 asio::detail::binder3< Handler, Arg1, Arg2, Arg3 >::arg1_
```


###  arg2_

```c
Arg2 asio::detail::binder3< Handler, Arg1, Arg2, Arg3 >::arg2_
```


###  arg3_

```c
Arg3 asio::detail::binder3< Handler, Arg1, Arg2, Arg3 >::arg3_
```


### binder3()



```c
asio::detail::binder3< Handler, Arg1, Arg2, Arg3 >::binder3(int, ASIO_MOVE_ARG(T) handler, const Arg1 &arg1, const Arg2 &arg2, const Arg3 &arg3)
```

!!! summary "引数"
	- int `` 
	- ASIO_MOVE_ARG() `handler` 
	- constArg1 & `arg1` 
	- constArg2 & `arg2` 
	- constArg3 & `arg3` 



### binder3()



```c
asio::detail::binder3< Handler, Arg1, Arg2, Arg3 >::binder3(Handler &handler, const Arg1 &arg1, const Arg2 &arg2, const Arg3 &arg3)
```

!!! summary "引数"
	- Handler & `handler` 
	- constArg1 & `arg1` 
	- constArg2 & `arg2` 
	- constArg3 & `arg3` 



### operator()()



```c
void asio::detail::binder3< Handler, Arg1, Arg2, Arg3 >::operator()()
```



### operator()()



```c
void asio::detail::binder3< Handler, Arg1, Arg2, Arg3 >::operator()() const
```



