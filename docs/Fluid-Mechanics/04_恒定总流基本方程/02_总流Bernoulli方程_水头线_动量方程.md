# 第 4 章：恒定总流基本方程（二）

!!! failure "AI生成"
    本文档由AI生成，如果有更好的选择请自行移步。

## 讲义：Bernoulli Equation and Momentum Equation for Steady Total Flow

本讲义根据课件 `D10k_English_Steady total flow-Bernoulli.pdf` 整理，主要内容包括实际流体元流 Bernoulli 方程、恒定总流 Bernoulli 方程、水头线、Bernoulli 方程扩展、气流 Bernoulli 方程、泵和射流器例题，以及恒定总流动量方程。

## 学习目标

完成本讲后，你应能够：

- 写出实际流体元流 Bernoulli 方程。
- 写出恒定总流 Bernoulli 方程，并说明各项物理意义和几何意义。
- 掌握 Bernoulli 方程的适用条件和应用步骤。
- 理解水头线、总水头线和测压管水头线。
- 判断管道中可能出现真空的位置。
- 使用扩展 Bernoulli 方程处理分流、汇流和泵/水轮机能量输入输出。
- 理解低速气流的 Bernoulli 方程形式。
- 写出恒定总流动量方程，并用于求解水流对结构或管件的作用力。

## 1. 本讲内容结构

本 PDF 覆盖第 4 章后半部分：

- Section 3 Bernoulli equation for steady total flow
- Section 4 Momentum equation for steady total flow
- Chapter summary

其中 Bernoulli 部分包括：

1. Bernoulli equation for element flow of real fluid
2. Bernoulli equation for steady total flow
3. Water head line
4. Extension of Bernoulli equation

## 2. 实际流体元流 Bernoulli 方程

### 2.1 理想流体 Bernoulli 方程

理想流体、恒定、不可压缩、只受重力作用时，Bernoulli 方程为：

$$
z+\frac{p}{\rho g}+\frac{u^2}{2g}=C
$$

两断面形式：

$$
z_1+\frac{p_1}{\rho g}+\frac{u_1^2}{2g}
=
z_2+\frac{p_2}{\rho g}+\frac{u_2^2}{2g}
$$

### 2.2 实际流体元流方程

实际流体存在黏性和能量损失。因此从断面 1 到断面 2：

$$
z_1+\frac{p_1}{\rho g}+\frac{u_1^2}{2g}
=
z_2+\frac{p_2}{\rho g}+\frac{u_2^2}{2g}
+h_w'
$$

其中：

- $h_w'$：element flow 的水头损失。
- 它表示单位重量黏性流体从第一个断面流到第二个断面时损失的机械能。

### 2.3 皮托管测速原理

皮托管测速利用总压与静压之差确定流速。

根据实际流体元流 Bernoulli 方程，并考虑局部损失：

$$
h_w'=\zeta\frac{u^2}{2g}
$$

可得：

$$
u=c\sqrt{2g\Delta h}
$$

其中：

- $c$：Pitot tube factor（皮托管系数）。
- $\Delta h$：测得的水头差。
- $\zeta$：水头损失系数。

皮托管系数：

$$
c=\frac{1}{\sqrt{1-\zeta}}
$$

通常由实验确定，数值接近 1。

## 3. 恒定总流 Bernoulli 方程

### 3.1 从元流到总流

从实际流体元流方程出发：

$$
z_1+\frac{p_1}{\rho g}+\frac{u_1^2}{2g}
=
z_2+\frac{p_2}{\rho g}+\frac{u_2^2}{2g}
+h_w'
$$

对总流过流断面积分，并引入：

- 断面平均流速 $v$。
- 动能修正系数 $\alpha$。
- 平均水头损失 $h_w$。

得到恒定总流 Bernoulli 方程：

$$
z_1+\frac{p_1}{\rho g}+\alpha_1\frac{v_1^2}{2g}
=
z_2+\frac{p_2}{\rho g}+\alpha_2\frac{v_2^2}{2g}
+h_w
$$

### 3.2 各项意义

