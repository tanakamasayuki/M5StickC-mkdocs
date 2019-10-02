# asio::detail::binder2



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1binder2.html)

## メンバー

###  handler_

```c
Handler asio::detail::binder2< Handler, Arg1, Arg2 >::handler_
```


###  arg1_

```c
Arg1 asio::detail::binder2< Handler, Arg1, Arg2 >::arg1_
```


###  arg2_

```c
Arg2 asio::detail::binder2< Handler, Arg1, Arg2 >::arg2_
```


### binder2()



```c
asio::detail::binder2< Handler, Arg1, Arg2 >::binder2(int, ASIO_MOVE_ARG(T) handler, const Arg1 &arg1, const Arg2 &arg2)
```

!!! summary "引数"
	- int `` 
	- ASIO_MOVE_ARG() `handler` 
	- constArg1 & `arg1` 
	- constArg2 & `arg2` 



### binder2()



```c
asio::detail::binder2< Handler, Arg1, Arg2 >::binder2(Handler &handler, const Arg1 &arg1, const Arg2 &arg2)
```

!!! summary "引数"
	- Handler & `handler` 
	- constArg1 & `arg1` 
	- constArg2 & `arg2` 



### operator()()



```c
void asio::detail::binder2< Handler, Arg1, Arg2 >::operator()()
```



### operator()()



```c
void asio::detail::binder2< Handler, Arg1, Arg2 >::operator()() const
```



