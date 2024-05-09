+++
title = 'Test'
date = 2024-03-21T10:43:52+08:00
draft = true
+++
#### 第一章
##### Q1:恒星为什么有自行？
恒星本身在宇宙中的运动。
##### Q2:自行和径向速度的关系?
自行是垂直于视线方向的运动，径向运动是沿着视线方向的运动。
##### Q3:单位为什么不一样?
⾃⾏通过恒星⾚经和⾚纬的变化来测量。通常以⻆秒/年（$arcsec/yr$）或毫⻆秒/年（$milli-arcsec/yr$）为单位
⽽径向速度通过多普勒频移来测量，通常以$km/s$为单位
##### Q4:怎样将自行变成和径向速度相同的单位？
需要通过获得恒星距离$D$来获得切向速度$V_T=\mu D$此时与径向速度量纲一致，假设$D$的单位是$km$ 由于$1\ arcsec=\frac{1}{3600}deg=\frac{2\pi}{360*3600}rad,\ 1yr=3.15\times10^7s$因此只需调整为原本数值的$\frac{2\pi}{360*3600*3.15\times10^7}$ 倍。
#### 第二章
##### 运用Gaia计算恒星距离
 $\epsilon\ CRT$ star (HD 99167)，视差为8.177988986211076$mag$
```python
def plx2d(parallex):
    AU = 0.000004848
    PI = parallex/1000*0.0000048
    d = AU/PI
    dly = d*3.2
    return d, dly
parallex = 8.177988986211076
d, dly = plx2d(parallex)
print("%s pc %s ly" % (d, dly))
```
output: 123.50224507552687 $pc$ 395.20718424168604 $ly$
#### 第三章
##### 已知太阳的绝对星等为$M_v=+4.83$，求太阳的视星等(V段)。
已知视星等和绝对星等的关系为
$$M_v-m_v=-5log(d)+5$$
将$M_v=+4.83$，日地距离$d=4.8*10^{-6}pc$ 带入得
$$m_v=-26.76$$
```python
import math
M_v = 4.83
def cal(M_v):
    d = 0.0000048
    m_v = 5* math.log10(d) - 5 + M_v
    return m_v
print(cal(M_v))
```
output:-26.763793813122064