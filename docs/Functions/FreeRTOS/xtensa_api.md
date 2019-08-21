# xtensa_api



## メンバー





### xt_set_exception_handler()



```c
xt_exc_handler xt_set_exception_handler(int n, xt_exc_handler f)
```

!!! summary "引数"
	- int `n` 
	- xt_exc_handler `f` 

!!! note "戻り値"
	xt_exc_handler



### xt_set_interrupt_handler()



```c
xt_handler xt_set_interrupt_handler(int n, xt_handler f, void *arg)
```

!!! summary "引数"
	- int `n` 
	- xt_handler `f` 
	- void * `arg` 

!!! note "戻り値"
	xt_handler



### xt_ints_on()



```c
void xt_ints_on(unsigned int mask)
```

!!! summary "引数"
	- unsigned int `mask` 

!!! note "戻り値"
	void



### xt_ints_off()



```c
void xt_ints_off(unsigned int mask)
```

!!! summary "引数"
	- unsigned int `mask` 

!!! note "戻り値"
	void



### xt_set_intset()



```c
static void xt_set_intset(unsigned int arg)
```

!!! summary "引数"
	- unsigned int `arg` 

!!! note "戻り値"
	void



### xt_set_intclear()



```c
static void xt_set_intclear(unsigned int arg)
```

!!! summary "引数"
	- unsigned int `arg` 

!!! note "戻り値"
	void



### xt_get_interrupt_handler_arg()



```c
void* xt_get_interrupt_handler_arg(int n)
```

!!! summary "引数"
	- int `n` 

!!! note "戻り値"
	void *



