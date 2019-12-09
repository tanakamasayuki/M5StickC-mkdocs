# Hatの使い方

```python
import hat

# Hatのクラスを取得
hat_env0 = hat.get(hat.ENV)

# 取得したクラスを利用する
lcd.print((hat_env0.pressure), 0, 70, 0xffffff)
lcd.print((hat_env0.temperature), 0, 70, 0xffffff)
lcd.print((hat_env0.humidity), 0, 70, 0xffffff)
```

## 利用できるHat

- [hatモジュール](../module/hat/)
- [hatsモジュール](../module/hats/)

hatモジュールの定数が利用できるHatになります。
hat.get()関数で呼び出した後に、hatsモジュールに該当クラスが追加されます。
