# asio::async_result

An interface for customising the behaviour of an initiating function. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1async__result.html)

## メンバー





### async_result()
Construct an async result from a given handler.

When using a specalised , the constructor has an opportunity to initialise some state associated with the completion handler, which is then returned from the initiating function. 
```c
asio::async_result< CompletionToken, Signature >::async_result(completion_handler_type &h)
```

!!! summary "引数"
	- completion_handler_type& `h` 



### get()
Obtain the value to be returned from the initiating function.


```c
return_type asio::async_result< CompletionToken, Signature >::get()
```

!!! note "戻り値"
	return_type



