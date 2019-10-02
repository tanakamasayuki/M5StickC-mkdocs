# asio::experimental::redirect_error_t



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1experimental_1_1redirect__error__t.html)

## メンバー

###  token_

```c
CompletionToken asio::experimental::redirect_error_t< CompletionToken >::token_
```


###  ec_

```c
asio::error_code& asio::experimental::redirect_error_t< CompletionToken >::ec_
```


### redirect_error_t()
Constructor.


```c
asio::experimental::redirect_error_t< CompletionToken >::redirect_error_t(ASIO_MOVE_ARG(T) completion_token, asio::error_code &ec)
```

!!! summary "引数"
	- ASIO_MOVE_ARG() `completion_token` 
	- asio::error_code& `ec` 



