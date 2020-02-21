# asio::executor

Polymorphic wrapper for executors. 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1executor.html)

## メンバー



### executor()
Default constructor.


```c
asio::executor::executor() ASIO_NOEXCEPT
```



### executor()
Construct from nullptr.


```c
asio::executor::executor(nullptr_t) ASIO_NOEXCEPT
```

!!! summary "引数"
	- nullptr_t `` 



### executor()
Copy constructor.


```c
asio::executor::executor(const executor &other) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `other` 



### executor()
Construct a polymorphic wrapper for the specified executor.


```c
asio::executor::executor(Executor e)
```

!!! summary "引数"
	- Executor `e` 



### executor()


Allocator-aware constructor to create a polymorphic wrapper for the specified executor. 
```c
asio::executor::executor(allocator_arg_t, const Allocator &a, Executor e)
```

!!! summary "引数"
	- allocator_arg_t `` 
	- constAllocator & `a` 
	- Executor `e` 



### ~executor()
Destructor.


```c
asio::executor::~executor()
```



### operator=()
Assignment operator.


```c
executor& asio::executor::operator=(const executor &other) ASIO_NOEXCEPT
```

!!! summary "引数"
	- const& `other` 

!!! note "戻り値"
	executor&



### operator=()
Assignment operator for .


```c
executor& asio::executor::operator=(nullptr_t) ASIO_NOEXCEPT
```

!!! summary "引数"
	- nullptr_t `` 

!!! note "戻り値"
	executor&



### operator=()


Assignment operator to create a polymorphic wrapper for the specified executor. 
```c
executor& asio::executor::operator=(ASIO_MOVE_ARG(Executor) e) ASIO_NOEXCEPT
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Executor) `e` 

!!! note "戻り値"
	executor&



### context()
Obtain the underlying execution context.


```c
execution_context& asio::executor::context() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	execution_context&



### on_work_started()
Inform the executor that it has some outstanding work to do.


```c
void asio::executor::on_work_started() const ASIO_NOEXCEPT
```



### on_work_finished()
Inform the executor that some work is no longer outstanding.


```c
void asio::executor::on_work_finished() const ASIO_NOEXCEPT
```



### dispatch()
Request the executor to invoke the given function object.

This function is used to ask the executor to execute the given function object. The function object is executed according to the rules of the target executor object.
```c
void asio::executor::dispatch(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### post()
Request the executor to invoke the given function object.

This function is used to ask the executor to execute the given function object. The function object is executed according to the rules of the target executor object.
```c
void asio::executor::post(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### defer()
Request the executor to invoke the given function object.

This function is used to ask the executor to execute the given function object. The function object is executed according to the rules of the target executor object.
```c
void asio::executor::defer(ASIO_MOVE_ARG(Function) f, const Allocator &a) const
```

!!! summary "引数"
	- ASIO_MOVE_ARG(Function) `f` The function object to be called. The executor will make a copy of the handler object as required. The function signature of the function object must be:
	- constAllocator & `a` An allocator that may be used by the executor to allocate the internal storage needed for function invocation. 



### operator unspecified_bool_type()
Operator to test if the executor contains a valid target.


```c
asio::executor::operator unspecified_bool_type() const ASIO_NOEXCEPT
```



### target_type()
Obtain type information for the target executor object.



```c
const std::type_info& asio::executor::target_type() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	conststd::type_info & If  has a target type of type , ; otherwise, . 



### target()
Obtain a pointer to the target executor object.



```c
Executor * asio::executor::target() ASIO_NOEXCEPT
```

!!! note "戻り値"
	Executor * If , a pointer to the stored executor target; otherwise, a null pointer. 



### target()
Obtain a pointer to the target executor object.



```c
const Executor * asio::executor::target() const ASIO_NOEXCEPT
```

!!! note "戻り値"
	constExecutor * If , a pointer to the stored executor target; otherwise, a null pointer. 



### unspecified_bool_true()



```c
static void asio::executor::unspecified_bool_true(unspecified_bool_type_t)
```

!!! summary "引数"
	- unspecified_bool_type_t `` 







