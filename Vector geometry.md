---
tags:
  - MATH133
---
# Vector geometry
## Vectors and lines
A length of a vector $\vec{v}=\begin{bmatrix}x\\ y\\ z\end{bmatrix}$ is $||\vec{v}||=$::$\sqrt{x^{2}+y^{2}+z^{2}}$.
<!--SR:!2024-12-25,37,250-->
If $\vec{u}$, $\vec{u}\in\mathbb{R}^{3}$ with $\vec{v}=c\vec{u}$ where $c\in\mathbb{R}$ nonzero, then we say that $\vec{u}$ and $\vec{v}$ have (2):
?
- same direction if $c>0$
- opposite direction if $c<0$
<!--SR:!2025-01-10,47,250-->

Vectors of length $1$ are called:: unit vectors.
<!--SR:!2024-12-22,40,290-->
$||c\vec{v}||=$::$|c|\cdot||\vec{v}||$
<!--SR:!2024-12-25,22,230-->

Unit vector $\vec{u}=$::$\frac{\vec{v}}{||\vec{v}||}$
<!--SR:!2024-12-09,22,230-->

If $\vec{Q}$ is a point $\frac{1}{k}^{th}$ the way on a line $\overrightarrow{P_{1}P_{2}}$, than the coordinates of $\vec{Q}=$::$\vec{P_{1}}+\frac{1}{k}\vec{P_{2}}-\frac{1}{k}\vec{P_{1}}=\vec{P_{1}}(1-\frac{1}{k})+\frac{1}{k}\vec{P_{2}}$.
<!--SR:!2024-12-24,29,230-->

Two vectors are parallel if:: one is a multiple of another (they are in the same or opposite direction).
<!--SR:!2025-02-09,67,250-->

Vector equation of a line $\vec{P}=$::$\vec{P_{0}}+t\vec{d}$. $\left\{\begin{matrix}x=x_{0}+ta\\ y=y_{0}+tb\\ z=z_{0}+tc\end{matrix}\right\}$ (parametric equation of the line).
<!--SR:!2025-01-06,47,250-->

Parametric equation of $\vec{P}=P_{1}+t\overrightarrow{P_{1}P_{2}}$ is:: $\left\{\begin{matrix}x=x_{1}+t(x_{2}-x_{1})\\ y=y_{1}+t(y_{2}-y_{1})\\ z=z_{1}+t(y_{2}-y_{1})\end{matrix}\right\}$
<!--SR:!2025-01-05,43,250-->

## Projections and planes
Given $\vec{v}=\begin{bmatrix}x_{1}\\ y_{1}\\ z_{1}\end{bmatrix}$ and $\vec{w}=\begin{bmatrix}x_{2}\\ y_{2}\\ z_{2}\end{bmatrix}$, the dot product (or scalar product) is defined by::$$\vec{v}\cdot\vec{w}=x_{1}x_{2}+y_{1}y_{2}+z_{1}z_{2}=\vec{v}^{T}\vec{w}=||\vec{v}||\cdot||\vec{w}||\cdot\cos\theta$$
<!--SR:!2024-12-09,15,172-->
(It is a scalar).

$\cos\theta=\frac{\vec{v}\cdot\vec{w}}{||\vec{v}||\cdot||\vec{w}||}$

- Is the dot product commutative ($\vec{v}\cdot\vec{w}=\vec{w}\cdot\vec{v}$) ?:: Yes.
<!--SR:!2025-01-27,54,252-->
- $\vec{v}\cdot\vec{0}=$::$0$
<!--SR:!2024-12-11,28,252-->
- $\vec{v}\cdot\vec{v}=$::$||\vec{v}||^{2}$
<!--SR:!2025-01-11,44,252-->
- $\vec{v}\cdot(k\vec{w})=$::$(k\vec{v})\cdot\vec{w}=k(\vec{v}\cdot\vec{w})$
<!--SR:!2025-02-07,62,252-->
- $\vec{v}\cdot(\vec{u}+\vec{w})=$::$\vec{v}\cdot\vec{u}+\vec{v}\cdot\vec{w}$
<!--SR:!2025-01-30,57,252-->

