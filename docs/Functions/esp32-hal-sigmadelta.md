# SigmaDelta変調(sigmaDelta)

PWMのようにSigmaDelta変調で電圧を制御して出力する関数群です。

## 利用例

- [Peripherals/シグマデルタ変調](../../Peripherals/Sigma-delta/)

## メンバー

### sigmaDeltaSetup()



```c
uint32_t sigmaDeltaSetup(uint8_t channel, uint32_t freq)
```

!!! summary "引数"
	- uint8_t `channel` 
	- uint32_t `freq` 

!!! note "戻り値"
	uint32_t



### sigmaDeltaWrite()



```c
void sigmaDeltaWrite(uint8_t channel, uint8_t duty)
```

!!! summary "引数"
	- uint8_t `channel` 
	- uint8_t `duty` 

!!! note "戻り値"
	void



### sigmaDeltaRead()



```c
uint8_t sigmaDeltaRead(uint8_t channel)
```

!!! summary "引数"
	- uint8_t `channel` 

!!! note "戻り値"
	uint8_t



### sigmaDeltaAttachPin()



```c
void sigmaDeltaAttachPin(uint8_t pin, uint8_t channel)
```

!!! summary "引数"
	- uint8_t `pin` 
	- uint8_t `channel` 

!!! note "戻り値"
	void



### sigmaDeltaDetachPin()



```c
void sigmaDeltaDetachPin(uint8_t pin)
```

!!! summary "引数"
	- uint8_t `pin` 

!!! note "戻り値"
	void



