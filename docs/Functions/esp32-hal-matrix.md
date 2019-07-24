# ピンマトリクス(pinMatrix)

通常使うことがない関数群です。

## メンバー

### pinMatrixOutAttach()



```c
void pinMatrixOutAttach(uint8_t pin, uint8_t function, bool invertOut, bool invertEnable)
```

!!! summary "引数"
	- uint8_t `pin` 
	- uint8_t `function` 
	- bool `invertOut` 
	- bool `invertEnable` 

!!! note "戻り値"
	void



### pinMatrixOutDetach()



```c
void pinMatrixOutDetach(uint8_t pin, bool invertOut, bool invertEnable)
```

!!! summary "引数"
	- uint8_t `pin` 
	- bool `invertOut` 
	- bool `invertEnable` 

!!! note "戻り値"
	void



### pinMatrixInAttach()



```c
void pinMatrixInAttach(uint8_t pin, uint8_t signal, bool inverted)
```

!!! summary "引数"
	- uint8_t `pin` 
	- uint8_t `signal` 
	- bool `inverted` 

!!! note "戻り値"
	void



### pinMatrixInDetach()



```c
void pinMatrixInDetach(uint8_t signal, bool high, bool inverted)
```

!!! summary "引数"
	- uint8_t `signal` 
	- bool `high` 
	- bool `inverted` 

!!! note "戻り値"
	void



