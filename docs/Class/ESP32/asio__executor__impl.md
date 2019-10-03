# asio::executor::impl



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1executor_1_1impl.html)

## メンバー

### ASIO_REBIND_ALLOC()



```c
typedef asio::executor::impl< Executor, Allocator >::ASIO_REBIND_ALLOC(Allocator, impl) allocator_type
```

!!! summary "引数"
	- impl `` 

!!! note "戻り値"
	typedef



### impl()



```c
asio::executor::impl< Executor, Allocator >::impl(const Executor &e, const Allocator &a) ASIO_NOEXCEPT
```

!!! summary "引数"
	- constExecutor & `e` 
	- constAllocator & `a` 



### clone()



```c
impl_base* asio::executor::impl< Executor, Allocator >::clone() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	impl_base *



### destroy()



```c
void asio::executor::impl< Executor, Allocator >::destroy() ASIO_NOEXCEPT
```



### on_work_started()



```c
void asio::executor::impl< Executor, Allocator >::on_work_started() ASIO_NOEXCEPT
```



### on_work_finished()



```c
void asio::executor::impl< Executor, Allocator >::on_work_finished() ASIO_NOEXCEPT
```



### context()



```c
execution_context& asio::executor::impl< Executor, Allocator >::context() ASIO_NOEXCEPT
```

!!! note "戻り値"
	execution_context&



### dispatch()



```c
void asio::executor::impl< Executor, Allocator >::dispatch(ASIO_MOVE_ARG(function) f)
```

!!! summary "引数"
	- ASIO_MOVE_ARG() `f` 



### post()



```c
void asio::executor::impl< Executor, Allocator >::post(ASIO_MOVE_ARG(function) f)
```

!!! summary "引数"
	- ASIO_MOVE_ARG() `f` 



### defer()



```c
void asio::executor::impl< Executor, Allocator >::defer(ASIO_MOVE_ARG(function) f)
```

!!! summary "引数"
	- ASIO_MOVE_ARG() `f` 



### target_type()



```c
type_id_result_type asio::executor::impl< Executor, Allocator >::target_type() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	type_id_result_type



### target()



```c
void* asio::executor::impl< Executor, Allocator >::target() ASIO_NOEXCEPT
```

!!! note "戻り値"
	void *



### target()



```c
const void* asio::executor::impl< Executor, Allocator >::target() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	constvoid *



### equals()



```c
bool asio::executor::impl< Executor, Allocator >::equals(const impl_base *e) const ASIO_NOEXCEPT
```

!!! summary "引数"
	- constimpl_base * `e` 

!!! note "戻り値"
	bool



### create()



```c
static impl_base* asio::executor::impl< Executor, Allocator >::create(const Executor &e, Allocator a=Allocator())
```

!!! summary "引数"
	- constExecutor & `e` 
	- Allocator `a` 

!!! note "戻り値"
	impl_base *



