# Relativity

[TOC]

### Fundamental

**The relativity principle**: All natural laws are the same in all inertial reference frames.

**The propagation speed of interactions**: The maximum propagation speed of interaction is the same in all inertial reference frames (as can be derived from the principle of relativity). It can be proven that this speed is the speed of light in a vacuum.  (By taking the limit as $c\to \infty$, we can transition to classical mechanics.)
$$
c = 2.998 × 10^8 m/s
$$

- 时间是相对的, 不同参考系中时间的流逝速度不同. "两个不同事件之间有一定的事件间隔"这句话, 只有在指定哪一个参考系下才有意义, 因为在参考系$K_1$同时发生的两个事件, 在参考系$K_2$可能是不同时的.

### Minkowski Space

Minkowski spacetime is a four-dimensional manifold that combines three-dimensional Euclidean space and time. 
$$
(t, x, y, z)
$$

**Event**: 一个事件由其发生的位置和时间所描述$(t, x, y, z)$.

**Event interval**:
$$
\begin{align*}
  s_{12} &= (c^2 (t_2-t_1)^2 - (x_2-x_1)^2 - (y_2-y_1)^2 - (z_2-z_1)^2)^{1/2}  \\
  -d s &= (c^2 \mathrm d t^2 - \mathrm d x^2 - \mathrm d y^2 - \mathrm d z^2)^{1/2}
\end{align*}
$$

- 两个事件的间隔在任何惯性系下都一样. 这个不变性,就是光速不变的数学表示.        
- 类时间隔, 仅在时间上有变化的间隔, 故间隔为实数.
- 类空间隔, 仅在空间上有变化的间隔, 故间隔为虚数.

### Lorentz Transformation

$$
\begin{align*}
    \left(\begin{matrix} t' \\ x' \\ y' \\ z' \end{matrix}\right) &= \left(\begin{matrix} 
    -\frac{1}{\sqrt{1-(\frac{V}{c})^2}} & \frac{-\frac{V}{c^2}}{\sqrt{1-( \frac{V}{c} )^2}}  \\
    -\frac{-V}{\sqrt{1-( \frac{V}{c} )^2}} & \frac{1}{\sqrt{1-( \frac{V}{c} )^2}} \\
    & & 1\\ & & & 1 \end{matrix}\right)   \left(\begin{matrix} t \\ x \\ y \\ z \end{matrix}\right)
  \end{align*}
