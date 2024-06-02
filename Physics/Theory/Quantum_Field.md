# Quantum Field

[TOC]

## Wave function

### Schrödinger equation

**时间依赖的薛定谔方程**：
$$
i\hbar \frac{\partial}{\partial t} \psi(\mathbf{r}, t) = \hat{H} \psi(\mathbf{r}, t)
$$
其中，$\psi(\mathbf{r}, t)$是波函数，$\hbar$是约化普朗克常数，$\hat{H}$是哈密顿算符。

**时间独立的薛定谔方程**：
$$
\hat{H} \psi(\mathbf{r}) = E \psi(\mathbf{r})
$$
Schrödinger equation其中，$E$是能量本征值。
$$
\nabla^{2} \psi-\frac{8 \pi^{2}}{h^{2}} V \psi \mp \frac{4 \pi i}{h} \frac{\partial \psi}{\partial t}=0
$$

定态薛定谔方程
$$
\nabla^2 \psi + \frac{8 \pi^2}{h^2} (E-V) \psi = 0
$$

**玻恩规则**
$$
\mathbb P = |\psi(x)|^2\\
\int|\psi(x)|^2 d^3 r= 1
$$


算符对易关系
$$
[\hat x, \hat y] = x y - yx = i \hbar
$$
**测量中的期望值**
$$
\langle\hat{A}\rangle=\int \psi^{*}(\mathbf{r}, t) \hat{A} \psi(\mathbf{r}, t) d^{3} r
$$
## Uncertainty Principle

描述了两个共轭可观测量（如位置和动量，或能量和时间）之间的不确定性关系。一般形式的海森堡不确定性原理可以表示为：
$$
\Delta A \Delta B \geq \frac{1}{2} \left| \langle [\hat{A}, \hat{B}] \rangle \right|
$$

其中：

- $\Delta A$ 是可观测量 $A$ 的标准偏差（不确定性）。
- $\hat{A}$ 和 $\hat{B}$ 是对应的量子算符。
- $\langle [\hat{A}, \hat{B}] \rangle$ 是对易算符的期望值。

具体到位置和动量的情况，不确定性原理可以表示为：

$$
\Delta x \Delta p \geq \frac{\hbar}{2}
$$

### 狄拉克方程

狄拉克方程是一个关于四分量自旋量子的方程，可以写作：

$$
(i \gamma^\mu \partial_\mu - m) \psi = 0
$$

其中：
- $\psi$ 是狄拉克自旋量子，具有四个分量，表示粒子的波函数。
- $\gamma^\mu$ 是狄拉克矩阵，满足反对易关系 $\{ \gamma^\mu, \gamma^\nu \} = 2g^{\mu\nu}$，其中 $g^{\mu\nu}$ 是闵可夫斯基度规。
- $m$ 是粒子的质量。
- $\partial_\mu$ 是对时空坐标的偏导数。

狄拉克矩阵 $\gamma^\mu$ 是 4×4 矩阵，满足以下反对易关系：

$$
\{ \gamma^\mu, \gamma^\nu \} = \gamma^\mu \gamma^\nu + \gamma^\nu \gamma^\mu = 2g^{\mu\nu}I
$$

这些矩阵的一个常见表示是标准的狄拉克表示（Dirac-Pauli 表示）：

$$
\gamma^0 = \begin{pmatrix}
I & 0 \\
0 & -I
\end{pmatrix}, \quad
\gamma^i = \begin{pmatrix}
0 & \sigma^i \\
-\sigma^i & 0
\end{pmatrix}
$$
其中 $I$ 是 2×2 单位矩阵，$\sigma^i$ 是泡利矩阵。

## 自旋


## Fermi-Dirac Distribution（用于描述费米子）：

$$
f(E) = \frac{1}{e^{(E - \mu) / k_B T} + 1}
$$
其中，$E$是能量，$\mu$是化学势，$k_B$是玻尔兹曼常数，$T$是温度。

## Bose-Einstein Distribution（用于描述玻色子）：

$$
n(\epsilon) = \frac{1}{e^{(\epsilon - \mu) / k_B T} - 1}
$$
其中，$\epsilon$是单粒子能量，$\mu$是化学势。



**路径积分表述（Path Integral Formulation）**（费曼路径积分）：
$$
\langle x_f, t_f | x_i, t_i \rangle = \int \mathcal{D}[x(t)] e^{\frac{i}{\hbar} S[x(t)]}
$$
其中，$S[x(t)]$是作用量。

## Yang-Mills theory

