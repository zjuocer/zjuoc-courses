# 第 3 章：流体运动基础（二）

!!! failure "AI生成"
    本文档由AI生成，如果有更好的选择请自行移步。

## 讲义：Basic Equations of Fluid Flow and Euler Integration

本讲义根据课件 `6_D07k_English.pdf` 整理，主要内容包括流体流动基本方程、连续性方程、理想流体的 Euler equations、实际流体的 Navier-Stokes equations，以及 Euler 方程在特定条件下积分得到 Bernoulli equation。

## 学习目标

完成本讲后，你应能够：

- 理解连续性方程的物理意义：质量守恒。
- 写出一般流动、恒定可压缩流和不可压缩流的连续性方程。
- 判断给定速度场是否满足不可压缩连续性方程。
- 写出理想流体的 Euler equations of motion。
- 说明实际流体与理想流体在受力和运动方程上的差异。
- 识别不可压缩 Navier-Stokes 方程中的黏性扩散项。
- 理解 Euler 方程积分的适用条件。
- 区分势流中的 Bernoulli 方程和沿流线积分的 Bernoulli 方程。
- 说明 Bernoulli 方程中各项的物理意义和几何意义。

## 1. 本讲内容结构

本 PDF 覆盖第 3 章中的两个核心小节：

- Section 4 Basic equations of fluid flow
- Section 5 Integration of Euler equations of motion

其中 Section 4 包括：

1. Continuity equation（连续性方程）
2. Momentum balance for ideal fluid（理想流体动量平衡）
3. Momentum balance for real fluid（实际流体动量平衡）

Section 5 包括：

1. 对恒定、无旋、不可压缩、只受重力作用的理想流体积分。
2. 对恒定、不可压缩、只受重力作用的理想流体沿流线积分。

## 2. 连续性方程

### 2.1 物理意义

Continuity equation（连续性方程）表达质量守恒。

对控制微元而言：

> 单位时间内流出质量大于流入质量的差值，等于微元内质量随时间减少的速率。

也就是说：

$$
\text{mass loss by outflow-inflow}
=
\text{mass loss due to density decrease in time}
$$

### 2.2 一般形式

三维流动的一般连续性方程为：

$$
\frac{\partial \rho}{\partial t}
+\frac{\partial(\rho u_x)}{\partial x}
+\frac{\partial(\rho u_y)}{\partial y}
+\frac{\partial(\rho u_z)}{\partial z}
=0
$$

向量形式：

$$
\frac{\partial \rho}{\partial t}
+\nabla\cdot(\rho\vec u)=0
$$

其中：

- $\rho$：密度。
- $\vec u=(u_x,u_y,u_z)$：速度矢量。

### 2.3 恒定可压缩流

若流动为 steady flow（恒定流），则：

$$
\frac{\partial \rho}{\partial t}=0
$$

连续性方程变为：

$$
\frac{\partial(\rho u_x)}{\partial x}
+\frac{\partial(\rho u_y)}{\partial y}
+\frac{\partial(\rho u_z)}{\partial z}
=0
$$

即：

$$
\nabla\cdot(\rho\vec u)=0
$$

### 2.4 不可压缩流

若流体不可压缩：

$$
\rho=const
$$

连续性方程化为：

$$
\frac{\partial u_x}{\partial x}
+\frac{\partial u_y}{\partial y}
+\frac{\partial u_z}{\partial z}
=0
$$

向量形式：

$$
\nabla\cdot\vec u=0
$$

这表示不可压缩流的速度场必须无散。

## 3. 连续性方程例题

### 3.1 例题 1：二维速度场是否有意义

设二维流动，$\rho=const$。

#### 情况 1

$$
u_x=-2y,\quad u_y=3x
$$

不可压缩连续性方程：

$$
\frac{\partial u_x}{\partial x}
+\frac{\partial u_y}{\partial y}
=0
$$

计算：

$$
\frac{\partial(-2y)}{\partial x}=0
$$

$$
\frac{\partial(3x)}{\partial y}=0
$$

因此：

$$
0+0=0
$$

满足不可压缩连续性方程，该速度场有意义。

#### 情况 2

$$
u_x=0,\quad u_y=3xy
$$

计算：

$$
\frac{\partial u_x}{\partial x}=0
$$

$$
\frac{\partial u_y}{\partial y}=3x
$$

因此：

$$
0+3x\ne 0
$$

不满足不可压缩连续性方程。若同时给定 $\rho=const$，则该速度场对不可压缩流没有物理意义。

### 3.2 例题 2：修正速度分量满足连续性

给定：