$$
  设两个惯性参考系 $K, K'$, 其中$K'$沿$x$轴以速度$V$相对于$K$作相对运动.

  - Proof
    - If the relative velocities of the new and old reference frames remain constant, then the reference frame transformation is a linear transformation
      $$\left(\begin{matrix} c t' \\ x' \\ y' \\ z' \end{matrix}\right) = \boldsymbol A   \left(\begin{matrix} c t \\ x \\ y \\ z \end{matrix}\right)$$

    - The principle of constant speed of light. The required reference frame transformation can ensure that all event intervals before and after the transformation remain unchanged in Minkowski spacetime.
      $$
      \begin{align*}
      Δs^2 &= c^2 Δt^2 - Δx^2 - Δy^2 - Δz^2 \\
          &= c^2 Δt'^2 - Δx'^2 - Δy'^2 - Δz'^2  \\
          &= const.
      \end{align*}
      $$
      化为矩阵式, 可解得 $\boldsymbol η = \boldsymbol A^T \boldsymbol η \boldsymbol A$.
      $$
      \begin{align*}
      \Rightarrow \quad &   \left(\begin{matrix} c Δt \\ Δx \\ Δy \\ Δz \end{matrix}\right)^T   \left(\begin{matrix} -1 \\ & 1\\ & & 1\\ & & & 1 \end{matrix}\right)   \left(\begin{matrix} c Δt \\ Δx \\ Δy \\ Δz \end{matrix}\right) =   \left(\begin{matrix} c Δt' \\ Δx' \\ Δy' \\ Δz' \end{matrix}\right)^T   \left(\begin{matrix} -1 \\ & 1\\ & & 1\\ & & & 1 \end{matrix}\right)   \left(\begin{matrix} c Δt' \\ Δx' \\ Δy' \\ Δz' \end{matrix}\right) = const.  \\
      \Rightarrow \quad & \boldsymbol p^T \boldsymbol η \boldsymbol p = \boldsymbol p'^T \boldsymbol η \boldsymbol p'  \tag{simplified form}  \\
          & \boldsymbol p^T \boldsymbol η \boldsymbol p = (\boldsymbol A \boldsymbol p)^T \boldsymbol η (\boldsymbol A \boldsymbol p)  \tag{substitution}  \\
          & \boldsymbol p^T \boldsymbol η \boldsymbol p = \boldsymbol p^T \boldsymbol A^T \boldsymbol η \boldsymbol A \boldsymbol p  \tag{transposition}  \\
      \Rightarrow \quad & \boldsymbol η = \boldsymbol A^T \boldsymbol η \boldsymbol A  \tag{Matrix calculation}
      \end{align*}
      $$

    - The only transformations that can satisfy the condition of constant event interval are translation and rotation Excluding familiar transformations such as translation, three-dimensional spatial rotation, spatial reflection, and time inversion, we focus on the rotation within the $(tx, ty, tz) $plane Assuming that the y-axis and z-axis do not undergo transformation, only the t-axis and x-axis undergo transformation to simplify the problem and eliminate three-dimensional spatial rotation, it can be concluded that,
      $$
      \begin{align*}
      \Rightarrow \quad & \left(\begin{matrix} c Δt' \\ Δx' \end{matrix}\right) = \boldsymbol A_{t,x}   \left(\begin{matrix} c Δt \\ Δx \end{matrix}\right)  \\
      & \left(\begin{matrix} -1 \\ & 1 \end{matrix}\right) = \boldsymbol A_{t,x}   \left(\begin{matrix} -1 \\ & 1 \end{matrix}\right) \boldsymbol A_{t,x}  \\
      \Rightarrow \quad & \boldsymbol A_{t,x} = \left(\begin{matrix} a & b \\ c & d \end{matrix}\right) \quad ; \left\{\begin{matrix}
          -a^2 + c^2 = -1  \\
          -b^2 + d^2 =  1  \\
          -a b + c d =  0
          \end{matrix}\right.
      \end{align*}
      $$

      It can be seen that the hyperbolic function $cosh ^ 2 x - sinh ^ 2 x=1$is a solution that satisfies the system of equations, which is the rotation transformation matrix of the $t$-$x$ plane,
      $$
      \boldsymbol A_{t,x} =   \left(\begin{matrix} \cosh μ & \sinh μ \\ \sinh μ & \cosh μ \end{matrix}\right)
      $$

    - In the new inertial reference frame, the origin coordinate is always zero, while in the old inertial reference frame, the origin of the new system moves along the x axis at a velocity of $V$, and the substitution can be solved $μ$ And the objective transformation matrix

      $$
      \left(\begin{matrix} c t' \\ 0 \end{matrix}\right) = \boldsymbol A_{t,x} \left(\begin{matrix} c t \\ V t \end{matrix}\right) =   \left(\begin{matrix} \cosh μ & \sinh μ \\ \sinh μ & \cosh μ \end{matrix}\right)   \left(\begin{matrix} c t \\ V t \end{matrix}\right)
      $$
      $$
      \begin{align*}
      \Rightarrow \quad  & μ = \text{arctanh}\left(-\frac{V}{c}\right)\\
      \Rightarrow \quad  & \left\{\begin{matrix}
          -\tanh μ = -\frac{V}{c} = \frac{\sinh μ}{\cosh μ}  \\
          -\cosh^2 μ - \sinh^2 μ = 1
          \end{matrix}\right.  \\
      \Rightarrow \quad  & \left\{\begin{matrix}
          -\sinh μ = \frac{-\frac{V}{c}}{\sqrt{1 - (\frac{V}{c})^2}}  \\
          -\cosh μ = \frac{1}{\sqrt{1 - (\frac{V}{c})^2}}
          \end{matrix}\right.  \\
      \Rightarrow \quad  &   \left(\begin{matrix} c t' \\ x' \end{matrix}\right) =   \left(\begin{matrix}
          -\frac{1}{\sqrt{1-( \frac{V}{c} )^2}} & \frac{-\frac{V}{c}}{\sqrt{1-(\frac{V}{c} )^2}}\\
          -\frac{-\frac{V}{c}}{\sqrt{1-( \frac{V}{c} )^2}} & \frac{1}{\sqrt{1-( \frac{V}{c} )^2}}
          \end{matrix}\right)   \left(\begin{matrix} c t \\ x \end{matrix}\right)  \\
      \Rightarrow \quad  &   \left(\begin{matrix} t' \\ x' \end{matrix}\right) = \left(\begin{matrix}
          -\frac{1}{\sqrt{1-( \frac{V}{c} )^2}} & \frac{-\frac{V}{c^2}}{\sqrt{1-(\frac{V}{c} )^2}}\\
          -\frac{-V}{\sqrt{1-( \frac{V}{c} )^2}} & \frac{1}{\sqrt{1-( \frac{V}{c} )^2}}
          \end{matrix}\right)   \left(\begin{matrix} t \\ x \end{matrix}\right)
      \end{align*}
      $$

#### Transform of speed
$$
\Rightarrow v_x = \frac{v'_x + V}{1 + v'_x \frac{V}{c^2}}, \quad  v_y = \frac{v'_y \sqrt{1 - \frac{V^2}{c^2}}}{1 + v'_x \frac{V}{c^2}},\quad  v_z = \frac{v'_z \sqrt{1 - \frac{V^2}{c^2}}}{1 + v'_x \frac{V}{c^2}}
$$
- Proof 

$$
\boldsymbol v = \frac{d\boldsymbol r}{dt},\quad  v' = \frac{d\boldsymbol r'}{dt}
$$