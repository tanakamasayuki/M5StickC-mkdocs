# asio::executor::impl_base



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1executor_1_1impl_3_01system__executor_00_01_allocator_01_4.html)

## メンバー

### clone()



```c
virtual impl_base* asio::executor::impl_base::clone() const ASIO_NOEXCEPT=0
```

!!! note "戻り値"
	impl_base *



### destroy()



```c
virtual void asio::executor::impl_base::destroy() ASIO_NOEXCEPT=0
```



### context()



```c
virtual execution_context& asio::executor::impl_base::context() ASIO_NOEXCEPT=0
```

!!! note "戻り値"
	execution_context&



### on_work_started()



```c
virtual void asio::executor::impl_base::on_work_started() ASIO_NOEXCEPT=0
```



### on_work_finished()



```c
virtual void asio::executor::impl_base::on_work_finished() ASIO_NOEXCEPT=0
```



### dispatch()



```c
virtual void asio::executor::impl_base::dispatch(ASIO_MOVE_ARG(function))=0
```

!!! summary "引数"
	- ASIO_MOVE_ARG() `` 



### post()



```c
virtual void asio::executor::impl_base::post(ASIO_MOVE_ARG(function))=0
```

!!! summary "引数"
	- ASIO_MOVE_ARG() `` 



### defer()



```c
virtual void asio::executor::impl_base::defer(ASIO_MOVE_ARG(function))=0
```

!!! summary "引数"
	- ASIO_MOVE_ARG() `` 



### target_type()



```c
virtual type_id_result_type asio::executor::impl_base::target_type() const ASIO_NOEXCEPT=0
```

!!! note "戻り値"
	type_id_result_type



### target()



```c
virtual void* asio::executor::impl_base::target() ASIO_NOEXCEPT=0
```

!!! note "戻り値"
	void *



### target()



```c
virtual const void* asio::executor::impl_base::target() const ASIO_NOEXCEPT=0
```

!!! note "戻り値"
	constvoid *



### equals()



```c
virtual bool asio::executor::impl_base::equals(const impl_base *e) const ASIO_NOEXCEPT=0
```

!!! summary "引数"
	- constimpl_base * `e` 

!!! note "戻り値"
	bool



