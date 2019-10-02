# asio::experimental::detail::redirect_error_handler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1experimental_1_1detail_1_1redirect__error__handler.html)

## メンバー

###  ec_

```c
asio::error_code& asio::experimental::detail::redirect_error_handler< Handler >::ec_
```


###  handler_

```c
Handler asio::experimental::detail::redirect_error_handler< Handler >::handler_
```


### redirect_error_handler()



```c
asio::experimental::detail::redirect_error_handler< Handler >::redirect_error_handler(redirect_error_t< CompletionToken > e)
```

!!! summary "引数"
	- redirect_error_t< CompletionToken > `e` 



### operator()()



```c
void asio::experimental::detail::redirect_error_handler< Handler >::operator()()
```



### operator()()



```c
enable_if< !is_same<typename decay<Arg>::type, asio::error_code>::value >::type asio::experimental::detail::redirect_error_handler< Handler >::operator()(ASIO_MOVE_ARG(Arg) arg)
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Arg) `arg` 

!!! note "戻り値"
	enable_if< !is_same< typename decay< Arg >::type,  >:: >::type



### operator()()



```c
void asio::experimental::detail::redirect_error_handler< Handler >::operator()(const asio::error_code &ec)
```

!!! summary "引数"
	- const& `ec` 



