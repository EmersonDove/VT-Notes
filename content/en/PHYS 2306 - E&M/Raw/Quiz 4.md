---
title: Quiz 4
position: 4
category: PHYS 2306 - E&M
---

# Ohm's Law

$\Delta V=IR$

# Kirchoff's Laws

The sum of changes in voltage around a circuit in any given loop is always zero: $\Delta V_{loop} =\Sigma(\Delta V)_i=0$

# Power

Power dissipated by an element with some resistance (or just resistor): $P_R = I\Delta V_R = I^2R=\frac{(\Delta V_R)^2}{R}$

# Equivalent Resistance

## Series

$R_{eq} = R_1+R_2+ \cdots + R_N$

## Parallel

$R_{eq} =(\frac{1}{R_1}+\frac{1}{R_2}+ \cdots + \frac{1}{R_N})^{-1}$

# RC Circuits

## Properties

- Capacitors in series always have the same amount of charge.

## Energy of Capacitor

$E=\frac{1}{2}CV^2$

## Capacitor Relationship

$Q=CV$

## Time Constant

$\tau = RC$

## Capacitor Equations

### Discharging

#### Charge After Time

$Q=Q_0e^{-t/\tau}$

#### Current After Time

$I=-\frac{dQ}{dt}=\frac{Q_0}{\tau}e^{-t/\tau}=I_0e^{-t/\tau}$

#### Voltage After Time

$V_C=V_0e^{-t/\tau}$

### Charging

#### Charge After Time

$Q=CV_b[1-e^{\frac{-t}{\tau}}]$

#### Charging Current

$I=\frac{V_b}{R}e^{\frac{-t}{\tau}}$

# Magnetic Field

## Constants

$\mu_0 = 4\pi\times10^{-7} T\ m/a$

## Equations

### Point Charge

$\vec{B}_{point\ charge} = \frac{\mu_0}{4\pi} \frac{q\vec{v}\times \hat{r}}{r^2}$

Or sometimes easier:

$\vec{B}_{point\ charge} = \frac{\mu_0}{4\pi}\frac{q\vec{v}\times \vec{r}}{r^3}$

Notice the second one does not involve finding the $\hat{}$ (unit vector) of *r*. 

### Current Segment

$\vec{B}_{current\ segment} = \frac{\mu_0}{4\pi} \frac{I dl\times \hat{r}}{r^2}$

Notice a current segment is an equation representing point charges.

### Infinite Wire

$B=\frac{\mu_0}{2\pi} \frac{I}{r}$

### A current loop

With N turns:

$B_{center} = \frac{\mu_0}{2}\frac{NI}{R}$

#### Dipole Moment of Ring

$\vec{B}_{dipole} = \frac{\mu_0}{4\pi}\frac{2\vec{\mu}}{z^3}$

or

$\vec{\mu} = (AI, \text{from South Pole to North Pole})$

*A* is the area of the loop, *I* is current.

### Solenoid

With coil density $n=N/L$

$B=\mu_0nI =\frac{\mu_0NI}{L}$

### Loop off of the X-Y Plane

$B_{loop} = \frac{\mu_0}{2} \frac{IR^2}{(z^2+R^2)^{3/2}}$

Where *R* is the ring radius, *Z* is the distance from the center.

## Ampère's Law

$\int_{surface}\vec{B} \cdot d\vec{s} = \mu_0I_{through}$

If you curl your right fingers around the closed path in the direction in which you are going to integrate, then any current passing through the bounded area in the direction of your thumb is a positive current. Any direction opposite is a negative current.

## Field of Wire With Thickness

## Inside

$B=\frac{\mu_0 I}{2\pi r}r$

Where *r* is the inner radius.

## Outside

Reuse Ampère's law:

$B=\frac{\mu_0 I}{2\pi R}$

Where *R* is distance outside.

# Cross Product

Determinant of matrix

## 2 Dimensions

$||A\times B|| = ||\vec{A}||\ ||\vec{B}|| \sin(\theta)$

Or $= A_1B_2 - A_2B_1$

## 3 Dimensions

$$
\vec{u}\times \vec{v} =
\begin{bmatrix}
\vec{i} & \vec{j} & \vec{k} \\
u_x & u_y & u_z\\
v_x & v_y & v_z
\end{bmatrix}=
\begin{bmatrix}
u_y & u_z\\
v_y & v_z
\end{bmatrix}\vec{i}-
\begin{bmatrix}
u_x & u_z\\
v_x & v_z
\end{bmatrix}\vec{j}+
\begin{bmatrix}
u_x & u_y\\
v_x & v_y
\end{bmatrix}\vec{k}
$$

