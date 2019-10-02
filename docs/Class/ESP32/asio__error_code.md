# asio::error_code

Class to represent an error code value. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1error__code.html)

## メンバー



### error_code()
Default constructor.


```c
asio::error_code::error_code()
```



### error_code()
Construct with specific error code and category.


```c
asio::error_code::error_code(int v, const error_category &c)
```

!!! summary "引数"
	- int `v` 
	- const& `c` 



### error_code()
Construct from an error code enum.


```c
asio::error_code::error_code(ErrorEnum e)
```

!!! summary "引数"
	- ErrorEnum `e` 



### clear()
Clear the error value to the default.


```c
void asio::error_code::clear()
```



### assign()
Assign a new error value.


```c
void asio::error_code::assign(int v, const error_category &c)
```

!!! summary "引数"
	- int `v` 
	- const& `c` 



### value()
Get the error value.


```c
int asio::error_code::value() const
```

!!! note "戻り値"
	int



### category()
Get the error category.


```c
const error_category& asio::error_code::category() const
```

!!! note "戻り値"
	const&



### message()
Get the message associated with the error.


```c
std::string asio::error_code::message() const
```

!!! note "戻り値"
	std::string



### operator unspecified_bool_type()
Operator returns non-null if there is a non-success error code.


```c
asio::error_code::operator unspecified_bool_type() const
```



### operator!()
Operator to test if the error represents success.


```c
bool asio::error_code::operator!() const
```

!!! note "戻り値"
	bool



### unspecified_bool_true()



```c
static void asio::error_code::unspecified_bool_true(unspecified_bool_type_t)
```

!!! summary "引数"
	- unspecified_bool_type_t `` 







