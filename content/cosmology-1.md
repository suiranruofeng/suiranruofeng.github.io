+++
title = 'Cosmology 1 Newtonian Perturbation Theory'
date = 2024-05-17T01:01:19+08:00
draft = true
+++
# 牛顿微扰理论
连续性方程：
$$
\partial_t \rho=-\nabla_r\cdot(\rho \boldsymbol{u})
$$
描述了在一个固定的体积中，只有一股粒子离开或进入这个体积（用质量的通量$\rho \vec{u}$反映）时，质量密度才会发生变化。

欧拉方程
$$
(\partial_t+\boldsymbol{u}\cdot \nabla_r)\boldsymbol{u}=\frac{\nabla_r P}{\rho}-\nabla_r \Phi
$$
这里面$D_t \boldsymbol{u}=(\partial_t+\boldsymbol{u}\cdot \nabla_r)\boldsymbol{u}$表示“对流时间导数”。$P=P(\rho,T)$是压强依赖于密度和温度的关系（又叫状态方程equation of state）。后面那一项是势的梯度，表示外力（引力）。

接下来对$P$和$\rho$作微扰，其结果里带一横杠的是"背景数"（background values），有$\delta$的项是微扰部分
$$
\begin{align}
\rho(t,\boldsymbol{r}) & =\bar{\rho}(t)+\delta \rho(t,\boldsymbol{r}) \\
P(t,\boldsymbol{r}) & =\bar{P}(t)+\delta P(t,\boldsymbol{r})
\end{align}
$$
## 没有引力的静态空间

我们考虑一个静态的空间，忽略了引力$\Phi=0$然后把上面两个式子带进连续性方程和欧拉方程里，分别得到（是两个方程的线性化，线性化的内涵是略去高阶微扰）
$$
\begin{align}
\partial_t \delta \rho&=-\nabla_r \cdot(\bar{\rho} \boldsymbol{u}) \\
\bar{\rho}\partial_t \boldsymbol{u}&=-\nabla_r \delta P
\end{align}
$$
上边两个式子结合一下（分别乘$\partial_t$和$\nabla_r$然后相加一下）可以得到
$$
\partial_t^2 \delta \rho - \nabla_r^2 \delta P=0 \tag{4.1.6} \label{4.1.6}
$$
这里我们想只用$\delta \rho$写这个式子的话，我们可以考虑正压的流体$P=P(\rho)$这样就可以把压强的微扰重新写成
$$
\delta P =\frac{\partial P}{\partial\rho}\delta \rho \equiv c_s^2 \delta \rho
$$
这里面$c_s$就是流体的声速（**声速是介质中微弱压强扰动的传播速度**）。
那我们$\eqref{4.1.6}$式子就可以变成
$$
(\partial_t^2-c_s^2 \nabla^2_r)\delta \rho=0 \tag{4.1.7}\label{4.1.7}
$$
这显然是一个波动方程，那么它的平面波解自然就是
$$
\delta \rho(\boldsymbol{r},t)=\boldsymbol{A_k}\sin(wt-\boldsymbol{k \cdot r})+\boldsymbol{B_k}\cos(wt-\boldsymbol{k \cdot
 r})
$$
这里面有波矢（空间的频率）$\boldsymbol{k}$和频率（时间的频率）$w$

>傅里叶变换$\delta \rho$从真实空间变换到傅里叶空间
$$
\delta \rho(t,\boldsymbol{r})=\int\frac{d^3 k}{(2\pi)^3}e^{i\boldsymbol{k\cdot r}}\delta \rho_(t,\boldsymbol{k})
$$
带入偏微分方程$\eqref{4.1.7}$就可以得到（空间导数项把$ik$pull down下来变成$-k^2$）
$$
(\partial_t^2+c_s^2k^2)\delta \rho_(t,\boldsymbol{k})=0
$$
它的解是
$$
\delta \rho_(t,\boldsymbol{k})=\boldsymbol{C_k}e^{iw_kt}+\boldsymbol{D_k}e^{-iw_kt}, \quad w_\boldsymbol{k}\equiv c_sk
$$
这和平面波解是一致的。

## 有引力的静态空间

现在考虑有外力（引力）的情况，$\Phi$的大小是由泊松方程通过局域密度决定的
$$
\nabla^2 \Phi=4\pi G \rho
$$
再和没有考虑引力中的一样，将微扰带进连续性方程和欧拉方程中，分别得到
$$
\begin{align}
\partial_t \delta \rho&=-\nabla_r \cdot(\bar{\rho} \boldsymbol{u}) \\
\bar{\rho}\partial_t \boldsymbol{u}&=-\nabla_r \delta P-\bar{\rho}\nabla_r \delta \Phi
\end{align}
$$
其中$\delta \Phi =\Phi-\bar{\Phi}$满足泊松方程
$$
\nabla^2 \delta\Phi=4\pi G \delta \rho
$$
同样把上面的两个式子结合得到一个新的波动方程
$$
(\partial_t^2-c_s^2 \nabla^2_r-4\pi G \bar{\rho})\delta \rho=0 
$$
对$\delta \rho$作傅里叶变换后上面的波动方程变成
$$
(\partial_t^2+c_s^2 \boldsymbol{k}^2-4\pi G \bar{\rho})\delta \rho=0 
$$
讨论这个式子，我们可以得到一个临界波数，称为Jeans尺度，可以使得对时间导数为0
$$
k_J\equiv \frac{\sqrt{4 \pi G \rho}}{c_s}
$$
所以这个式子的解的性质可以考虑$k$和$k_J$的关系
当波速$k$比较大（波长$\lambda$比较小）时，压强占主导，与之前的解有类似的波动形式
当波速$k$比较小（波长$\lambda$比较大）时，引力占主导，极端些我们直接忽略掉压强项得到
$$
(\partial_t^2-4 \pi G \rho)\delta \rho =0
$$
这个微分方程的解为
$$
\delta \rho \propto \exp(\pm\frac{t}{\sqrt{4 \pi G \bar{\rho}}})
$$
这样随着时间指数增长的扰动称之为Jeans不稳定性。
>Jeans长度
$$
\lambda_J=\frac{2 \pi}{k_J}=c_s\sqrt{\frac{\pi}{G \bar{\rho}}}
$$

## 膨胀的空间

现在考虑膨胀的空间而非上面的静止的空间，首先膨胀可以用物理坐标$\boldsymbol{r}$和共动坐标$\boldsymbol{x}$来定义
$$
\boldsymbol{r}=a(t)\boldsymbol{x}
$$
那么物理速度就可以写成
$$
\boldsymbol{u}(t)=\dot{\boldsymbol{r}}=\dot{a}\boldsymbol{x}+\dot{\boldsymbol{x}}a=\frac{\dot{a}}{a}a\boldsymbol{x}+a\dot{\boldsymbol{x}}=H\boldsymbol{r}+\boldsymbol{v}
$$
这里面