| 项 | 几何意义 | 物理意义 |
| --- | --- | --- |
| $z$ | 位置水头 | 单位重量位置势能 |
| $\frac{p}{\rho g}$ | 压强水头 | 单位重量压能 |
| $\alpha\frac{v^2}{2g}$ | 流速水头 | 单位重量平均动能 |
| $z+\frac{p}{\rho g}$ | 测压管水头 / 水力水头 | 单位重量总势能 |
| $z+\frac{p}{\rho g}+\alpha\frac{v^2}{2g}$ | 总水头 | 单位重量总机械能 |
| $h_w$ | 水头损失 | 单位重量机械能损失 |

### 3.3 总流与元流 Bernoulli 方程的区别

总流 Bernoulli 方程相较于元流方程有两点变化：

1. 用断面平均流速 $v$ 代替元流点速度 $u$。
2. 用总流平均水头损失 $h_w$ 代替元流水头损失 $h_w'$。

由于总流断面速度分布不均匀，动能项需要引入修正系数 $\alpha$。

## 4. 恒定总流 Bernoulli 方程的适用条件

恒定总流 Bernoulli 方程：

$$
z_1+\frac{p_1}{\rho g}+\alpha_1\frac{v_1^2}{2g}
=
z_2+\frac{p_2}{\rho g}+\alpha_2\frac{v_2^2}{2g}
+h_w
$$

适用条件包括：

1. Steady flow（恒定流）。
2. Incompressible fluid（不可压缩流体）。
3. Gravity is the sole mass force（质量力只有重力）。
4. 两个计算断面必须选在渐变流或均匀流断面；两断面之间可以存在急变流。
5. 总流流量沿程不变。
6. 两断面之间除水头损失外，没有机械能输入或输出。
7. 方程中每一项表示单位重量流体的平均能量。

若考虑总重量流体的能量，应将方程乘以：

$$
\rho gq_V
$$

## 5. Bernoulli 方程应用方法

课件总结为：

> Three selections & one list（三选一列）

### 5.1 选择基准面

Select datum plane。

常见选择：

- 过流断面形心所在平面。
- 自由液面。
- 使计算水头尽量为正的平面。

### 5.2 选择计算断面

Select calculation sections。

断面应选在：

- 均匀流段。
- 渐变流段。
- 已知量较多的位置。
- 包含待求未知量的位置。

### 5.3 选择计算点

Select calculation point。

常见选择：

- 管流中常取断面中心。
- 明渠流中常取自由液面。

由于渐变流断面上：

$$
z+\frac{p}{\rho g}=C
$$

因此同一断面上计算点可灵活选取。

### 5.4 列 Bernoulli 方程并求解

应用时应注意：

- 同一方程中必须采用同一压强基准。
- 通常使用相对压强。
- 出现真空时，最好使用绝对压强检查是否低于汽化压强。
- 可结合连续性方程：

$$
q_V=vA
$$

## 6. 虹吸管例题

### 6.1 问题要点

虹吸管中顶部断面可能出现负压甚至真空。

课件例题给定损失：

$$
h_{w1,2}=0.6\frac{v^2}{2g}
$$

$$
h_{w2,3}=0.5\frac{v^2}{2g}
$$

并要求求顶部断面 2 的平均压强。

### 6.2 解题思路

1. 取基准面。
2. 对断面 1 与 3 列 Bernoulli 方程，求管内平均速度 $v$。
3. 对断面 1 与 2 列 Bernoulli 方程，求 $p_2/\rho g$。
4. 得到 $p_2$ 为负值，说明顶部发生真空。

课件结果：

$$
\frac{p_2}{\rho g}=-4.29\ \mathrm{m}
$$

$$
p_2=-42.04\ \mathrm{kPa}
$$

这说明虹吸管顶部相对压强为负。

### 6.3 工程意义

为了避免 cavitation（空化），应控制虹吸管顶部高度，即 suction height，避免形成过大的真空。

## 7. 水头线

### 7.1 为什么使用水头线

