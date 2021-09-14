---
title: Quiz 3
position: 3
category: PHYS 2306 - E&M
---

# Constants

Elementary Charge: $e =1.602 \times 10^{-19}$C

Mass of Electron: $m = 9.109 \times 10^{-31} \text{kg}$

Mass of Proton: $m=1.672\times 10^{-27} \text{kg}$

Vacuum Permittivity: $\epsilon_0 = 8.854\times 10^{-12}$

Coulomb Constant: $k = 9.0\times 10^9 \frac{N m^2}{C^2}$

# Gauss's Law

## Flux Equations

### Flux through a surface

$\Phi_e=E_\perp A = EA\cos(\theta)$ where $\theta$ is the angle between the normal line and the flux lines or the angle between $\hat{n}$ and $\vec{E}$.

### Flux Integral

$\Phi_{e} = \oint \vec{E} \cdot d\vec{A}$

When using a Gaussian sphere:

$\Phi_e = \frac{q}{4\pi \epsilon_0 r^2} \cdot 4\pi r^2 = \frac{q}{\epsilon_0}$

### Gauss Law Combined

$\Phi_{e} = \oint \vec{E} \cdot d\vec{A} = \frac{Q_{in}}{\epsilon_0}$

### Most General Use

$$
\Phi_e = EA_{sphere} = 4\pi r^2 E\\
\text{when using the surface area of a sphere:}\\
4\pi r^2E=\frac{Q_{in}}{\epsilon_0}
$$

### Flux Around a Charged Wire

$\Phi_e=2\pi rLE = \frac{Q_{in}}{\epsilon_0} = \frac{\lambda L}{\epsilon_0}$

Notice this the same as the sphere, except the surface area is just the perimeter of a circle $\times$ length.

### Flux of Infinite Plane of Charge

$Q_{in} = \eta A$

$\Phi_e=2EA=\frac{Q_{in}}{\epsilon_0} = \frac{\eta A}{\epsilon_0}$

Area divides out revealing:

$E_{plane} = \frac{\eta}{2\epsilon_0}$

# Electric Potential

## Uniform Electric Field

$U_{elec} = U_0 + qEs$

$U_0$ is the potential at the negative plate (often $U_0 = 0$)

$s$ is the distance from the negative plate

## Difference for Negative and Positive Charges

In general, movement against the electric field is negative energy.

### Positive

- Field direction is "downhill." Potential energy decreases as the charge speeds up.
- Potential goes down and kinetic goes up as it moves to the negative.

### Negative

- Field direction is "uphill." Potential energy increases as the charge slows.
- Potential goes up and kinetic goes down as it moves toward the negative.
- The movement of an electron towards the positive (natural movement) is *negative* mechanical energy: $E_{mech} = K_i + (-e)Ed$. $K_i$ is zero.

## Potential Equations

### Potential Energy of Point Charges

$U_{elec} = K \frac{q_q q_2}{r}$ or $\frac{1}{4\pi \epsilon_0} \frac{q_1 q_2}{r}$

### Escape speed

$K_f+U_f=K_i+U_i$

$v_i = \sqrt{\frac{K q_1 q_2}{m r_i}} \larr$ Unclear when the usage of this is.

### Potential of a Dipole

$U_{dipole} = -pE \cos(\phi) = -\vec{p}\cdot \vec{E}$

Where $\vec{p}$ is the dipole vector

### Electric Potential Energy from Voltage

$U_q = qV$

Where 1 volt = $1\ J/C$

Example: A proton would loose $-100e$ moving through $100V$. Potential is negative even though the charge is positive:
$$
K_f+qV_f=K_i+qV_i\\
K_f=K_i-q\Delta V
$$


### Electric Potential inside a Parallel-Plate Capacitor

$V=Es$, where *s* is the distance form the *negative* electrode

Field can also be defined by $E=\frac{\Delta V_C}{d}$. This is more common.

### Electric Potential from a Point Charge

$V=k \frac{q}{r}$

### Electric Potential from a Ring

$V_{ring\ on\ axis} = k \frac{Q}{\sqrt{R^2+z^2}}$, R is radius, z is distance.

### Electric Potential from Charged Disk

$V_{disk\ on\ axis} = \frac{Q}{2 \pi \epsilon_0 R^2}(\sqrt{R^2+z^2}-z)$

# Potential and Field

$\Delta V = V_f -V_i = -\int_{s_i}^{s_f} E_s ds$

## Electric Field from Potential

$E_s = -\frac{dV}{ds} \larr$ Ensuring that a $\Delta$ is always $final - initial$ is important. The this equation is bad for varying electric fields.

## Energy from Electric Field or Potential

Because $U_{elec} = U_0 + qEs$, the integral above ($-\int_{s_i}^{s_f} E_s ds$) can be multiplied by charge to get field because $\text{Voltage} = J/C$.

## Field Equations

### Field of radial rod and shell:

$E(r) = \frac{\lambda}{2\pi \epsilon_0 r}$, $\lambda$ is equal to the charge density of all enclosed charges.

# Capacitors

## Charge on Capacitor

$Q=C \Delta V$

### Parallel Plate Capacitor

$E=\frac{Q}{\epsilon_0 A}$ or $C=\frac{Q}{\Delta V_c} = \frac{\epsilon_0 A}{d}$

## Equivalent Capacitance

### Parallel

$C_{eq} =C_1+C_2+C_3 + \cdots$

### Series

$C_{eq} = (\frac{1}{C_1}+\frac{1}{C_2}+\frac{1}{C_3} + \cdots)^{-1}$

## Energy of Capacitor

$U_C=\frac{1}{2}C(\Delta V)^2$

## Dielectric Constant

$\kappa = \frac{E_0}{E}$

Capacitance is then increased proportionally:

$C=\kappa C_0$

This is designed to let air be $\kappa = 1$

## Change in Voltage

$\Delta V = V_f- V_i = - \int_{s_i}^{s_f} E_s ds$

## Concentric Cylinders

$C=\frac{2\pi \epsilon_0 l}{\ln(\frac{R_2}{R_1})}$

## Concentric Spheres

$C=\frac{4\pi \epsilon_0}{\frac{1}{R_1}-\frac{1}{R_2}}$

