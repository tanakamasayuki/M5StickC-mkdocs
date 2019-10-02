# PeakDetector



## 詳細情報

- [Doxygenクラスリファレンス](https://lang-ship.com/reference/Arduino/latest/class_peak_detector.html)

## メンバー

### PeakDetector()



```c
PeakDetector::PeakDetector(const int lag=5, const float threshold=3.5, const float influence=0.5)
```

!!! summary "引数"
	- constint `lag` 
	- constfloat `threshold` 
	- constfloat `influence` 



### ~PeakDetector()



```c
PeakDetector::~PeakDetector()
```



### detect()



```c
int PeakDetector::detect(float sample)
```

!!! summary "引数"
	- float `sample` 

!!! note "戻り値"
	int



### getAvg()



```c
float PeakDetector::getAvg()
```

!!! note "戻り値"
	float



### getStd()



```c
float PeakDetector::getStd()
```

!!! note "戻り値"
	float