Bernoulli 方程中各项单位都是长度，因此可以用几何线段描述能量沿程变化。

常见线包括：

- total head line（总水头线）。
- piezometric head line（测压管水头线）。

### 7.2 测压管水头线

Piezometric head 为：

$$
H_p=z+\frac{p}{\rho g}
$$

测压管水头线表示 $H_p$ 沿流动方向的变化。

### 7.3 总水头线

Total head 为：

$$
H=z+\frac{p}{\rho g}+\alpha\frac{v^2}{2g}
$$

总水头线表示总水头沿流动方向的变化。

总水头线与测压管水头线之间的距离为速度水头：

$$
\alpha\frac{v^2}{2g}
$$

### 7.4 水力坡降

Hydraulic slope $J$ 定义为单位长度平均水头损失：

$$
J=\frac{dh_w}{ds}
=-\frac{dH}{ds}>0
$$

### 7.5 测压管水头坡降

Slope of piezometric head $J_p$ 为：

$$
J_p=-\frac{d}{ds}
\left(
z+\frac{p}{\rho g}
\right)
$$

### 7.6 水头线性质

1. 理想流体总水头线为水平线。
2. 实际流体总水头线沿程下降。
3. 测压管水头线可以上升、下降或保持水平。
4. 均匀流中，总水头线与测压管水头线平行。
5. 总水头线与测压管水头线之间的距离等于速度水头。

### 7.7 水头线的应用

水头线可用于：

- 判断管道中可能发生真空的范围。
- 确定管道布置的最高位置。
- 分析虹吸管中的真空区。

若管道某段满足：

$$
z+\frac{p}{\rho g}\le z
$$

则：

$$
\frac{p}{\rho g}\le 0
$$

该段相对压强为零或负值，可能出现真空。

## 8. Bernoulli 方程扩展

### 8.1 分流与汇流

#### 分流

对于分流，可分别在主流与各支流之间列单位重量 Bernoulli 方程。

例如从断面 1 分到断面 2 和 3：

$$
E_1=E_2+h_{w1,2}
$$

$$
E_1=E_3+h_{w1,3}
$$

其中：

$$
E=z+\frac{p}{\rho g}+\alpha\frac{v^2}{2g}
$$

#### 汇流

对于汇流，需要考虑总能量守恒。若多个分支汇入一个断面，应使用能量流率形式：

$$
\rho gq_{V1}E_1+\rho gq_{V2}E_2
=
\rho gq_{V3}E_3
+\text{loss terms}
$$

也就是说，汇流问题不能简单对任意两支单独套用单管 Bernoulli 方程。

### 8.2 有能量输入或输出

若流动中存在水泵、风机、水轮机等机械设备，则 Bernoulli 方程改为：

$$
z_1+\frac{p_1}{\rho g}+\alpha_1\frac{v_1^2}{2g}
\pm H
=
z_2+\frac{p_2}{\rho g}+\alpha_2\frac{v_2^2}{2g}
+h_w
$$

其中：

- $+H$：泵、风机等给单位重量流体输入的能量。
- $-H$：水轮机等从单位重量流体取走的能量。

### 8.3 泵系统例题

题目：水泵将水从低水池输送到高水池，高差 $15\ \mathrm{m}$，流量：

$$
q_V=0.03\ \mathrm{m^3/s}
$$

管径：

$$
d=150\ \mathrm{mm}
$$

水泵效率：

$$
\eta_p=0.76
$$

管路损失：

$$
h_w=10\frac{v^2}{2g}
$$

求水泵轴功率。

管内平均流速：

$$
v=\frac{q_V}{A}
=\frac{0.03}{\pi(0.15)^2/4}
=1.7\ \mathrm{m/s}
$$

Bernoulli 方程可求得泵扬程：

$$
h_p=16.47\ \mathrm{m}
$$

轴功率：

$$
N_p=\frac{\rho gq_Vh_p}{\eta_p}
$$

课件结果：

$$
N_p=6.37\ \mathrm{kW}
$$

## 9. 低速气流 Bernoulli 方程

