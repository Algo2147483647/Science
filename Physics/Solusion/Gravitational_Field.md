

## Two-body gravitational motion

一个质点并作为原点静止时, 另一个质点的轨迹方程如下所述。其中, 圆锥曲线的极坐标方程, $e$离心率, $p$半通径.
$$
\begin{align*}
  r &= \frac{p}{1 - e \sin(θ + θ_0)}  \\
  p &= \frac{L^2}{G M m^2}  \\
  e &= \sqrt{1 + 2 \frac{E}{m} \left(\frac{L}{G M m}\right)^2}
\end{align*}
$$
二体场景在惯性系中可以抽象为绕等效质心运动。

- Proof

  - 建立方程组。其中$L, E$是常量. $r, θ, v_r, v_θ$是变量. 3个方程4个变量.求出 $r-θ$ 关系式.
    $$
    \begin{align*}
      L &= m r v_θ  \tag{角动量守恒}  \\
      E &= \frac{1}{2} m (v_r^2 + v_θ^2) - G \frac{M m}{r}  \tag{能量守恒}  \\
      \frac{\mathrm d r}{\mathrm d θ} &= r \frac{v_r}{v_θ}  \tag{$v_r = \frac{\mathrm d r}{\mathrm d t}, v_θ = r \frac{\mathrm d θ}{\mathrm d t}$}
    \end{align*}
    $$
    
  - 解方程组
    $$
    \begin{align*}
      v_θ &= \frac{L}{m r}  \tag{独立$v_θ$}  \\
      v_r &= \sqrt{\frac{2 E}{m} + \frac{2 G M}{r} -\left(\frac{L}{m}\right)^2 \frac{1}{r^2}}  \tag{独立$v_r$}
    \end{align*}
    $$
    $$
    \begin{align*}
      \Rightarrow\quad  \frac{\mathrm d r}{\mathrm d θ} &= r \frac{v_r}{v_θ}  \\
        &= r \frac{m r \sqrt{\frac{2 E}{m} + \frac{2 G M}{r} - \left(\frac{L}{m}\right)^2 \frac{1}{r^2}}}{L}  \tag{代入}
    \end{align*}
    $$

    $$
    \begin{align*}
    \Rightarrow\quad  \int \frac{\mathrm d r}{r^2 \sqrt{\frac{2 E}{m} + \frac{2 G M}{r} - \left(\frac{L}{m}\right)^2 \frac{1}{r^2}}} &= \int \frac{m}{L} \mathrm d θ  \tag{两边独立$r,θ$,并积分}  \\
    \Rightarrow\quad  - \int \frac{\mathrm d \left(\frac{1}{r}\right)}{\sqrt{\frac{2 E}{m} + 2 G M \frac{1}{r} - (\frac{L}{m})^2 \frac{1}{r^2}}} &= \frac{m}{L} θ + C_θ  \tag{换元}  \\
    \Rightarrow\quad  - \left(\frac{m}{L} \arcsin \frac{\left(\frac{L}{m}\right)^2 \frac{1}{r} - G M}{\sqrt{G^2 M^2 + \frac{2 E}{m} \left(\frac{L}{m}\right)^2 }} + C_r\right) &= \frac{m}{L} θ + C_θ  \tag{积分公式$\int \frac{\mathrm d x}{\sqrt{c+b x-a x^2}} = \frac{1}{\sqrt{a}} \arcsin \frac{2 a x-b}{\sqrt{b^2 + 4 a c}} + C$}  \\
    \Rightarrow\quad  - \left(\frac{1}{L_0} \arcsin \frac{L_0^2 \frac{1}{r} - G M}{\sqrt{G^2 M^2 + 2 E_0 L_0^2 }} + C_r\right) &= \frac{1}{L_0} θ + C_θ  \tag{$L_0 = \frac{L}{m}, E_0 = \frac{E}{m}$}
    \end{align*}
    $$

    $$
    \begin{align*}
      \Rightarrow\quad  r &= \frac{L_0^2}{\sqrt{G^2 M^2 + 2 E_0 L_0^2 } \sin(-θ + θ_0) + G M}  \\
      \Rightarrow\quad  r &= \frac{L_{00}^2 G M}{1 + \sqrt{1 + 2 E_0 L_{00}^2 } \sin(-θ + θ_0)}  \tag{$L_{00} = \frac{L_0}{G M} = \frac{L}{G M m}$}
    \end{align*}
    $$