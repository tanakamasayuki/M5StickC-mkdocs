# asio::detail::descriptor_read_op_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1descriptor__read__op__base.html)

## メンバー

### descriptor_read_op_base()



```c
asio::detail::descriptor_read_op_base< MutableBufferSequence >::descriptor_read_op_base(int descriptor, const MutableBufferSequence &buffers, func_type complete_func)
```

!!! summary "引数"
	- int `descriptor` 
	- constMutableBufferSequence & `buffers` 
	- func_type `complete_func` 



### do_perform()



```c
static status asio::detail::descriptor_read_op_base< MutableBufferSequence >::do_perform(reactor_op *base)
```

!!! summary "引数"
	- reactor_op* `base` 

!!! note "戻り値"
	status