### 9.1 不可压缩气流条件

当气流速度小于约：

$$
50\ \mathrm{m/s}
$$

时，气体可近似视为不可压缩。

### 9.2 气流 Bernoulli 方程

气流计算常使用压强形式。考虑外界大气密度 $\rho_a$ 与气体密度 $\rho$ 不同，可写为：

$$
p_1+\frac{1}{2}\rho v_1^2
+(\rho_a-\rho)g(z_2-z_1)
=
p_2+\frac{1}{2}\rho v_2^2+p_w
$$

其中：

- $p_1,p_2$：静压。
- $\frac{1}{2}\rho v^2$：动压。
- $(\rho_a-\rho)g(z_2-z_1)$：位压或浮升压。
- $p_w=\rho gh_w$：压力损失。

### 9.3 特殊情况

若：

$$
\rho_a=\rho
$$

或：

$$
z_2=z_1
$$

则位压项为零，方程化为：

$$
p_1+\frac{1}{2}\rho v_1^2
=
p_2+\frac{1}{2}\rho v_2^2+p_w
$$

静压与动压之和称为 total pressure（总压）。

若气体密度远大于环境空气密度，即：

$$
\rho\gg\rho_a
$$

则可近似得到与液体总流相同的形式。

### 9.4 自然抽烟烟囱例题

烟囱问题需使用气流 Bernoulli 方程，因为烟气密度和外界空气密度不同。

课件例题给出：

- 烟囱直径 $d=1\ \mathrm{m}$。
- 烟气流量 $q_V=10\ \mathrm{m^3/s}$。
- 烟气密度 $\rho=0.7\ \mathrm{kg/m^3}$。
- 外界空气密度 $\rho_a=1.2\ \mathrm{kg/m^3}$。
- 底部入口真空度为 $10\ \mathrm{mm}$ 水柱。

通过气流 Bernoulli 方程并计入压力损失，课件求得烟囱高度：

$$
H=48.29\ \mathrm{m}
$$

## 10. 恒定总流动量方程

### 10.1 动量定理

动量定理表述为：

> 系统动量对时间的变化率等于作用在系统上的所有外力的矢量和。

即：

$$
\sum \vec F=\frac{d(m\vec u)}{dt}
$$

### 10.2 总流动量方程

对于恒定不可压缩总流，控制体入口为 1、出口为 2，则：

$$
\sum \vec F
=
\rho q_V(\beta_2\vec v_2-\beta_1\vec v_1)
$$

分量形式：

$$
\sum F_x
=
\rho q_V(\beta_2v_{2x}-\beta_1v_{1x})
$$

$$
\sum F_y
=
\rho q_V(\beta_2v_{2y}-\beta_1v_{1y})
$$

$$
\sum F_z
=
\rho q_V(\beta_2v_{2z}-\beta_1v_{1z})
$$

其含义是：

> 控制体内流体所受外力在某方向上的合力，等于该方向流出动量与流入动量之差。

### 10.3 外力包括哪些

动量方程中的 $\sum\vec F$ 包括：

1. 作用在控制体内所有流体质点上的质量力。
2. 控制体表面上的表面力，如压力、剪切力。
3. 周围固体边界对流体的总作用力。

### 10.4 适用条件

动量方程适用于：

- 理想流体或实际流体。
- 不可压缩流体。
- 恒定流。
- 控制断面选在渐变流或均匀流段。
- 控制体内部可包含急变流。
- 总流流量沿程不变。

若流量存在分支变化，则使用：

$$
\sum\vec F
=
\sum_{out}\rho q_V\beta\vec v
-
\sum_{in}\rho q_V\beta\vec v
$$

## 11. 动量方程应用步骤

使用动量方程求解时：

1. 选择控制体：通常取两个渐变流断面之间的水体。
2. 建立坐标系：确定各力和速度投影的正负方向。
3. 画受力图：标出所有外力方向。
4. 分析作用在水体上的外力，包括压力、重力、边界反力等。
5. 写出动量方程的分量式。
6. 结合连续性方程和 Bernoulli 方程求解未知量。

