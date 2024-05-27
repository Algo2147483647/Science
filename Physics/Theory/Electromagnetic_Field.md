# Electromagnetic Field

[TOC]

# Concepts

Electromagnetic Field 通过四维矢势 $A^i$ 来描述, $\varphi, \boldsymbol A$ 分别是电势和磁矢势.
$$
A^i = (\varphi, \boldsymbol A)
$$


## The action of a charged particle moving in an electromagnetic field

The action of a charged particle moving in an electromagnetic field
$$
S = \int_a^b (-mc \mathrm{d} s - \frac{e}{c}A_i\mathrm{d}x^i)
$$

### Lagrangian

$$
L = -mc^2\sqrt{1 - \frac{v^2}{c^2}} + \frac{e}{c}A\cdot v - e \varphi\\
P = \frac{mv}{\sqrt{1 - \frac{v^2}{c^2}}}+\frac{e}{c}A\\
H = \sqrt{m^2c^4 + c^2 (P-\frac{e}{c}A)^2}+e\varphi
$$



### Equation of motion

$$
m c \frac{\mathrm{d} u^i}{\mathrm{d} s} = \frac{e}{c} F^{ik} u_k \\
F^{ik} = \frac{\partial A_k}{\partial x^i}-\frac{\partial A_i}{\partial x^k}=\left(\begin{matrix} 0 & -E_x & -E_y & -E_z \\ E_x & 0 & -H_z & H_y \\ E_y & H_z & 0 & -H_x \\ E_z & -H_y  & H_x & 0 \end{matrix}\right)
$$

三维形式:

$$
\frac{\mathrm{d} \boldsymbol p}{\mathrm{d} t} = e \boldsymbol E + \frac{e}{c} \boldsymbol v \times \boldsymbol H \\
\frac{\mathrm{d} \mathrm E_{kin}}{\mathrm{d} t} = e \boldsymbol E \cdot \boldsymbol v
$$

- Proof
  $$
  \begin{align*}
  δ S &= 0\\
  δ\int_a^b (-mc \mathrm{d} s - \frac{e}{c}A_i\mathrm{d}x^i) &= 0\\
  \int_a^b (mc \frac{\mathrm{d} x_i\mathrm{d} δ x^i}{\mathrm{d} s} + \frac{e}{c}A_iδ\mathrm{d}x^i + \frac{e}{c}δA_i\mathrm{d}x^i)
   &= 0 \tag{$\mathrm{d} s = \sqrt{\mathrm{d} x_i\mathrm{d} x^i}$}\\
  \int_a^b (mc \mathrm{d} u_i \mathrm{d} δ x^i + \frac{e}{c}A_iδ\mathrm{d}x^i + \frac{e}{c}δA_i\mathrm{d}x^i) &= 0 \tag{$u_i = \frac{\mathrm{d} x_i}{\mathrm{d} s}$}\\
  \int_a^b \left(mc \frac{\mathrm{d} u_i}{\mathrm{d} s} - \frac{e}{c}\left(\frac{\partial A_k}{\partial x^i}-\frac{\partial A_i}{\partial x^k} \right)u_k\right)δx^i \mathrm{d} s &= 0\\
  mc \frac{\mathrm{d} u_i}{\mathrm{d} s} - \frac{e}{c}\left(\frac{\partial A_k}{\partial x^i}-\frac{\partial A_i}{\partial x^k} \right)u_k&=0
  \end{align*}
  $$
  

## 场的参考系变换

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


此外，磁场的矢量势（A）和电场的标量势（Φ）与电场和磁场之间的关系为：

$$
\mathbf{B} = \nabla \times \mathbf{A}\\
\mathbf{E} = -\grad \Phi - \frac{\partial \mathbf{A}}{\partial t}
$$

## Electromagnetic field action

$$
S = \sum\int mc \mathrm ds - \sum \int \frac{e}{c} A_k \mathrm dx^k - \frac{1}{16 \pi c} \int F_{ik}F^{ik} \mathrm d \Omega
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

## Geometrical Optics

### Basic Principles

- Light propagates in a straight line.
- Light paths are reversible.
- When two beams of light propagate without interference and converge at the same point, their intensities simply add up.
- Laws of light propagation at the interface between media.

#### Reflection

**Specular reflection** states that a reflected ray of light emerges from the reflecting surface at the same angle to the surface normal as the incident ray, but on the opposing side of the surface normal in the plane formed by the incident and reflected rays.
$$
θ_i = θ_o
$$

<img src="./assets/800px-Reflection_angles.svg.png" alt="undefined" style="zoom: 20%;" />

<img src="./assets/1024px-Fényvisszaverődés.jpg" alt="undefined" style="zoom: 22%;" />

#### Reflected ray calculation

$$
\boldsymbol L_o = \boldsymbol L_i - 2 (\boldsymbol N · \boldsymbol L_i) \boldsymbol N
$$

Where:
- $\boldsymbol L_o$ is the outgoing (reflected) light direction.
- $\boldsymbol L_i$ is the incoming (incident) light direction.
- $\boldsymbol N$ is the surface normal at the point of reflection.
- $\cdot$ represents the dot product between two vectors.

#### Refraction
$$
n_i·\sin θ_i = n_o·\sin θ_o
$$

#### Total internal reflection

Total internal reflection is a phenomenon that occurs when a ray of light traveling from a denser medium to a less dense medium is incident on the boundary between the two media at an angle of incidence greater than the critical angle. When this happens, instead of the light refracting (bending) as it normally would when passing from one medium to another, all of the light is reflected back into the denser medium.

### 干涉

#### 双缝干涉

#### Newton环

#### 薄膜干涉

### 衍射

#### 菲涅尔衍射

#### 夫郎禾费单缝衍射

#### 光栅衍射

### 偏振

#### 马吕斯定律

#### 布儒斯特定律