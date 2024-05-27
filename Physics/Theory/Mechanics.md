# Mechanics

[TOC]

## Generalized coordinates & Generalized velocity

define
$$
L(q_1,q_2, ... ,q_s,\dot q_1,\dot q_2, ... ,\dot q_s,t)
$$
每一个力学系统可以用一个确定的Lagrange函数表征.

## Principle of least action

$$
\begin{align*}
  S &= \int_{t_1}^{t_2} L(q,\dot q,t) \mathrm d t  \\
  δ S &= 0
\end{align*}
$$

$$
\begin{align*}
  δ S &= δ \int_{t_1}^{t_2} L(q,\dot q,t)\mathrm d t   \\
    &= \int_{t_1}^{t_2} (\frac{∂ L}{∂ q}δ q + \frac{∂ L}{∂ \dot q}δ \dot q) \mathrm d t   \\
    &= \frac{∂ L}{∂ \dot q} δ q |_{t_1}^{t_2} + \int_{t_1}^{t_2} (\frac{∂ L}{∂ q} - \frac{d}{dt} \frac{∂ L}{∂ \dot q}) δ q \mathrm d t = 0
\end{align*}
$$
系统在两个时刻的, 位置之间的运动, 使得Lagrange函数积分(作用量S)取最小值.
least action principle
$$
\delta S=\delta \int^{t_{2}}_{t_1} L(q, \dot{q}, t) \mathrm{d} t=0
$$

## Equations of motion

$$
\frac{d}{dt} \frac{∂ L}{∂ \dot q_i} - \frac{∂ L}{∂ q_i} = 0 \quad   (i=1,\dots,s)
$$

## 不变性

### 能量守恒 -- 时间均匀性

- Theorem
  时间均匀性: 封闭系统Lagrange函数不显含时间. 

  $$
  \Rightarrow L(\boldsymbol q,\dot {\boldsymbol q})
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
  - Define
    $$E = \sum \dot q_i \frac{∂ L}{∂ \dot q_i} - L  = T(q,\dot q) + U(q) = const.$$

### 动量守恒 -- 空间均匀性

- Theorem
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

  - Define
    $$
    \Rightarrow \boldsymbol P = \sum \frac{∂ L}{∂ \boldsymbol v_i} = \sum m_i \boldsymbol v_i = const.
    $$

### 角动量守恒 -- 空间各向同性

- Theorem
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

  - Define
    $$
    \Rightarrow \boldsymbol M = \sum \boldsymbol r_i × \boldsymbol P_i = const.
    $$


Lagrangian equation
$$
\frac{\mathrm d}{\mathrm d t} \frac{\partial L}{\partial \dot q} - \frac{\partial L}{\partial q} = 0
$$
Hamiltonian function
$$
H(p,q,t) = \sum_i p_i \dot q_i - L
$$
poisson bracket
$$
\{H, f\}=\sum_{k}\left(\frac{\partial H}{\partial p_{k}} \frac{\partial f}{\partial q_{k}}-\frac{\partial H}{\partial q_{k}} \frac{\partial f}{\partial p_{k}}\right)
$$