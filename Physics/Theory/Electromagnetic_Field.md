# Electromagnetic

[TOC]

## 作用量

描述带电粒子在电磁场中运动的作用量
$$
S = \int_a^b (-mc \mathrm d s - \frac{e}{c}A_i\mathrm dx^i)
$$

### Lagrange 量

$$
L = -mc^2\sqrt{1 - \frac{v^2}{c^2}} + \frac{e}{c}A\cdot v - e \varphi\\
P = \frac{mv}{\sqrt{1 - \frac{v^2}{c^2}}}+\frac{e}{c}A\\
H = \sqrt{m^2c^4 + c^2 (P-\frac{e}{c}A)^2}+e\varphi
$$



### 运动方程

$$
m c \frac{\mathrm d u^i}{\mathrm d s} = \frac{e}{c} F^{ik} u_k \\
F^{ik} = \frac{\partial A_k}{\partial x^i}-\frac{\partial A_i}{\partial x^k}
$$

$$
\frac{\mathrm d p}{\mathrm d t} = eE + \frac{e}{c}v \times H
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
\mathbf{B} = \nabla \times \mathbf{A}
$$

$$
\mathbf{E} = -\grad \Phi - \frac{\partial \mathbf{A}}{\partial t}
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

<img src="./assets/1024px-Snells_law.svg.png" alt="undefined" style="zoom:25%;" />

<img src="./assets/1024px-Refraction_photo.png" alt="undefined" style="zoom:25%;" />

#### Total internal reflection

<img src="./assets/1024px-RefractionReflextion.svg.png" alt="undefined" style="zoom: 40%;" />

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