Two vectors are orthogonal if:: and only if $\vec{v}\cdot\vec{w}=0$, (either $\vec{v}=0$ or $\vec{w}=0$ or $\theta\angle(\vec{v},\,\vec{w})=\frac{\pi}{2}$).
<!--SR:!2024-12-10,27,252-->
If the dot product between two vectors is positive, the angle between them is:: less than $\frac{\pi}{2}$.
<!--SR:!2024-12-24,31,247-->


![[image-20241031192952475.png]]
The vector $\vec{v_{1}}$ is called and denoted:
?
The projection of $\vec{v}$ on $\vec{d}$ and denoted by $\vec{v_{1}}=\text{proj}_{\vec{d}}\vec{v}$
<!--SR:!2025-01-27,54,252-->


Scalar projection of $\vec{v}$ onto $\vec{d}$ is:: $$\frac{\vec{v}\cdot \vec{d}}{||\vec{d}||}$$
<!--SR:!2024-12-30,28,207-->
$\vec{v}$, $\vec{d}$ two vectors ($\vec{d}\neq 0$), then $\text{proj}_{\vec{d}}\vec{v}$ is::$$\text{proj}_{\vec{d}}\vec{v}=\frac{\vec{v}\cdot \vec{d}}{||\vec{d}||}\cdot \frac{\vec{d}}{||\vec{d}||}=\frac{\vec{v}\cdot \vec{d}}{||\vec{d}||^{2}}\vec{d}$$
<!--SR:!2024-12-22,20,232-->

Any vector that is orthogonal to a plane is called:: a normal vector to that plane.
<!--SR:!2024-12-16,27,249-->

![[image-20241101154037946.png]]$P$ is on the plane if:: and only if $\overrightarrow{P_{0}P}$ and $\vec{n}$ are orthogonal. ($\overrightarrow{P_{0}P}\cdot \vec{n}=0$).
<!--SR:!2025-01-27,51,249-->

![[image-20241101154738050.png]]Vector equation of plane $d=$::$\vec{P_{0}}\cdot\vec{n}=\vec{P}\cdot \vec{n}$
<!--SR:!2025-01-03,36,231-->

Two planes are parallel if:: and only if their normal vectors are parallel. ($\vec{n_{1}}\times \vec{n_{2}}=0$)
<!--SR:!2025-01-16,46,251-->

Given $\vec{v}=\begin{bmatrix}x_{1}\\ y_{1}\\ z_{1}\end{bmatrix}$ and $\vec{w}=\begin{bmatrix}x_{2}\\ y_{2}\\ z_{2}\end{bmatrix}$, the cross product (or vector product) is defined by::$$\vec{v}\times\vec{w}=\begin{bmatrix}y_{1}z_{2}-y_{2}z_{1}\\-x_{1}z_{2}+x_{2}z_{1}\\x_{1}y_{2}-x_{2}y_{1}\end{bmatrix}=\begin{vmatrix}\vec{i}&x_{1}&x_{2}\\\vec{j}&y_{1}&y_{2}\\\vec{k}&z_{1}&z_{2}\end{vmatrix}$$
<!--SR:!2024-12-30,30,211-->

1. $\vec{v_{1}}\times \vec{v_{2}}$ is always:: orthogonal to $\vec{v_{1}}$ and $\vec{v_{2}}$.
<!--SR:!2024-12-31,37,251-->
2. $\vec{v_{1}}\times \vec{v_{2}}=0$ if:: and only $\vec{v_{1}}$ and $\vec{v_{2}}$ are parallel ($\vec{v_{1}}$, $\vec{v_{2}}$ non-zero)
<!--SR:!2025-01-24,51,251-->

