# FP

API for managing Function Pointers 

## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_f_p.html)

## メンバー

###  c_callback
Footprint for a global function
```c
retT(* FP< retT, argT >::c_callback) (argT)
```


###  method_callback
Footprint for a member function
```c
retT(FPtrDummy::* FP< retT, argT >::method_callback) (argT)
```


### FP()


Create the  object - only one callback can be attached to the object, that is a member function or a global function, not both at the same time 
```c
FP< retT, argT >::FP()
```



### attach()



```c
void FP< retT, argT >::attach(T *item, retT(T::*method)(argT))
```

!!! summary "引数"
	- T * `item` - Address of the initialized object 
	- retT(T::*)(argT) `method` 



### attach()



```c
void FP< retT, argT >::attach(retT(*function)(argT))
```

!!! summary "引数"
	- retT(*)(argT) `function` - The address of a globally defined function 



### operator()()



```c
retT FP< retT, argT >::operator()(argT arg) const
```

!!! summary "引数"
	- argT `arg` - An argument that is passed into the function handler that is called 

!!! note "戻り値"
	retT The return from the function hanlder called by this class 



### attached()


Determine if an callback is currently hooked 

```c
bool FP< retT, argT >::attached()
```

!!! note "戻り値"
	bool 1 if a method is hooked, 0 otherwise 



### detach()


Release a function from the callback hook 
```c
void FP< retT, argT >::detach()
```



