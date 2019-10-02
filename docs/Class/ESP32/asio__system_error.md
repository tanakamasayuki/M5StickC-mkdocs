# asio::system_error



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1system__error.html)

## メンバー

### system_error()
Construct with an error code.


```c
asio::system_error::system_error(const error_code &ec)
```

!!! summary "引数"
	- const& `ec` 



### system_error()
Construct with an error code and context.


```c
asio::system_error::system_error(const error_code &ec, const std::string &context)
```

!!! summary "引数"
	- const& `ec` 
	- const& `context` 



### system_error()
Copy constructor.


```c
asio::system_error::system_error(const system_error &other)
```

!!! summary "引数"
	- const& `other` 



### ~system_error()
Destructor.


```c
virtual asio::system_error::~system_error()
```



### operator=()
Assignment operator.


```c
system_error& asio::system_error::operator=(const system_error &e)
```

!!! summary "引数"
	- const& `e` 

!!! note "戻り値"
	system_error&



### what()
Get a string representation of the exception.


```c
virtual const char* asio::system_error::what() const
```

!!! note "戻り値"
	constchar *



### code()
Get the error code associated with the exception.


```c
error_code asio::system_error::code() const
```

!!! note "戻り値"
	error_code



