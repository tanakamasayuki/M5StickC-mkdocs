# list



## メンバー



























































### vListInitialise()



```c
void vListInitialise(List_t *const pxList)
```

!!! summary "引数"
	- List_t*const `pxList` 

!!! note "戻り値"
	void



### vListInitialiseItem()



```c
void vListInitialiseItem(ListItem_t *const pxItem)
```

!!! summary "引数"
	- ListItem_t*const `pxItem` 

!!! note "戻り値"
	void



### vListInsert()



```c
void vListInsert(List_t *const pxList, ListItem_t *const pxNewListItem)
```

!!! summary "引数"
	- List_t*const `pxList` 
	- ListItem_t*const `pxNewListItem` 

!!! note "戻り値"
	void



### vListInsertEnd()



```c
void vListInsertEnd(List_t *const pxList, ListItem_t *const pxNewListItem)
```

!!! summary "引数"
	- List_t*const `pxList` 
	- ListItem_t*const `pxNewListItem` 

!!! note "戻り値"
	void



### uxListRemove()



```c
UBaseType_t uxListRemove(ListItem_t *const pxItemToRemove)
```

!!! summary "引数"
	- ListItem_t*const `pxItemToRemove` 

!!! note "戻り値"
	UBaseType_t



