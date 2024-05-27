# Fluid

[TOC]

## Ideal Fluid

不可压缩、不计粘性的流体.

- 给定5个量:速度$(v_x, v_y, v_z)$,压强$p$,密度$ρ$,可完全确定运动流体的状态.


### Mass Conservation

$$
\begin{align*}
  \oint ρ \boldsymbol v · d \boldsymbol f &= -\frac{∂}{∂ t}\int ρ dV   \\
  \Rightarrow\quad  \int ∇ · (ρ \boldsymbol v) dV  &= -\frac{∂}{∂ t}\int ρ dV  \\
  \Rightarrow\quad  \int \left(∇ · (ρ \boldsymbol v) + \frac{∂ ρ}{∂ t} \right) dV  &= 0  
\end{align*}
$$
区域体流出质量 = 区域封闭面流出质量.

### Continuity equation

$$
∇ · (ρ \boldsymbol v) + \frac{∂ ρ}{∂ t} = 0
$$
质量流流出速率 = 流体密度减少速率.

- 质量流密度 $\boldsymbol j = ρ \boldsymbol v$

### Equation of motion

$$
\begin{align*}
  -\oint p d \boldsymbol f &= -\int ∇ p\ dV  \\
  ρ \frac{d \boldsymbol v}{t} &= -∇ p
\end{align*}
$$

### Eular Ideal fluid equation

$$
\begin{align*}
  \frac{∂ \boldsymbol v}{∂ t} + (\boldsymbol v · ∇)\boldsymbol v &= - \frac{1}{ρ} ∇ p  \\
  \frac{∂ \boldsymbol v}{∂ t} + (\boldsymbol v · ∇)\boldsymbol v &= - \frac{1}{ρ}·∇ p + \boldsymbol g  \tag{重力场$\boldsymbol g$下}
\end{align*}
$$

$- ∇ p$: 单位体积流体上的作用力.

- Proof
  $$
  \begin{align*}
    ρ \frac{\mathrm d \boldsymbol v}{\mathrm d t} &=  - ∇ p + ρ \boldsymbol g  \tag{微元运动方程}  \\
    \mathrm d \boldsymbol v &= \frac{∂ \boldsymbol v}{∂t} \mathrm d t + (\mathrm d \boldsymbol r · ∇) \boldsymbol v    \tag{全导数}  \\
    \Rightarrow\quad \frac{\mathrm d \boldsymbol v}{\mathrm d t} &= \frac{∂ \boldsymbol v}{∂t} + (\boldsymbol v · ∇) \boldsymbol v  \tag{除以$\mathrm d t$}  \\
    \Rightarrow\quad \frac{∂ \boldsymbol v}{∂t} + (\boldsymbol v · ∇) \boldsymbol v &= - \frac{1}{ρ} ∇ p + \boldsymbol g  \tag{代入}
  \end{align*}
  $$

## Stable fluid


流体所在区域任意一点的位置都不随时间变化的流体.

- 均匀向下重力场$\boldsymbol g = g \hat{\boldsymbol z}$中的静止流体.
  $$
  \begin{align*}
    ∇ p &= ρ \boldsymbol g  \\
    \Rightarrow\quad p &= -ρ g z + const.  \tag{$\boldsymbol g = g \hat{\boldsymbol z}$, 积分}  \\
    \Rightarrow\quad p &= -ρ g h + p_0  \tag{距液面深度$h$, 大气压$p_0$}
  \end{align*}
  $$
- 质量极大的由于万有引力而结合在一起的一团流体 (如, 恒星).
  $$
  \begin{align*}
    Δ \varphi &= 4 π G ρ  \tag{引力势}  \\
    ∇ · \left(\frac{1}{ρ} ∇ p \right) &= -4 π G ρ
  \end{align*}
  $$

## Steady fluid


流体所在区域任意一点的速度都不随时间变化的流体. 

- Bernoulli equation
  $$
  \begin{align*}
    \frac{v^2}{2} + w &= const.  \\
    \frac{v^2}{2} + w + g z &= const.  \tag{重力场中}
  \end{align*}
  $$

## Viscous Fluid

### Navier Stokes Equations  
$$
ρ \left(\frac{∂\boldsymbol v}{∂t} + (\boldsymbol v · ∇) \boldsymbol v \right) =  - ∇ P  + ρ \boldsymbol f + η ∇^2 \boldsymbol v + \left(ζ + \frac{η}{3} \right) ∇ (∇ · \boldsymbol v)
$$

For dimension $d$, the component formula is 
$$
ρ \left(\frac{∂ v_x}{∂t} + \sum_{i=1}^{\dim} v_i \frac{∂ v_d}{∂x_i}\right) =  - \frac{∂ P}{∂d}  + ρ  f_d + η \sum_{i=1}^{\dim} \left(\frac{∂^2 v_d}{∂ x_i^2}\right) + \left(ζ + \frac{η}{3} \right) \frac{∂\left(\sum\limits_{i=1}^{\dim} \frac{∂ v_d}{∂x_i}\right)}{∂x_i}
$$

For incompressible fluid, we have $∇ ·\boldsymbol v ≡ 0$ and
$$
\frac{∂\boldsymbol v}{∂t} + (\boldsymbol v·∇) \boldsymbol v = -\frac{1}{ρ} ∇ P  + \boldsymbol f + \frac{η}{ρ} ∇^2 \boldsymbol v  \tag{$∇ ·\boldsymbol v ≡ 0$}
$$
- $η$: Viscosity
- $ρ$: Density
- Pressure: $∇ ·∇ P = ∇ ·v·ρ/ dt$

