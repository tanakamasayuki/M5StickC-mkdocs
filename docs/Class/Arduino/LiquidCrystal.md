# LiquidCrystal



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/1.8.9/class_liquid_crystal.html)

## メンバー

### LiquidCrystal()



```c
LiquidCrystal::LiquidCrystal(uint8_t rs, uint8_t enable, uint8_t d0, uint8_t d1, uint8_t d2, uint8_t d3, uint8_t d4, uint8_t d5, uint8_t d6, uint8_t d7)
```

!!! summary "引数"
	- uint8_t `rs` 
	- uint8_t `enable` 
	- uint8_t `d0` 
	- uint8_t `d1` 
	- uint8_t `d2` 
	- uint8_t `d3` 
	- uint8_t `d4` 
	- uint8_t `d5` 
	- uint8_t `d6` 
	- uint8_t `d7` 



### LiquidCrystal()



```c
LiquidCrystal::LiquidCrystal(uint8_t rs, uint8_t rw, uint8_t enable, uint8_t d0, uint8_t d1, uint8_t d2, uint8_t d3, uint8_t d4, uint8_t d5, uint8_t d6, uint8_t d7)
```

!!! summary "引数"
	- uint8_t `rs` 
	- uint8_t `rw` 
	- uint8_t `enable` 
	- uint8_t `d0` 
	- uint8_t `d1` 
	- uint8_t `d2` 
	- uint8_t `d3` 
	- uint8_t `d4` 
	- uint8_t `d5` 
	- uint8_t `d6` 
	- uint8_t `d7` 



### LiquidCrystal()



```c
LiquidCrystal::LiquidCrystal(uint8_t rs, uint8_t rw, uint8_t enable, uint8_t d0, uint8_t d1, uint8_t d2, uint8_t d3)
```

!!! summary "引数"
	- uint8_t `rs` 
	- uint8_t `rw` 
	- uint8_t `enable` 
	- uint8_t `d0` 
	- uint8_t `d1` 
	- uint8_t `d2` 
	- uint8_t `d3` 



### LiquidCrystal()



```c
LiquidCrystal::LiquidCrystal(uint8_t rs, uint8_t enable, uint8_t d0, uint8_t d1, uint8_t d2, uint8_t d3)
```

!!! summary "引数"
	- uint8_t `rs` 
	- uint8_t `enable` 
	- uint8_t `d0` 
	- uint8_t `d1` 
	- uint8_t `d2` 
	- uint8_t `d3` 



### init()



```c
void LiquidCrystal::init(uint8_t fourbitmode, uint8_t rs, uint8_t rw, uint8_t enable, uint8_t d0, uint8_t d1, uint8_t d2, uint8_t d3, uint8_t d4, uint8_t d5, uint8_t d6, uint8_t d7)
```

!!! summary "引数"
	- uint8_t `fourbitmode` 
	- uint8_t `rs` 
	- uint8_t `rw` 
	- uint8_t `enable` 
	- uint8_t `d0` 
	- uint8_t `d1` 
	- uint8_t `d2` 
	- uint8_t `d3` 
	- uint8_t `d4` 
	- uint8_t `d5` 
	- uint8_t `d6` 
	- uint8_t `d7` 



### begin()



```c
void LiquidCrystal::begin(uint8_t cols, uint8_t rows, uint8_t charsize=LCD_5x8DOTS)
```

!!! summary "引数"
	- uint8_t `cols` 
	- uint8_t `rows` 
	- uint8_t `charsize` 



### clear()



```c
void LiquidCrystal::clear()
```



### home()



```c
void LiquidCrystal::home()
```



### noDisplay()



```c
void LiquidCrystal::noDisplay()
```



### display()



```c
void LiquidCrystal::display()
```



### noBlink()



```c
void LiquidCrystal::noBlink()
```



### blink()



```c
void LiquidCrystal::blink()
```



### noCursor()



```c
void LiquidCrystal::noCursor()
```



### cursor()



```c
void LiquidCrystal::cursor()
```



### scrollDisplayLeft()



```c
void LiquidCrystal::scrollDisplayLeft()
```



### scrollDisplayRight()



```c
void LiquidCrystal::scrollDisplayRight()
```



### leftToRight()



```c
void LiquidCrystal::leftToRight()
```



### rightToLeft()



```c
void LiquidCrystal::rightToLeft()
```



### autoscroll()



```c
void LiquidCrystal::autoscroll()
```



### noAutoscroll()



```c
void LiquidCrystal::noAutoscroll()
```



### setRowOffsets()



```c
void LiquidCrystal::setRowOffsets(int row1, int row2, int row3, int row4)
```

!!! summary "引数"
	- int `row1` 
	- int `row2` 
	- int `row3` 
	- int `row4` 



### createChar()



```c
void LiquidCrystal::createChar(uint8_t, uint8_t[])
```

!!! summary "引数"
	- uint8_t `` 



### setCursor()



```c
void LiquidCrystal::setCursor(uint8_t, uint8_t)
```

!!! summary "引数"
	- uint8_t `` 



### write()



```c
size_t LiquidCrystal::write(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 

!!! note "戻り値"
	size_t



### command()



```c
void LiquidCrystal::command(uint8_t)
```

!!! summary "引数"
	- uint8_t `` 



### write()



```c
virtual size_t Print::write(uint8_t)=0
```

!!! note "戻り値"
	size_t



### write()



```c
size_t Print::write(const char *str)
```

!!! note "戻り値"
	size_t



### write()



```c
size_t Print::write(const uint8_t *buffer, size_t size)
```

!!! note "戻り値"
	size_t



### write()



```c
size_t Print::write(const char *buffer, size_t size)
```

!!! note "戻り値"
	size_t