$$
u_x=t,\quad u_y=3xy,\quad u_z=xz,\quad \rho=t
$$

课件判断该流动不满足连续性方程，因此没有物理意义。

若保持 $u_x$、$u_y$、$\rho$ 不变，需要修改 $u_z$，使其满足：

$$
\frac{\partial \rho}{\partial t}
+\frac{\partial(\rho u_x)}{\partial x}
+\frac{\partial(\rho u_y)}{\partial y}
+\frac{\partial(\rho u_z)}{\partial z}
=0
$$

由课件推得：

$$
\frac{\partial u_z}{\partial z}=-(1+3x)
$$

积分：

$$
u_z=-(1+3x)z+f(x,y)
$$

若取 $f(x,y)=0$，则：

$$
u_z=-(1+3x)z
$$

这类题的关键是：把未知速度分量代入连续性方程，再对相应坐标积分。

## 4. 理想流体动量方程：Euler Equations

### 4.1 理想流体受力特点

Ideal fluid（理想流体）无黏性，因此表面力只有压强，没有黏性剪切应力。

对微元体列 Newton 第二定律：

$$
\sum F=ma
$$

即可得到理想流体的运动微分方程。

### 4.2 分量形式

Euler equations of motion（欧拉运动方程）为：

$$
f_x-\frac{1}{\rho}\frac{\partial p}{\partial x}
=\frac{du_x}{dt}
$$

$$
f_y-\frac{1}{\rho}\frac{\partial p}{\partial y}
=\frac{du_y}{dt}
$$

$$
f_z-\frac{1}{\rho}\frac{\partial p}{\partial z}
=\frac{du_z}{dt}
$$

其中：

$$
\frac{du_x}{dt}
=
\frac{\partial u_x}{\partial t}
+u_x\frac{\partial u_x}{\partial x}
+u_y\frac{\partial u_x}{\partial y}
+u_z\frac{\partial u_x}{\partial z}
$$

类似地可写出 $y$、$z$ 分量。

### 4.3 向量形式

理想流体一般动量平衡可写为：

$$
\vec f-\frac{1}{\rho}\nabla p
=
\frac{\partial \vec u}{\partial t}
+(\vec u\cdot\nabla)\vec u
$$

右侧即 Euler acceleration。

### 4.4 与静力平衡方程的关系

若流体加速度为零：

$$
\frac{du_x}{dt}
=\frac{du_y}{dt}
=\frac{du_z}{dt}=0
$$

Euler 方程退化为静止流体平衡方程：

$$
f_x-\frac{1}{\rho}\frac{\partial p}{\partial x}=0
$$

$$
f_y-\frac{1}{\rho}\frac{\partial p}{\partial y}=0
$$

$$
f_z-\frac{1}{\rho}\frac{\partial p}{\partial z}=0
$$

## 5. 实际流体动量方程

### 5.1 实际流体特点

Real fluid（实际流体）与 ideal fluid 的主要区别是：

1. 实际流体有黏性。
2. 实际流体中存在剪切应力。
3. 由于黏性应力存在，压应力不再严格各向同性。

即可能有：

$$
p_{xx}\ne p_{yy}\ne p_{zz}
$$

对不可压缩流，平均压强可写为：

$$
p=\frac{1}{3}(p_{xx}+p_{yy}+p_{zz})
$$

### 5.2 广义牛顿应力关系

实际流体表面力包括：

- compressive stress（压应力）
- shear stress（剪切应力）

剪切应力可由广义牛顿内摩擦公式描述，例如：

$$
\tau_{xy}
=\mu
\left(
\frac{\partial u_x}{\partial y}
+\frac{\partial u_y}{\partial x}
\right)
$$

$$
\tau_{yz}
=\mu
\left(
\frac{\partial u_y}{\partial z}
+\frac{\partial u_z}{\partial y}
\right)
$$

$$
\tau_{zx}
=\mu
\left(
\frac{\partial u_z}{\partial x}
+\frac{\partial u_x}{\partial z}
\right)
$$

### 5.3 Navier-Stokes Equations

对不可压缩实际流体，可得到 incompressible Navier-Stokes equations：

$$
\vec f-\frac{1}{\rho}\nabla p+\nu\nabla^2\vec u
=
\frac{\partial\vec u}{\partial t}
+(\vec u\cdot\nabla)\vec u
$$

其中：

- $\nu=\mu/\rho$：运动黏度。
- $\nabla^2\vec u$：速度的 Laplacian，表示黏性扩散项。

分量形式为：

$$
f_x-\frac{1}{\rho}\frac{\partial p}{\partial x}
+\nu\nabla^2u_x
=\frac{du_x}{dt}
$$

