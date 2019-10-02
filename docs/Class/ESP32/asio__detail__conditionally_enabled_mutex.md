# asio::detail::conditionally_enabled_mutex



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1conditionally__enabled__mutex.html)

## メンバー

### conditionally_enabled_mutex()



```c
asio::detail::conditionally_enabled_mutex::conditionally_enabled_mutex(bool enabled)
```

!!! summary "引数"
	- bool `enabled` 



### ~conditionally_enabled_mutex()



```c
asio::detail::conditionally_enabled_mutex::~conditionally_enabled_mutex()
```



### enabled()



```c
bool asio::detail::conditionally_enabled_mutex::enabled() const
```

!!! note "戻り値"
	bool



### lock()



```c
void asio::detail::conditionally_enabled_mutex::lock()
```



### unlock()



```c
void asio::detail::conditionally_enabled_mutex::unlock()
```



