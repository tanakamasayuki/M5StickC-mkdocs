# asio::bad_executor

Exception thrown when trying to access an empty polymorphic executor. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1bad__executor.html)

## メンバー

### bad_executor()
Constructor.


```c
ASIO_DECL asio::bad_executor::bad_executor() ASIO_NOEXCEPT
```

!!! note "戻り値"
	ASIO_DECL



### what()
Obtain message associated with exception.


```c
virtual ASIO_DECL const char* asio::bad_executor::what() const ASIO_NOEXCEPT_OR_NOTHROW
```

!!! note "戻り値"
	ASIO_DECLchar *



