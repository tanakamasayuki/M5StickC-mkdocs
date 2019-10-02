# asio::basic_io_object

Base class for all I/O objects. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1basic__io__object.html)

## メンバー







### get_io_context()




```c
asio::io_context& asio::basic_io_object< IoObjectService >::get_io_context()
```

!!! note "戻り値"
	asio::io_context&



### get_io_service()




```c
asio::io_context& asio::basic_io_object< IoObjectService >::get_io_service()
```

!!! note "戻り値"
	asio::io_context&



### get_executor()
Get the executor associated with the object.


```c
executor_type asio::basic_io_object< IoObjectService >::get_executor() ASIO_NOEXCEPT
```

!!! note "戻り値"
	executor_type