$$
f_y-\frac{1}{\rho}\frac{\partial p}{\partial y}
+\nu\nabla^2u_y
=\frac{du_y}{dt}
$$

$$
f_z-\frac{1}{\rho}\frac{\partial p}{\partial z}
+\nu\nabla^2u_z
=\frac{du_z}{dt}
$$

同时满足不可压缩连续性方程：

$$
\frac{\partial u_x}{\partial x}
+\frac{\partial u_y}{\partial y}
+\frac{\partial u_z}{\partial z}
=0
$$

### 5.4 理想流体与实际流体方程的关系

实际流体方程比理想流体 Euler 方程多了由黏性剪切应力引起的项。

对不可压缩 Newtonian fluid，这些黏性项体现为：

$$
\nu\nabla^2\vec u
$$

若忽略黏性：

$$
\nu=0
$$

Navier-Stokes 方程退化为 Euler 方程。

## 6. Euler 方程积分

### 6.1 一般情况下不能直接积分

Euler equations 在一般情况下不能直接积分。只有在特定条件下，才能得到简单的 Bernoulli 形式。

本课件讨论两种情况：

1. 恒定、无旋、不可压缩、只受重力作用的理想流体。
2. 恒定、不可压缩、只受重力作用的理想流体沿同一流线积分。

## 7. 势流中的 Bernoulli 方程

### 7.1 适用条件

第一种积分适用于：

- steady flow（恒定流）
- incompressible fluid（不可压缩流体）
- ideal fluid（理想流体）
- only gravity as mass force（质量力只有重力）
- potential flow / irrotational flow（势流 / 无旋流）

### 7.2 推导关键

从 Euler 方程出发，分别乘以 $dx$、$dy$、$dz$ 后相加。

若只受重力：

$$
f_x=0,\quad f_y=0,\quad f_z=-g
$$

重力项给出：

$$
-gdz
$$

不可压缩条件下：

$$
\frac{1}{\rho}dp=d\left(\frac{p}{\rho}\right)
$$

无旋条件使动能项可写为：

$$
d\left(\frac{u^2}{2}\right)
$$

最终得到：

$$
gdz+\frac{1}{\rho}dp+d\left(\frac{u^2}{2}\right)=0
$$

积分：

$$
gz+\frac{p}{\rho}+\frac{u^2}{2}=C
$$

除以 $g$：

$$
z+\frac{p}{\rho g}+\frac{u^2}{2g}=C
$$

这就是 Bernoulli equation 的水头形式。

### 7.3 两点形式

对于同一势流场中任意两点：

$$
z_1+\frac{p_1}{\rho g}+\frac{u_1^2}{2g}
=
z_2+\frac{p_2}{\rho g}+\frac{u_2^2}{2g}
$$

在势流条件下，常数 $C$ 对整个流场相同。

## 8. Bernoulli 方程的意义

### 8.1 物理意义

Bernoulli 方程可写为：

$$
gz+\frac{p}{\rho}+\frac{u^2}{2}=C
$$

表示单位质量流体的机械能守恒。

若写为：

$$
z+\frac{p}{\rho g}+\frac{u^2}{2g}=C
$$

则表示单位重量流体的总机械能守恒。

### 8.2 几何意义

各项水头含义如下：

| 项 | 名称 | 几何意义 | 物理意义 |
| --- | --- | --- | --- |
| $z$ | elevation head | 位置水头 | 单位重量势能 |
| $\frac{p}{\rho g}$ | pressure head | 压强水头 | 单位重量压能 |
| $\frac{u^2}{2g}$ | velocity head / flow head | 流速水头 | 单位重量动能 |
| $z+\frac{p}{\rho g}$ | hydraulic head | 水力水头 | 单位重量总势能 |
| $z+\frac{p}{\rho g}+\frac{u^2}{2g}$ | total head | 总水头 | 单位重量总机械能 |

### 8.3 总能量守恒

对于恒定、不可压缩、无旋、只受重力作用的理想流体：

$$
\frac{p}{\rho g}+z+\frac{u^2}{2g}=C
$$

表示流场中每一点单位重量流体的总能量相同。

## 9. 沿流线积分的 Bernoulli 方程

### 9.1 适用条件

第二种积分适用于：

- steady flow（恒定流）
- incompressible fluid（不可压缩流体）
- ideal fluid（理想流体）
- only gravity（只受重力）
- 沿同一 streamline（同一流线）

与势流积分不同，它不要求整个流场无旋。

### 9.2 沿流线积分结果

沿同一流线有：

$$
z+\frac{p}{\rho g}+\frac{u^2}{2g}=C
$$

