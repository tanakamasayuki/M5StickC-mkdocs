# Bluetooth

この関数群を通常使うことはありません。BLE*系クラスを利用して呼び出してください。

## 利用例

- [Bluetooth/Bluetooth Classic](../../Bluetooth/Classic/)
- [Bluetooth/Bluetooth LE](../../Bluetooth/LE/)

## メンバー

### Bluetooth状態確認 btStarted()
Bluetoothが開始しているか確認。

```c
bool btStarted()
```

!!! note "戻り値"
	bool 開始状態



### Bluetooth利用開始 btStart()
Bluetoothを利用開始する。

```c
bool btStart()
```

!!! note "戻り値"
	bool 実行結果



### Bluetooth利用停止 btStop()
Bluetoothを利用停止する。


```c
bool btStop()
```

!!! note "戻り値"
	bool 実行結果
