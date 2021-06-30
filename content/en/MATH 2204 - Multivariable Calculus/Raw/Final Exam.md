---
title: Final Exam
position: 3
category: MATH 2204 - Multivariable Calculus
---

# Multivariable Calculus Final Exam Formulas

# Section 1

## Vector Formulas

### 2D Dot Product

$$\vec{u} \cdot \vec{v} = |\vec{u}||\vec{v}|\cos{\theta}$$

### Scalar Projection

Projection of $$\vec{v}$$ onto $$\vec{u}$$

$$comp_{\vec{u}} \vec{v} = \frac{\vec{u} \cdot \vec{v}}{|\vec{u}|}$$

### Vector Projection

Projection of $$\vec{v}$$ onto $$\vec{u}$$

$$proj_{\vec{u}} \vec{v} = \frac{\vec{u} \cdot \vec{v}}{|\vec{u}|}\frac{\vec{u}}{|\vec{u}|}$$

## Limits

For limits, try to evaluate first by:

- Plugging in (if you get a number it’s done)

- Try squeeze theorem:

- - Find functions g(h) that sandwich X between them
  - $$\lim_{(x,y) \rarr g(x,y)} \le \lim_{(x,y) \rarr f(x,y)} \le \lim_{(x,y) \rarr h(x,y)} $$
  - Most often used for trig functions

- Manipulate f by rationalization, conjugate, factorization

- Polar coordinates (not on test 1)

- If none of the above works, show the limit does not exist

To show doesn't exist

- Find two curves that both go through the point (a,b) such that the limit on those curves are different

## Planes

$$\langle a,b,c \rangle \cdot \langle x-x_0, y-y_0, z-z_0\rangle = 0$$

# Section 2

## Integration Identities

$$
\\Polar\\
r^2=x^2+y^2\\
x=r\cos(\theta)\\
y=r\sin(\theta)\\[30pt]

\\Cartesian\ to\ Cylindrical\\
\\Notice\ this\ is\ Polar\ with\ z=z\\
x=r \cos(\theta)\\
y=r \sin(\theta)\\
z=z\\[10pt]

\\Spherical\ to\ Cylindrical\\
r=\rho \sin(\phi)\\
\theta = \theta\\
z = \rho \cos(\phi)\\[10pt]

\rho^2 = r^2+z^2\\[30pt]

\\Spherical\\
\rho^2=x^2+y^2+z^2\\
\\Notice\ this\ is\ polar\ with\ z\ defined\\
x=r \cos(\theta)\\
y=r \sin(\theta)\\
z=\rho \cos(\phi)\\[10pt]
x=\rho \sin(\phi) \cos(\theta)\\
y=\rho \sin(\phi) \sin(\theta)\\
z=\rho \cos(\phi)\\
$$



# Section 3

## Position Vector

The position vector is given by $$\vec{r}(t)= <x(t),y(t),z(t)>$$ where position is given at any moment $$t$$ by. This can be plotted in 3-space to yield a curve.

### Arc Length

