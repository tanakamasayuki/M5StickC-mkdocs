# asio::detail::object_pool



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/ESP32/latest/classasio_1_1detail_1_1object__pool.html)

## メンバー

### object_pool()



```c
asio::detail::object_pool< Object >::object_pool()
```



### ~object_pool()



```c
asio::detail::object_pool< Object >::~object_pool()
```



### first()



```c
Object* asio::detail::object_pool< Object >::first()
```

!!! note "戻り値"
	Object *



### alloc()



```c
Object* asio::detail::object_pool< Object >::alloc()
```

!!! note "戻り値"
	Object *



### alloc()



```c
Object* asio::detail::object_pool< Object >::alloc(Arg arg)
```

!!! summary "引数"
	- Arg `arg` 

!!! note "戻り値"
	Object *



### free()



```c
void asio::detail::object_pool< Object >::free(Object *o)
```

!!! summary "引数"
	- Object * `o` 



