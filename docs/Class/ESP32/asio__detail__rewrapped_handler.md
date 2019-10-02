# asio::detail::rewrapped_handler



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1rewrapped__handler.html)

## メンバー

###  context_

```c
Context asio::detail::rewrapped_handler< Handler, Context >::context_
```


###  handler_

```c
Handler asio::detail::rewrapped_handler< Handler, Context >::handler_
```


### rewrapped_handler()



```c
asio::detail::rewrapped_handler< Handler, Context >::rewrapped_handler(Handler &handler, const Context &context)
```

!!! summary "引数"
	- Handler & `handler` 
	- constContext & `context` 



### rewrapped_handler()



```c
asio::detail::rewrapped_handler< Handler, Context >::rewrapped_handler(const Handler &handler, const Context &context)
```

!!! summary "引数"
	- constHandler & `handler` 
	- constContext & `context` 



### operator()()



```c
void asio::detail::rewrapped_handler< Handler, Context >::operator()()
```



### operator()()



```c
void asio::detail::rewrapped_handler< Handler, Context >::operator()() const
```



