###  Button()

```c
Button::Button(uint8_t pin, uint8_t invert, uint32_t dbTime)
```



### ボタンの状態更新 read()
ボタンの状態を更新する。この関数を呼び出さないとボタンの状態は更新されない。ただし個別に呼び出すのではなく、M5.update()で一括して状態を更新する。
```c
uint8_t Button::read()
```

!!! note "戻り値"
	1:現在ボタンが押されている, 0:その他の状態

!!! Tip "利用例"
	```c
	void loop() {
	 M5.update();
	} 
	```



### 現在ボタンが押されているか取得 isPressed()
現在ボタンが押されているかを取得する。1の状態が続く限り1を返却する。
```c
uint8_t Button::isPressed()
```

!!! note "戻り値"
	uint8_t 1:現在ボタンが押されている, 0:その他の状態

!!! Tip "利用例"
	```c
	int btnA = M5.BtnA.isPressed(); // ホームボタン
	int btnB = M5.BtnB.isPressed(); // 右ボタン 
	```



### 現在ボタンが押されていないか取得 isReleased()
現在ボタンが押されていないかを取得する。1の状態が続く限り1を返却する。
```c
uint8_t Button::isReleased()
```

!!! note "戻り値"
	1:現在ボタンが押されていない, 0:その他の状態

!!! Tip "利用例"
	```c
	int btnA = M5.BtnA.isReleased(); // ホームボタン
	int btnB = M5.BtnB.isReleased(); // 右ボタン 
	```



### ボタンが押されたか取得 wasPressed()
ボタンが押されてから最初に呼び出した時だけ1を返却。状態が変更していない場合2度目からは0を返却する。
```c
uint8_t Button::wasPressed()
```

!!! note "戻り値"
	1:ボタンが押された, 0:その他の状態

!!! Tip "利用例"
	```c
	int btnA = M5.BtnA.wasPressed(); // ホームボタン
	int btnB = M5.BtnB.wasPressed(); // 右ボタン 
	```



### ボタンが離されたか取得 wasReleased()
ボタンが押して、離してから最初に呼び出した時だけ1を返却。状態が変更していない場合2度目からは0を返却する。 一般的なボタンを押した条件として利用する。
```c
uint8_t Button::wasReleased()
```

!!! note "戻り値"
	1:ボタンが押され離された, 0:その他の状態

!!! Tip "利用例"
	```c
	int btnA = M5.BtnA.wasReleased(); // ホームボタン
	int btnB = M5.BtnB.wasReleased(); // 右ボタン 
	```



### ボタンが一定時間以上押されたか取得 pressedFor()
ボタンが押されてからms以上経過したかを返却。1の状態が続く限り1を返却する。 長押し系の判定に利用する。
```c
uint8_t Button::pressedFor(uint32_t ms)
```

!!! summary "引数"
	- uint32_t `ms` ミリ秒単位での判定時間

!!! note "戻り値"
	1:ボタンがms以上押された, 0:その他の状態

!!! Tip "利用例"
	```c
	int btnA = M5.BtnA.pressedFor(1000); // ホームボタン
	int btnB = M5.BtnB.pressedFor(1000); // 右ボタン 
	```



### ボタンを離してから一定時間以上経過したか取得 releasedFor()
ボタンが離されてからms以上経過したかを返却。1の状態が続く限り1を返却する。 連打防止などで一定時間経過後にフラグリセットなどを行う場合に利用する。
```c
uint8_t Button::releasedFor(uint32_t ms)
```

!!! summary "引数"
	- uint32_t `ms` ミリ秒単位での判定時間

!!! note "戻り値"
	1:ボタンを離してからms以上経過した, 0:その他の状態

!!! Tip "利用例"
	```c
	int btnA = M5.BtnA.releasedFor(1000); // ホームボタン
	int btnB = M5.BtnB.releasedFor(1000); // 右ボタン 
	```



### ボタンを離してから一定時間以上経過したか取得 wasReleasefor()
ボタンをms以上押してから、離して最初に呼び出した時だけ1を返却。状態が変更していない場合2度目からは0を返却する。 非常に短い時間を指定するとチャタリング防止的に利用可能。1秒以上を指定すると長押しの判定に利用できる。
```c
uint8_t Button::wasReleasefor(uint32_t ms)
```

!!! summary "引数"
	- uint32_t `ms` ミリ秒単位での判定時間

!!! note "戻り値"
	1:ms以上ボタンを押してから離した, 0:その他の状態

!!! Tip "利用例"
	```c
	int btnA = M5.BtnA.wasReleasefor(1000); // ホームボタン
	int btnB = M5.BtnB.wasReleasefor(1000); // 右ボタン 
	```



### ボタンが最後に状態変更した時間取得 lastChange()
最後にボタンの状態が変更された時の millis() の値を返却。現在のmillis()からの差分が経過時間になります。
```c
uint32_t Button::lastChange()
```

!!! note "戻り値"
	最後にボタンの状態が変更された時の millis() の値

!!! Tip "利用例"
	```c
	int btnA = M5.BtnA.lastChange(); // ホームボタン
	int btnB = M5.BtnB.lastChange(); // 右ボタン 
	```