![[image-20241101163941426.png]] $\vec{n}=$::$\overrightarrow{PQ}\times \overrightarrow{PR}$
<!--SR:!2025-01-19,49,251-->


To find a point on a plane with the vector equation of plane, we can:: set $y=z=0$ and so $x=\frac{d}{a}$.
<!--SR:!2024-12-16,9,190-->

- $\vec{v}\times \vec{0}=$::$\vec{0}\times\vec{v}=\vec{0}$
<!--SR:!2024-12-10,22,229-->
- $\vec{v}\times \vec{v}=$::$\vec{0}$
<!--SR:!2024-12-18,14,211-->
- $\vec{v_{1}}\times \vec{v_{2}}=$::$-\vec{v_{2}}\times \vec{v_{1}}$
<!--SR:!2024-12-16,21,230-->
- $(k \vec{v_{1}})\times \vec{v_{2}}=$::$\vec{v_{1}}\times (k \vec{v_{2}})=k(\vec{v_{1}}\times \vec{v_{2}})$
<!--SR:!2025-01-21,49,251-->
- $\vec{v_1}\times (\vec{v_2}+\vec{v_3})=$::$\vec{v_1}\times \vec{v_2}+\vec{v_1}\times \vec{v_3}$
<!--SR:!2025-01-20,49,250-->
- $(\vec{v_1}+\vec{v_2})\times \vec{v_3}$=::$\vec{v_1}\times \vec{v_3}+\vec{v_2}\times \vec{v_3}$
<!--SR:!2025-01-09,42,250-->

Let $\vec{v_0}$, $\vec{v_1}$, $\vec{v_{2}} \in\mathbb{R}^{3}$. Then $\vec{v_0}\cdot \vec{v_1}\times \vec{v_2}=$::$\det \begin{pmatrix}\vec{v_0}&\vec{v_1}&\vec{v_2}\end{pmatrix}$ (cross product is calculated first)
<!--SR:!2025-01-01,36,231-->

Lagrange's identity::$$\begin{Vmatrix}\vec{v_1}\times \vec{v_2}\end{Vmatrix}^{2}=||\vec{v_{1}}||^{2}||\vec{v_{2}}||^{2}-(\vec{v_{1}}\cdot \vec{v_{2}})^{2}$$
<!--SR:!2025-01-11,37,210-->

- $\begin{Vmatrix}\vec{v_1}\times \vec{v_2}\end{Vmatrix}=$::$||\vec{v_{1}}||||\vec{v_{2}}||\sin\theta$
<!--SR:!2025-01-19,48,251-->
- $\begin{Vmatrix}\vec{v_1}\times \vec{v_2}\end{Vmatrix}$ represents:: the area of parallelogram
<!--SR:!2025-01-25,52,251-->
- $\vec{v_{1}}$ and $\vec{v_{2}}$ are parallel if:: $\vec{v_{1}}\times \vec{v_{2}}=0$
<!--SR:!2024-12-30,37,250-->
- The area of a parallelogram formed by two vectors $\vec{v_1}$ and $\vec{v_2}$ can be found by doing:: $\begin{Vmatrix}\vec{v_1}\times \vec{v_2}\end{Vmatrix}$.
<!--SR:!2025-01-29,54,250-->
- The volume of a parallelepiped formed by three vectors $\vec{v_1}$, $\vec{v_{2}}$ and $\vec{v_3}$ can be found by doing:: $\begin{Vmatrix}\vec{v_1}\cdot (\vec{v_2}\times \vec{v_{3}})\end{Vmatrix}=\det \begin{pmatrix}\vec{v_1}&\vec{v_2}&\vec{v_3}\end{pmatrix}$.
<!--SR:!2024-12-23,17,224-->



- $\theta=$::$\frac{||\vec{v}\times \vec{w}||}{\vec{v}\cdot \vec{w}}$
<!--SR:!2025-01-03,33,244-->