注意：

- 计算中通常使用相对压强。
- 若假设的边界力方向与计算结果符号相反，则实际方向与假设方向相反。
- 动量方程是矢量方程，必须注意方向和符号。

## 12. 动量方程例题整理

### 12.1 溢流坝水平作用力

题目：上游水深 $H_1=1.5\ \mathrm{m}$，下游水深 $H_2=0.6\ \mathrm{m}$，忽略水头损失，求每米宽水流对坝的水平力。

解题步骤：

1. 取水体为控制体。
2. 分析上、下游静水压力和坝面对水流的反力。
3. 写 $x$ 方向动量方程：

$$
\frac{1}{2}\rho gH_1^2
-\frac{1}{2}\rho gH_2^2
-F_R'
=
\rho q_V(v_2-v_1)
$$

4. 使用连续性方程：

$$
q_V=v_1H_1=v_2H_2
$$

5. 使用 Bernoulli 方程：

$$
H_1+\frac{v_1^2}{2g}
=
H_2+\frac{v_2^2}{2g}
$$

课件结果：

$$
F_R'=1.71\ \mathrm{kN}
$$

水流对坝的作用力与坝对水流的力大小相等、方向相反：

$$
F_R=1.71\ \mathrm{kN}
$$

### 12.2 水平 60° 弯管推力

题目：水平管道有 $60^\circ$ 弯头，入口直径：

$$
d_1=1\ \mathrm{m}
$$

出口直径：

$$
d_2=0.75\ \mathrm{m}
$$

流量：

$$
q_V=1.57\ \mathrm{m^3/s}
$$

入口压强：

$$
p_1=5.05\times 10^4\ \mathrm{Pa}
$$

忽略水头损失，求水流对弯头的水平推力。

解题关键：

1. 用连续性方程求 $v_1,v_2$：

$$
v_1=2.0\ \mathrm{m/s}
$$

$$
v_2=3.56\ \mathrm{m/s}
$$

2. 用 Bernoulli 方程求出口压强：

$$
p_2=4.616\times 10^4\ \mathrm{Pa}
$$

3. 对控制体列 $x,y$ 方向动量方程，求边界对水体的反力分量。

课件结果：

$$
F_{Rx}'=29.8\ \mathrm{kN}
$$

$$
F_{Ry}'=22.5\ \mathrm{kN}
$$

合力：

$$
F_R'=37.3\ \mathrm{kN}
$$

方向角：

$$
\theta=37.1^\circ
$$

水流对弯头的作用力与弯头对水流的作用力大小相等、方向相反。

### 12.3 高低射流碰撞消能

课件例题研究高、低射流碰撞消能。

已知坝前水深：

$$
H=150\ \mathrm{m}
$$

碰撞位置距坝面线水平距离：

$$
a=50\ \mathrm{m}
$$

距坝脚高度：

$$
z=50\ \mathrm{m}
$$

忽略水头损失，且两股射流流量相等。

课件主要结果：

- 两孔深度：

$$
h_1=6.7\ \mathrm{m},\quad h_2=93.3\ \mathrm{m}
$$

- 碰撞角：

$$
\alpha=60^\circ
$$

- 碰撞后主流方向：

$$
\theta=45^\circ
$$

- 碰撞后速度：

$$
v'=38.36\ \mathrm{m/s}
$$

- 碰撞消能效率：

$$
\eta=25\%
$$

该例体现了 Bernoulli 方程、抛体运动和动量方程的综合应用。

## 13. 常见问答整理

### 13.1 为什么动量方程中没有显式水头损失项？

水头损失实际上已经通过外力体现出来。

动量方程中的外力包括剪切力，而剪切应力与水头损失直接相关。因此动量方程不需要额外写出 $h_w$ 项。

### 13.2 计算出的力为负是什么意思？

表示实际力方向与预先假设的正方向相反。

### 13.3 未知力大小是否与控制体大小有关？

在不考虑重力等体积力的情况下，未知边界力通常与所选控制体大小无关。但实际分析时应选择便于列方程的控制体边界和计算断面。

