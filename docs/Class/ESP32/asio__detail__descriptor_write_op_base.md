# asio::detail::descriptor_write_op_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1descriptor__write__op__base.html)

## メンバー

### descriptor_write_op_base()



```c
asio::detail::descriptor_write_op_base< ConstBufferSequence >::descriptor_write_op_base(int descriptor, const ConstBufferSequence &buffers, func_type complete_func)
```

!!! summary "引数"
	- int `descriptor` 
	- constConstBufferSequence & `buffers` 
	- func_type `complete_func` 



### do_perform()



```c
static status asio::detail::descriptor_write_op_base< ConstBufferSequence >::do_perform(reactor_op *base)
```

!!! summary "引数"
	- reactor_op* `base` 

!!! note "戻り値"
	status



