# asio::error_category

Base class for all error categories. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1error__category.html)

## メンバー

### ~error_category()
Destructor.


```c
virtual asio::error_category::~error_category()
```



### name()
Returns a string naming the error gategory.


```c
virtual const char* asio::error_category::name() const =0
```

!!! note "戻り値"
	constchar *



### message()
Returns a string describing the error denoted by .


```c
virtual std::string asio::error_category::message(int value) const =0
```

!!! summary "引数"
	- int `value` 

!!! note "戻り値"
	std::string



### operator==()
Equality operator to compare two error categories.


```c
bool asio::error_category::operator==(const error_category &rhs) const
```

!!! summary "引数"
	- const& `rhs` 

!!! note "戻り値"
	bool



### operator!=()
Inequality operator to compare two error categories.


```c
bool asio::error_category::operator!=(const error_category &rhs) const
```

!!! summary "引数"
	- const& `rhs` 

!!! note "戻り値"
	bool



