# Mechanics

[TOC]

## Generalized coordinates & Generalized velocity

$$
(q,\dot q,t)
$$



## Principle of least action, Lagrangian

$$
\begin{align*}
  S &= \int_{t_1}^{t_2} L(q,\dot q,t) \mathrm d t  \\
  δ S &= 0
\end{align*}
$$

系统在两个时刻的, 位置之间的运动, 使得Lagrange函数积分(作用量S)取最小值.

每一个力学系统可以用一个确定的Lagrange函数表征.
$$
L(q_1,q_2, ... ,q_s,\dot q_1,\dot q_2, ... ,\dot q_s,t)
$$


## Equations of motion

Equations of motion (Lagrangian equation)
$$
\frac{\mathrm d}{\mathrm d t} \frac{\partial L}{\partial \dot q} - \frac{\partial L}{\partial q} = 0
$$

- Proof
  $$
  \begin{align*}
  δ S &= 0\\
  δ \int_{t_1}^{t_2} L(q,\dot q,t)\mathrm d t &= 0\\
  \int_{t_1}^{t_2} \left(\frac{∂ L}{∂ q}δ q + \frac{∂ L}{∂ \dot q}δ \dot q \right) \mathrm d t &= 0\\
  \frac{∂ L}{∂ \dot q} δ q |_{t_1}^{t_2} + \int_{t_1}^{t_2} \left(\frac{∂ L}{∂ q} - \frac{d}{dt} \frac{∂ L}{∂ \dot q}\right) δ q \mathrm d t  &= 0\\
  \frac{\mathrm d}{\mathrm d t} \frac{\partial L}{\partial \dot q} - \frac{\partial L}{\partial q} &= 0
  \end{align*}
  $$

## Invariance

### 能量守恒, 时间均匀性

时间均匀性: 封闭系统Lagrange函数不显含时间. 
$$
L(\boldsymbol q,\dot {\boldsymbol q})
$$

$$
\begin{align*}
  \frac{dL}{dt} 
  &= \sum \frac{∂ L}{∂ q_i} \dot q_i + \sum \frac{∂ L}{∂ \dot q_i} \ddot q_i   \\
  &= \sum \frac{d}{dt} \left(\frac{∂ L}{∂ \dot q_i}\dot q_i \right)  \\
  \Rightarrow \frac{d}{dt}\left(\sum \dot q_i \frac{∂ L}{∂ \dot q_i} - L \right) &= 0
\end{align*}
$$

封闭系统、定常外场系统,即当Lagrange函数不显含时间时,能量守恒成立.

* 能量
  $$
  E = \sum \dot q_i \frac{∂ L}{∂ \dot q_i} - L  = T(q,\dot q) + U(q) = const.
  $$

### 动量守恒, 空间均匀性

空间均匀性: 空间平移不变性.
$$
\begin{align*}
δ L &= \sum \frac{∂ L}{∂ \boldsymbol r_i}· δ \boldsymbol r_i   \\
&= \boldsymbol \epsilon · \sum \frac{∂ L}{∂ \boldsymbol r_i}  \\
&= 0\quad  (\forall \boldsymbol \epsilon)  \\
\Rightarrow \sum \frac{∂ L}{∂ \boldsymbol r_i} &= \sum \frac{d}{dt} \frac{∂ L}{∂ \boldsymbol v_i} = \frac{d}{dt} \sum \frac{∂ L}{∂ \boldsymbol v_i} = 0
\end{align*}
$$

* 动量

  $$
  \Rightarrow \boldsymbol P = \sum \frac{∂ L}{∂ \boldsymbol v_i} = \sum m_i \boldsymbol v_i = const.
  $$

### 角动量守恒, 空间各向同性

空间各向同性: 空间旋转不变性.
$$
\begin{align*}
  δ L 
  &= \sum (\frac{∂ L}{∂ \boldsymbol r_i} · δ \boldsymbol r_i + \frac{∂ L}{∂ \boldsymbol v_i} · δ \boldsymbol v_i)  \\
  &= \sum [\dot{\boldsymbol P_i} · (δ \boldsymbol \varphi × \boldsymbol r_i) + \boldsymbol P_i · ( δ \boldsymbol \varphi × \boldsymbol v_i )]  \\
  &= δ \boldsymbol \varphi · \sum (\boldsymbol r_i × \dot{\boldsymbol P_i} + \boldsymbol v_i × \boldsymbol P_i) \\
  &= δ \boldsymbol \varphi · \frac{d}{dt} \sum \boldsymbol r_i × \boldsymbol P_i   \\
  &= 0\quad  (\forall \boldsymbol \varphi) \Rightarrow \frac{d}{dt}\sum \boldsymbol r_i × \boldsymbol P_i   \\
  &= 0
\end{align*}
$$

* 角动量

  $$
  \Rightarrow \boldsymbol M = \sum \boldsymbol r_i × \boldsymbol P_i = const.
  $$

## 相空间

相空间：由 s 个广义坐标和 s 个广义动量构成的 2s 维空间。
$$
(q, p)
$$

## Hamiltonian function

Hamiltonian function, Hamiltonian equations

哈密顿方法的好处是, 在特定限制下, 使 Lagrange 方程降阶，能找到 2s 个一阶微分方程, 方便计算. 
$$
H(p,q,t) = \sum_i p_i \dot q_i - L\\
\dot q_i = \frac{\partial H}{\partial p_i}\\
\dot p_i = \frac{\partial H}{\partial q_i}\\
$$

### Poisson bracket

$$
\{f, g\}=\sum_{k}\left(\frac{\partial f}{\partial p_{k}} \frac{\partial g}{\partial q_{k}}-\frac{\partial f}{\partial q_{k}} \frac{\partial g}{\partial p_{k}}\right)\\
\frac{\mathrm{d}f}{\mathrm{d}t} = \frac{\partial f}{\partial t} + \{H, f\}
$$

- $\{f, g\} = -\{g, f\}, \{f, const.\} = 0$

### 莫培督原理

假设拉格朗日量不显含时间，因而哈密顿量不显含时间，因此系统的能量守恒, 最小作用量原理有更简单的形式
$$
H(p, q) = E = const.
$$

### 刘维尔定理

在相空间内, 具有相体积不变性
$$
\int \mathrm{d} \Gamma = const.
$$
