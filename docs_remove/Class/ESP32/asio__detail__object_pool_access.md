# asio::detail::object_pool_access



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1object__pool__access.html)

## メンバー

### create()



```c
static Object* asio::detail::object_pool_access::create()
```

!!! note "戻り値"
	Object *



### create()



```c
static Object* asio::detail::object_pool_access::create(Arg arg)
```

!!! summary "引数"
	- Arg `arg` 

!!! note "戻り値"
	Object *



### destroy()



```c
static void asio::detail::object_pool_access::destroy(Object *o)
```

!!! summary "引数"
	- Object * `o` 



### next()



```c
static Object*& asio::detail::object_pool_access::next(Object *o)
```

!!! summary "引数"
	- Object * `o` 

!!! note "戻り値"
	Object *&



### prev()



```c
static Object*& asio::detail::object_pool_access::prev(Object *o)
```

!!! summary "引数"
	- Object * `o` 

!!! note "戻り値"
	Object *&



