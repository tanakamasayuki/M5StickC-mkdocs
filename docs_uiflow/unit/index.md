# Unitの使い方

```python
import unit

# Unitのクラスを取得(ポート番号を指定)
env0 = unit.get(unit.ENV, unit.PORTA)

# 取得したクラスを利用する
lcd.print((env0.pressure), 0, 70, 0xffffff)
lcd.print((env0.temperature), 0, 70, 0xffffff)
lcd.print((env0.humidity), 0, 70, 0xffffff)
```

## 利用できるUnit

- [unitモジュール](../module/unit/)
- [unitsモジュール](../module/units/)

unitモジュールの定数が利用できるUnitになります。
unit.get()関数で呼び出した後に、unitsモジュールに該当クラスが追加されます。