或两点形式：

$$
z_1+\frac{p_1}{\rho g}+\frac{u_1^2}{2g}
=
z_2+\frac{p_2}{\rho g}+\frac{u_2^2}{2g}
$$

### 9.3 常数的含义

沿流线积分时：

- 同一流线上的 $C$ 相同。
- 对有旋流，不同流线的 $C$ 可以不同。

### 9.4 与势流 Bernoulli 方程的区别

两种 Bernoulli 方程数学形式完全相同，但适用范围不同。

| 类型 | 适用范围 | 常数 $C$ |
| --- | --- | --- |
| 势流积分 | 恒定、不可压缩、无旋、理想流体，只受重力 | 整个流场相同 |
| 沿流线积分 | 恒定、不可压缩、理想流体，只受重力 | 同一流线相同，不同流线可不同 |

对于 rotational flow（有旋流），不能把 Bernoulli 常数推广到整个流场，只能沿同一流线使用。

## 10. 常见问答整理

### 10.1 实际流体相比理想流体有什么特点？

实际流体具有黏性，会产生剪切应力。

因此，实际流体运动方程比理想流体 Euler 方程多出黏性应力项。对于不可压缩 Newtonian fluid，这些项表现为：

$$
\nu\nabla^2\vec u
$$

### 10.2 连续性方程有哪些形式？

常见形式包括：

#### 一般形式

$$
\frac{\partial \rho}{\partial t}
+\nabla\cdot(\rho\vec u)=0
$$

#### 恒定可压缩流

$$
\nabla\cdot(\rho\vec u)=0
$$

#### 不可压缩流

$$
\nabla\cdot\vec u=0
$$

### 10.3 不可压缩连续性方程表达什么？

它表达不可压缩流体的质量守恒。由于密度为常数，质量守恒转化为速度场无散：

$$
\frac{\partial u_x}{\partial x}
+\frac{\partial u_y}{\partial y}
+\frac{\partial u_z}{\partial z}
=0
$$

### 10.4 势流 Bernoulli 方程和沿流线 Bernoulli 方程有何不同？

数学表达式相同：

$$
z+\frac{p}{\rho g}+\frac{u^2}{2g}=C
$$

但意义不同：

- 势流积分：适用于整个恒定、不可压缩、无旋理想流体场，任意两点可用同一常数。
- 沿流线积分：适用于恒定、不可压缩理想流体中同一流线上的点；对于有旋流，不同流线常数可不同。

## 11. 本讲小结

本讲建立了流体运动基本方程及 Bernoulli 方程的基础。

核心内容包括：

- 连续性方程来自质量守恒：

$$
\frac{\partial \rho}{\partial t}
+\nabla\cdot(\rho\vec u)=0
$$

- 不可压缩流体满足：

$$
\nabla\cdot\vec u=0
$$

- 理想流体运动方程为 Euler equations：

$$
\vec f-\frac{1}{\rho}\nabla p
=
\frac{\partial \vec u}{\partial t}
+(\vec u\cdot\nabla)\vec u
$$

- 实际不可压缩流体满足 Navier-Stokes equations：

$$
\vec f-\frac{1}{\rho}\nabla p+\nu\nabla^2\vec u
=
\frac{\partial \vec u}{\partial t}
+(\vec u\cdot\nabla)\vec u
$$

- 在特定条件下，Euler 方程可积分得到 Bernoulli equation：

$$
z+\frac{p}{\rho g}+\frac{u^2}{2g}=C
$$

- 势流中 Bernoulli 常数可用于整个流场；有旋流中一般只能沿同一流线使用。

## 12. 关键词对照

| English | 中文 |
| --- | --- |
| Continuity equation | 连续性方程 |
| Mass conservation | 质量守恒 |
| Compressible flow | 可压缩流 |
| Incompressible flow | 不可压缩流 |
| Divergence | 散度 |
| Momentum balance | 动量平衡 |
| Ideal fluid | 理想流体 |
| Real fluid | 实际流体 |
| Euler equations of motion | 欧拉运动方程 |
| Navier-Stokes equations | 纳维-斯托克斯方程 |
| Viscous stress | 黏性应力 |
| Shear stress | 剪切应力 |
| Compressive stress | 压应力 |
| Laplacian | 拉普拉斯算子 |
| Potential flow | 势流 |
| Irrotational flow | 无旋流 |
| Rotational flow | 有旋流 |
| Bernoulli equation | 伯努利方程 |
| Elevation head | 位置水头 |
| Pressure head | 压强水头 |
| Velocity head | 流速水头 |
| Hydraulic head | 水力水头 |
| Total head | 总水头 |
