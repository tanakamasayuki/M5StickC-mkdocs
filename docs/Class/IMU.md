# ジャイロ加速度計(IMU)

## 概要

初期ロットに搭載されているI2Cアドレス0x6cで接続されているSH200Qと、I2Cアドレス0x68で接続されているMPU6886を内部で判定してラッピングしているクラスです。

どちらのIMUでも同じようなコードで制御することが可能です。
細かい制御が必要な場合には、個別クラスを直接制御してください。

## データシート

- 6-axis IMU [SH200Q](https://github.com/m5stack/M5-Schematic/blob/master/Core/SH200Q.pdf)
- 6-axis IMU [[MPU6886](https://github.com/m5stack/M5-Schematic/blob/master/datasheet/MPU-6886-000193%2Bv1.1_GHIC.PDF.pdf)]

## Doxygenドキュメント

- [IMU クラス](https://lang-ship.com/reference/M5StickC/latest/class_i_m_u.html)

## メンバー

### IMU種別 ImuType
搭載されているIMUが初期化時に代入される。{ IMU_UNKNOWN = 0, IMU_SH200Q, IMU_MPU6886 }
```c
ImuType IMU::imuType
```


### 加速度スケール aRes

```c
float IMU::aRes
```


### ジャイロスケール gRes

```c
float IMU::gRes
```


### コンストラクタ IMU()
処理無し
```c
IMU::IMU()
```

### 初期化 Init()
内部関数のため、通常は利用しない
```c
int IMU::Init(void)
```

!!! note "戻り値"
	0:成功, -1:失敗


### ジャイロのスケール更新 getGres()
内部関数のため、通常は利用しない
```c
void IMU::getGres()
```



### 加速度のスケール更新 getAres()
内部関数のため、通常は利用しない
```c
void IMU::getAres()
```



### 加速度取得(スケール補正前) getAccelAdc()
スケール補正されていない取得した値
```c
void IMU::getAccelAdc(int16_t *ax, int16_t *ay, int16_t *az)
```

!!! summary "引数"
	- int16_t * `ax` X軸加速度(スケール補正前)
	- int16_t * `ay` Y軸加速度(スケール補正前)
	- int16_t * `az` Z軸加速度(スケール補正前)



### ジャイロ取得(スケール補正前) getGyroAdc()
スケール補正されていない取得した値
```c
void IMU::getGyroAdc(int16_t *gx, int16_t *gy, int16_t *gz)
```

!!! summary "引数"
	- int16_t * `gx` X軸ジャイロ(スケール補正前)
	- int16_t * `gy` Y軸ジャイロ(スケール補正前)
	- int16_t * `gz` Z軸ジャイロ(スケール補正前)



### 内部温度取得 getTempAdc()
内部の温度なので気温ではありません
```c
void IMU::getTempAdc(int16_t *t)
```

!!! summary "引数"
	- int16_t * `t` 温度Step(温度 = 21.0 + 温度Step / 333.87)



### 加速度取得(スケール補正後) getAccelData()
スケール補正された値
```c
void IMU::getAccelData(float *ax, float *ay, float *az)
```

!!! summary "引数"
	- float * `ax` X軸加速度(スケール補正後)
	- float * `ay` Y軸加速度(スケール補正後)
	- float * `az` Z軸加速度(スケール補正後)



### ジャイロ取得(スケール補正後) getGyroData()
スケール補正された値
```c
void IMU::getGyroData(float *gx, float *gy, float *gz)
```

!!! summary "引数"
	- float * `gx` X軸ジャイロ(スケール補正後)
	- float * `gy` Y軸ジャイロ(スケール補正後)
	- float * `gz` Z軸ジャイロ(スケール補正後)



### 内部温度取得 getTempData()
内部の温度なので気温ではありません
```c
void IMU::getTempData(float *t)
```

!!! summary "引数"
	- float * `t` 温度

### AHRS取得 getAhrsData()
3次元空間での回転状態を(ピッチ、ロール、ヨー)を取得します。
```c
void IMU::getAhrsData(float *pitch, float *roll, float *yaw)
```

!!! summary "引数"
	- float * `pitch` ピッチ
	- float * `roll` ロール
	- float * `yaw` ヨー

## 関連ブログ
- [M5StickCの6軸IMU(SH200Q)検証](https://lang-ship.com/blog/?p=570)


