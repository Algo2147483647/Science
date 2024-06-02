# Electromagnetic Field

[TOC]

## Concepts

Electromagnetic Field 通过电磁四维势 $A^i$ 来描述, $\varphi, \boldsymbol A$ 分别是电势和磁矢势.
$$
A^i = \left(\begin{matrix}\varphi \\ \boldsymbol A \end{matrix}\right)
$$

此外，磁场的矢量势和电场的标量势与电场和磁场之间的可观测量$\boldsymbol E, \boldsymbol B$关系为：

$$
\begin{align*}
\mathbf{B} &= \nabla \times \mathbf{A}\\
\mathbf{E} &= -\grad \Phi - \frac{\partial \mathbf{A}}{\partial t}
\end{align*}
$$

## The action of an Electromagnetic field

粒子的动能和静能的总和 + 粒子与电磁场相互作用的项 + 电磁场自身的作用量
$$
S = \sum\int mc \mathrm ds - \sum \int \frac{e}{c} A_k \mathrm dx^k - \frac{1}{16 \pi c} \int F_{ik}F^{ik} \mathrm d \Omega
$$

### The action of a charged particle moving in an electromagnetic field

The action of a charged particle moving in an electromagnetic field, 描述粒子的自由运动 + 粒子与电磁场的相互作用.
$$
S = \int_a^b (-mc \mathrm{d} s - \frac{e}{c}A_i\mathrm{d}x^i)
$$

**Lagrangian**
$$
\begin{align*}
L &= -mc^2\sqrt{1 - \frac{v^2}{c^2}} + \frac{e}{c}A\cdot v - e \varphi\\
P &= \frac{mv}{\sqrt{1 - \frac{v^2}{c^2}}}+\frac{e}{c}A\\
H &= \sqrt{m^2c^4 + c^2 (P-\frac{e}{c}A)^2}+e\varphi
\end{align*}
$$

### Equation of motion

描述了带电粒子在电磁场中的运动，是经典电动力学中的洛伦兹力公式在四维时空中的表示形式。电磁场张量 $F^{ik}$ 对粒子的四维速度 $u_k$ 作用，产生了加速度（即四维速度的变化率），其结果乘以电荷 $e$ 和光速 $c$，等于粒子的质量 $m$ 和光速 $c$ 乘以四维速度的变化率。
$$
m c \frac{\mathrm{d} u^i}{\mathrm{d} s} = \frac{e}{c} F^{ik} u_k \\
F^{ik} = \frac{\partial A_k}{\partial x^i}-\frac{\partial A_i}{\partial x^k}=\left(\begin{matrix} 0 & -E_x & -E_y & -E_z \\ E_x & 0 & -H_z & H_y \\ E_y & H_z & 0 & -H_x \\ E_z & -H_y  & H_x & 0 \end{matrix}\right)
$$

- **$\frac{\mathrm{d} u^i}{\mathrm{d} s}$**: 这是粒子的四维速度 $u^i$ 对粒子固有时间 $s$ 的导数。四维速度 $u^i$ 定义为：
  $$u^i = \frac{\mathrm{d} x^i}{\mathrm{d} s}$$
  其中 $x^i$ 是粒子的四维时空坐标。
- **$F^{ik}$**: 电磁场张量，它包含了电场和磁场的信息。
- **$u_k$**: 粒子的四维速度的共变分量（下标形式）。

三维形式:
$$
\frac{\mathrm{d} \boldsymbol p}{\mathrm{d} t} = e \boldsymbol E + \frac{e}{c} \boldsymbol v \times \boldsymbol H \\
\frac{\mathrm{d} \mathrm E_{kin}}{\mathrm{d} t} = e \boldsymbol E \cdot \boldsymbol v
$$

