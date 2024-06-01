+++
title = 'Review GR in short time'
date = 2024-05-31T20:01:54+08:00
draft = false
+++
## 重要概念
- 弱等效原理：$m_G/m_I$是常数。
- 强等效原理（爱因斯坦等效原理）：1. 满足WEP成立 2. 宇宙中任意时空点，存在一个自由降落的局部惯性系，其中所有非引力的物理定律取狭义相对论形式。（广义相对论的基础）爱因斯坦等效原理是一切引力几何化的基石！
- 协变理论：一个物理理论完全由张量或者张量的协变导数构成称为协变理论
- 广义协变原理：如果一个方程在没有引力场时成立，若这个方程是协变的，那么它在有引力场时也成立
- 施瓦西度规：描述球对称天体的外部引力场，是爱因斯坦方程的真空解
> 性质：1. 和时间无关 2. 完全球对称
> 施瓦西半径：$r=\frac{2GM}{c^2}$，太阳是3km \
> ISCO：最小稳定轨道，绕施瓦西黑洞旋转的粒子是有轨道半径下限的，并不是任意小的 \
> Birkhoff定理：任何电中性对称球体的外部引力场总是静态施瓦西度规
- BCRS：质心天球坐标系，全局系
- GCRS：地心天球坐标系，局部系
- TCB：BCRS中的坐标时
- TCG：GCRS中的坐标时
- TAI：国际原子时
- TT：地球时，与TAI仅相差固定常数
- 尺缩效应：沿杆子方向运动的杆子的长度比它静止时的长度短
- 钟慢效应：运动的时钟变慢。光线是长度为0，$ds^2=0$的曲线
- 双生子佯谬：
- 车库佯谬：
- 标准钟：时间读数=线长
- 固有时（原时）具有物理意义，依赖模型
- 坐标时没有物理意义，依赖模型
- 固有时和坐标时的关系
- 能动张量：分为点粒子的和理想流体的
- 四维坐标$$X^\mu=(ct,x^i(t))$$
- 时间膨胀$$t=\gamma \tau$$
- 四速度，定义$\frac{dx^\mu}{d \tau}$$$U^\mu=(\gamma c,\gamma u^i)$$
- 光线偏折：光线在通过强引力场附近时会发生弯曲
- 引力偏折：就是光线偏折
- 引力时延：光线在传播时间上发生延迟
- 引力红移：光线在强引力场作用下会出现拉伸现象，波长变长，向红波方向偏移
- 近日进动：（水星进动）后牛顿轨道是一个进动的椭圆（后牛顿推出，天体球对称，静止）
- Lense-Thirring进动：旋转的天体会拖拽其周围的时空，也叫参考系拖拽（假如天体有自旋）
- 测地进动：自由下落的自旋粒子的进动（地球自转轴的测地岁差）
- Thomas进动：自旋粒子在引力场中受到一个非引力的外力作用，自旋矢量会有一个额外的进动


## 几个重要公式
- 黎曼张量和度规的关系$$R_{abcd}=g^{de}R_{abc}^{\ \ \ \ \ \ e}$$
- 测地线方程$$\frac{d^2 x^\mu}{dt^2}+\Gamma^\mu_{\ \ \upsilon\sigma}\frac{d x^\upsilon}{dt} \frac{d x^\sigma}{dt} = 0$$
- 张量的协变导数 $$T^\upsilon_{\ \ \sigma;\mu}=T^\upsilon_{\ \ \sigma,\mu}+\Gamma^{\upsilon}_{\ \ \mu\alpha}T^\alpha_{\ \ \sigma}-\Gamma^{\alpha}_{\ \ \mu\sigma}T^\upsilon_{\ \ \alpha}$$
- 克氏符$$\Gamma^\sigma_{\ \ \mu \nu}=\frac{1}{2}g^{\sigma \rho}(g_{\rho \mu,\nu}+g_{\rho \nu,\mu}-g_{\mu \nu,\rho})$$
- 黎曼张量$$R^{\rho}_{\ \ \mu \upsilon \sigma}=\Gamma^\rho_{\ \ \mu \sigma,\upsilon}-\Gamma^\rho_{\ \ \upsilon \sigma,\mu}+\Gamma^\lambda_{\ \ \sigma\mu}\Gamma^\rho_{\ \ \upsilon \lambda}-\Gamma^\lambda_{\ \ \sigma\upsilon }\Gamma^\rho_{\ \ \mu \lambda}$$
- PNN度规的标准写法$$\begin{align}
g_{00}&=-\exp(-\frac{2w}{c^2})=-1+\frac{2w}{c^2}-\frac{2w^2}{c^4}+\mathcal{O_6}\\
g_{0i}&=-\frac{4w^i}{c^3}\\
g_{ij}&=\delta_{ij}\exp(\frac{2w}{c^2})+\mathcal{O}_4
\end{align}$$
- PNN度规的参数$\beta$（描述了引力场非线性的程度）和$\gamma$（描述了时空弯曲的程度）$$\begin{align}
g_{00}&=-1+\frac{2w}{c^2}-\beta\frac{4w^2}{c^4}\\
g_{0i}&=-\frac{4w^i}{c^3}\\
g_{ij}&=\delta_{ij}(1+\gamma\frac{2w}{c^2})
\end{align}$$
- PN施瓦西场的标量势$$w=\frac{GM}{r}$$ 矢量势$$w_i=0$$
- 爱因斯坦场方程$$G_{\mu \nu}=R_{\mu \nu}-\frac{1}{2}R g_{\mu \nu}=\frac{8\pi G}{c^4}T_{\mu \nu}$$
  > 是10阶PDE方程，由Bianchi恒等式只有6个独立方程，但$g_{\mu \nu}$作为方程的未知数有10个，比方程少，所以要适当选取坐标规范