### 13.4 “渐变流断面上不同位置的 $p/\rho g$ 为常数”是否正确？

不正确。

渐变流断面上近似满足：

$$
z+\frac{p}{\rho g}=C
$$

但由于 $z$ 不同，单独的压强水头：

$$
\frac{p}{\rho g}
$$

并不一定相等。

## 14. 第 4 章总结

### 14.1 基本概念

重要概念包括：

- element flow（元流）
- total flow（总流）
- flow cross-section（过流断面）
- point velocity（点速度）
- mean velocity（平均流速）
- gradually-varied flow（渐变流）
- rapidly-varied flow（急变流）
- momentum correction factor $\beta$
- kinetic energy correction factor $\alpha$

渐变流断面上：

$$
z+\frac{p}{\rho g}=C
$$

但该关系一般不表示不同断面之间也相等。

### 14.2 连续性方程

无分岔不可压缩总流：

$$
v_1A_1=v_2A_2
$$

或：

$$
q_{V1}=q_{V2}
$$

有分岔时：

$$
\sum q_{V,in}=\sum q_{V,out}
$$

### 14.3 Bernoulli 方程

恒定总流 Bernoulli 方程：

$$
z_1+\frac{p_1}{\rho g}+\alpha_1\frac{v_1^2}{2g}
=
z_2+\frac{p_2}{\rho g}+\alpha_2\frac{v_2^2}{2g}
+h_w
$$

若有能量输入或输出：

$$
z_1+\frac{p_1}{\rho g}+\alpha_1\frac{v_1^2}{2g}\pm H
=
z_2+\frac{p_2}{\rho g}+\alpha_2\frac{v_2^2}{2g}
+h_w
$$

### 14.4 动量方程

恒定不可压缩总流动量方程：

$$
\sum\vec F
=
\rho q_V(\beta_2\vec v_2-\beta_1\vec v_1)
$$

分量式：

$$
\sum F_x
=
\rho q_V(\beta_2v_{2x}-\beta_1v_{1x})
$$

$$
\sum F_y
=
\rho q_V(\beta_2v_{2y}-\beta_1v_{1y})
$$

$$
\sum F_z
=
\rho q_V(\beta_2v_{2z}-\beta_1v_{1z})
$$

分岔流动：

$$
\sum\vec F
=
\sum_{out}\rho q_V\beta\vec v
-
\sum_{in}\rho q_V\beta\vec v
$$

### 14.5 动量方程注意事项

1. 控制断面应选在渐变流段，但控制体内部可以包含急变流。
2. 动量方程为矢量方程，应选好投影轴。
3. 注意力和速度的正负号。
4. 外力包括质量力和表面力。
5. 边界对流体的作用力方向可先假设，若结果为负，则实际方向相反。
6. 动量方程右侧是动量流出减动量流入。
7. 动量方程通常只能独立求一个未知量，多个未知量时需结合连续性方程和 Bernoulli 方程。

## 15. 关键词对照

| English | 中文 |
| --- | --- |
| Bernoulli equation | 伯努利方程 |
| Head loss | 水头损失 |
| Element flow | 元流 |
| Steady total flow | 恒定总流 |
| Total head | 总水头 |
| Piezometric head | 测压管水头 |
| Water head line | 水头线 |
| Total head line | 总水头线 |
| Piezometric head line | 测压管水头线 |
| Hydraulic slope | 水力坡降 |
| Vacuum zone | 真空区 |
| Flow division | 分流 |
| Flow confluence | 汇流 |
| Energy input | 能量输入 |
| Energy output | 能量输出 |
| Pump head | 泵扬程 |
| Airflow | 气流 |
| Static pressure | 静压 |
| Dynamic pressure | 动压 |
| Total pressure | 总压 |
| Momentum equation | 动量方程 |
| Control volume | 控制体 |
| External force | 外力 |
| Boundary force | 边界作用力 |
| Momentum correction factor | 动量修正系数 |
| Kinetic energy correction factor | 动能修正系数 |
