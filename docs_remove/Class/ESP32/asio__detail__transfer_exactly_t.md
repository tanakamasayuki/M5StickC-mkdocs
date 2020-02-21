# asio::detail::transfer_exactly_t



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1transfer__exactly__t.html)

## メンバー



### transfer_exactly_t()



```c
asio::detail::transfer_exactly_t::transfer_exactly_t(std::size_t size)
```

!!! summary "引数"
	- std::size_t `size` 



### operator()()



```c
std::size_t asio::detail::transfer_exactly_t::operator()(const Error &err, std::size_t bytes_transferred)
```

!!! summary "引数"
	- constError & `err` 
	- std::size_t `bytes_transferred` 

!!! note "戻り値"
	std::size_t



