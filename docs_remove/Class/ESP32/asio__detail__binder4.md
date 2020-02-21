# asio::detail::binder4



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1binder4.html)

## メンバー

###  handler_

```c
Handler asio::detail::binder4< Handler, Arg1, Arg2, Arg3, Arg4 >::handler_
```


###  arg1_

```c
Arg1 asio::detail::binder4< Handler, Arg1, Arg2, Arg3, Arg4 >::arg1_
```


###  arg2_

```c
Arg2 asio::detail::binder4< Handler, Arg1, Arg2, Arg3, Arg4 >::arg2_
```


###  arg3_

```c
Arg3 asio::detail::binder4< Handler, Arg1, Arg2, Arg3, Arg4 >::arg3_
```


###  arg4_

```c
Arg4 asio::detail::binder4< Handler, Arg1, Arg2, Arg3, Arg4 >::arg4_
```


### binder4()



```c
asio::detail::binder4< Handler, Arg1, Arg2, Arg3, Arg4 >::binder4(int, ASIO_MOVE_ARG(T) handler, const Arg1 &arg1, const Arg2 &arg2, const Arg3 &arg3, const Arg4 &arg4)
```

!!! summary "引数"
	- int `` 
	- ASIO_MOVE_ARG() `handler` 
	- constArg1 & `arg1` 
	- constArg2 & `arg2` 
	- constArg3 & `arg3` 
	- constArg4 & `arg4` 



### binder4()



```c
asio::detail::binder4< Handler, Arg1, Arg2, Arg3, Arg4 >::binder4(Handler &handler, const Arg1 &arg1, const Arg2 &arg2, const Arg3 &arg3, const Arg4 &arg4)
```

!!! summary "引数"
	- Handler & `handler` 
	- constArg1 & `arg1` 
	- constArg2 & `arg2` 
	- constArg3 & `arg3` 
	- constArg4 & `arg4` 



### operator()()



```c
void asio::detail::binder4< Handler, Arg1, Arg2, Arg3, Arg4 >::operator()()
```



### operator()()



```c
void asio::detail::binder4< Handler, Arg1, Arg2, Arg3, Arg4 >::operator()() const
```