- Proof
  最小作用量原理, 
  $$
  \begin{align*}
  δ S &= 0\\
  δ\int_a^b (-mc \mathrm{d} s - \frac{e}{c}A_i\mathrm{d}x^i) &= 0\\
  δ\int_a^b (mc \sqrt{\mathrm{d} x_i\mathrm{d} x^i} + \frac{e}{c}A_i\mathrm{d}x^i) &= 0   \tag{$\mathrm{d} s = \sqrt{\mathrm{d} x_i\mathrm{d} x^i}$}\\
  \int_a^b (mc \frac{\mathrm{d} x_i\mathrm{d} δ x^i}{\mathrm{d} s} + \frac{e}{c}(A_iδ\mathrm{d}x^i + δA_i\mathrm{d}x^i)) &= 0\\
  \int_a^b \left(mc u_i \mathrm{d} δ x^i + \frac{e}{c}(A_iδ\mathrm{d}x^i + δA_i\mathrm{d}x^i)\right) &= 0 \tag{$u_i = \frac{\mathrm{d} x_i}{\mathrm{d} s}$}\\
  (mc u_i+\frac{e}{c}A_i)δ x^i - \int \left(mc \mathrm{d} u_i  δ x^i + \frac{e}{c}(\mathrm{d}A_iδx^i -  δA_i\mathrm{d}x^i) \right) &= 0 \tag{$\int u \mathrm{d} v = uv - \int v \mathrm{d} u$}\\
  \end{align*}
  $$
  
  因为$(mc u_i + \frac{e}{c}A_i)  δ x^i = 0$
  $$
  δA_i = \frac{\partial A_i}{\partial x^k} δ x^k\\
  \mathrm{d}A_i = \frac{\partial A_i}{\partial x^k} \mathrm{d}x^k\\
  $$
  
  $$
  \begin{align*}
  \Rightarrow\quad \int \left(mc \mathrm{d} u_i - \frac{e}{c}\mathrm{d}x^k(\frac{\partial A_k}{\partial x^i}-\frac{\partial A_i}{\partial x^k}) \right)δ x^i &= 0 \\
  \end{align*}
  $$
  
  因为$δ x^i$ 任意, 所以被积函数为零
  $$
  \begin{align*}
  \Rightarrow\quad mc \mathrm{d} u_i&=\frac{e}{c}\mathrm{d}x^k(\frac{\partial A_k}{\partial x^i}-\frac{\partial A_i}{\partial x^k}) \\
  mc \mathrm{d} u_i&=\frac{e}{c}\mathrm{d}x^kF_{ik} \tag{$F_{ik} = (\frac{\partial A_k}{\partial x^i}-\frac{\partial A_i}{\partial x^k})$}\\
  mc \mathrm{d} \frac{\mathrm{d}u_i}{\mathrm{d}s}&=\frac{e}{c}u_kF_{ik}\\
  \end{align*}
  $$
  Q.E.D.



## Reference frame transformation of Electromagnetic Field

$$
E= E+ \frac{1}{c}H'\times V\\
H = H' - \frac{1}{c}E'\times V\\
$$



## d'Alembert's equations

$$
\begin{align}
\nabla^2 \mathbf{A} - \frac{1}{c^2} \frac{\partial \mathbf{A}}{\partial t^2} &= - \mu_0 \mathbf{J} \\
\nabla^2 \Phi - \frac{1}{c^2} \frac{\partial^2 \Phi}{\partial t^2} &= -\frac{\rho}{\varepsilon_0}
\end{align}
$$


## Maxwell’s equations

$$
\partial _\mu F^{\mu\nu}=\frac{4\pi}{c}J^{\nu}\\
\partial _\mu \bar F^{\mu\nu}=0
$$


$$
\begin{align}
\nabla \cdot \mathbf{E} &= \frac{\rho}{\varepsilon_0}\\
\nabla \cdot \mathbf{B} &= 0 \\
\nabla \times \mathbf{E} + \frac{\partial \mathbf{B}}{\partial t}&= 0\\
\nabla \times \mathbf{B} - \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t}&=  \mu_0 \mathbf{J} 
\end{align}
$$
