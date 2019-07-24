# TextManager



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_text_manager.html)

## メンバー

### setMargin()



```c
void TextManager::setMargin(int margin_left, int margin_top)
```

!!! summary "引数"
	- int `margin_left` 
	- int `margin_top` 



### writeText()



```c
void TextManager::writeText(int lineNum, int colNum, char *txt, bool onOff=true)
```

!!! summary "引数"
	- int `lineNum` 
	- int `colNum` 
	- char * `txt` 
	- bool `onOff` 



### writeScript()



```c
void TextManager::writeScript(int seq, int line, int col)
```

!!! summary "引数"
	- int `seq` 
	- int `line` 
	- int `col` 



### input()



```c
void TextManager::input(int lin, int col, int code)
```

!!! summary "引数"
	- int `lin` 
	- int `col` 
	- int `code` 



### getInput()



```c
void TextManager::getInput(int lin, int col)
```

!!! summary "引数"
	- int `lin` 
	- int `col` 



### setInputPool()



```c
void TextManager::setInputPool(int code)
```

!!! summary "引数"
	- int `code` 



### pushInput()



```c
void TextManager::pushInput(int code)
```

!!! summary "引数"
	- int `code` 



### showPicture()



```c
void TextManager::showPicture(char *filename, int posX, int posY)
```

!!! summary "引数"
	- char * `filename` 
	- int `posX` 
	- int `posY` 



