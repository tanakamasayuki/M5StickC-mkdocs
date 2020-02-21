# GSM3MobileCellManagement



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_g_s_m3_mobile_cell_management.html)

## メンバー

### getLocation()



```c
virtual int GSM3MobileCellManagement::getLocation()
```

!!! note "戻り値"
	int



### getICCID()



```c
virtual int GSM3MobileCellManagement::getICCID()
```

!!! note "戻り値"
	int



### ready()


Get last command status 

```c
virtual int GSM3MobileCellManagement::ready()=0
```

!!! note "戻り値"
	int returns 0 if last command is still executing, 1 success, >1 error 