Arc length is the integral of the position vector: $$\int_a^b(| \vec{r}'(t)|)dt$$ where $$a\leq t \leq b$$.

### Distance

In general $$|\vec{r}'(t)| = \sqrt{x^2+y^2+z^2...n^2}$$

## Unit Tangent

Unit tangent is given by $$\vec{T}(t) = \frac{\vec{r}'(t)}{|\vec{r}'{t}|}$$

## Unit Normal

$$\vec{N}(t)=\frac{\vec{T}'(t)}{|\vec{T}'(t)|}$$

- Derivative of unit tangent normalized to unit normal

## Curvature

Vector function:

​	Curvature is given by $$\kappa(t)=\frac{\vec{T}'(t)}{|\vec{r}'(t)|}=\frac{|\vec{r}'(t) \times \vec{r}''(t)|}{|\vec{r}'(t)|^3}$$

Generic $$f(x)$$:

​	$$\kappa(x)=\frac{|f''(x)|}{(1+(f'(x))^2)^\frac{3}{2}}$$

- Always positive
- Measures how bendy

### Binormal

Vector:

​	$$\vec{B}=\vec{T}(t) \times \vec{N}(t)$$

- To quickly calculate
  - Need:
    - Unit tangent
    - Principal unit normal
  - Find by:
    - Start with r r(t) gives space curve
    - Find derivative of R
    - Find Unit tangent
    - Find derivative of the unit tangent
    - Divide by magnitude
    - Take cross product

- For some types of curves the curvature is the same and Binormal is constant

### Normal Plane

Spanned by Normal and Binormal vectors at $$(x_0,y_0,z_0)$$

$$0=\vec{r}'(t_0) \cdot<x-x_0,y-y_0,z-z_0>$$

### Osculating Plane

Kisses space curve

Spanned by Unit Tangent and Principal unit normal at $$(x_0,y_0,z_0)$$

$$0=\vec{B}(t_0) \cdot <x-x_0,y-y_0,z-z_0>$$

## Physics

### Transformation

Velocity

Velocity: $$\vec{v}(t)=\vec{r}'(t)$$

Speed: $$|\vec{v}(t)|$$

Acceleration: $$\vec{a}(t) = \vec{v}'(t)=\vec{r}''(t)$$

### Newtons Second Law

$$\vec{F}(t)=m\vec{a}(t)$$ Where $$\vec{f}$$ is force and $$m$$ is mass

### Projectile Motion

Defined by $$\vec{r}(t)$$

Begins with an initial velocity at time zero $$\vec{v}(0)$$

Goes up at an elevation angle $$\alpha$$ 

Acceleration is at magnitude = $$g \approx 9.8 m/s^2$$

To map an initial velocity back to a vector function: $$\vec{r}(t)=\int<|\vec{v}(0)|\cos(\alpha),|\vec{v}(0)|\sin(\alpha)-gt>dt$$

This can also be done with. This works for position after t given a starting position: $$\vec{r}(0) + <|\vec{v}(0)|\cos(\alpha)t,|\vec{v}(0)|\sin(\alpha)t-\frac{1}{2}gt^2>$$

### Tangential and Normal components of Acceleration

$$\vec{a}(t) = a_T\vec{T}(t)+a_N\vec{N}(t)$$

$$a_T=\frac{d}{dt}|\vec{v}(t)|=\frac{\vec{r}'(t) \cdot \vec{r}''(t)}{|\vec{r}'(t)|}$$

$$a_N=\kappa(t)|\vec{v}(t)|^2=\frac{|\vec{r}'(t) \times \vec{r}''(t)|}{|\vec{r}'(t)|}$$

### Intersections/Collisions

Two space curves $$\vec{r_1}(s)$$ and $$\vec{r_2}(t)$$ intersect when $$\vec{r_1}(t) = \vec{r_2}(s)$$ and $$s=t$$

### Chain Rule

Assume:

​	$$z=f(x_1,x_2,...,x_n)$$

​	$$x_i=g_i(t_1,t_2,...,t_m)$$

Then

​	$$\frac{\partial{z}}{\partial{t_k}}=\frac{\partial{f}}{\partial{x_1}}\frac{\partial{g_1}}{\partial{t_k}} + \frac{\partial{f}}{\partial{x_2}}\frac{\partial{g_2}}{\partial{t_k}} + ... + \frac{\partial{f}}{\partial{x_n}}\frac{\partial{g_n}}{\partial{t_k}}$$

### Directional Derivative

$$D_{\frac{\vec{u}}{|\vec{u}|}}f=\nabla f \cdot \frac{\vec{u}}{|\vec{u}|}$$

$$D_{\vec{u}}f(x,y,z)=f_x(x,y,z)a+f_y(x,y,z)b+f_z(x,y,z)c$$

Where $$a,b,c$$ are the components of the directional vector normalized to a unit vector

$$a=\frac{x}{\sqrt{x^2+y^2+z^2}}$$

Or more generally

$$<a,b,c>=\frac{<x,y,z>}{\sqrt{x^2+y^2+z^2}}$$

### Second partial derivative test

If $$\nabla f(x_0,y_0) = 0$$ then

$$H=f_{xx}(x_0,y_0)f_{yy}(x_0,y_0)-f_{xy}(x_0,y_0)^2$$

If $$H<0$$, then $$(x_0,y_0)$$ is a saddle point

If $$H>0$$, then $$(x_0,y_0)$$ is a maximum or minimum: 

- If $$f_{xx}(x_0,y_0) < 0,\ (x_0,y_0)$$ is a local maximum
- If $$f_{xx}(x_0,y_0) > 0,\ (x_0,y_0)$$ is a local minimum