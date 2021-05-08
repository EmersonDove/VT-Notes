[TOC]

# Simple Harmonic Motion

$$f=\frac{1}{T}$$

Period = $$T$$
Frequency = $$f$$

Angular frequency $$w =  \frac{2\pi}{T}$$ or $w=2\pi f$

Period: $T=\frac{1}{f}= 2\pi \sqrt{\frac{m}{k}}$

Maximum velocity of a wave $$ = v_{max} = \frac{2\pi A}{T} = 2\pi fA = wA$$

Maximum acceleration of a wave $ = -w^2A = (2\pi f)^2A$

General formulas:

$$x(t) = A \cos(wt+\phi_0)$$

$$v_x(t) = \frac{dx}{dt} = -wA\sin(wt+\phi_0) = -v_{max}\sin(wt+\phi_0)$$

$a_x(t) = \frac{d^2x}{dt^2}=-w^2A\cos(wt)$

Energy: $E=K+U=\frac{1}{2}mv^2+\frac{1}{2}kx^2$

# Traveling Waves

Linear Density

$$\mu=\frac{m}{L}$$

$$T_s=\text{tension}$$

Wave speed: $$v=f\lambda=\sqrt{\frac{T_s}{\mu}} = \frac{w}{k}$$

Note: $$v=f\lambda \text{ is from } v=\frac{\text{distance}}{\text{time}}$$

## Sound

### Velocity

$$v_{sound} = \sqrt{\frac{B}{\rho}}$$

$$B = \text{Bulk moduli} Pa$$

$$\rho = \text{density}\ kg/m^3$$

Dry air at 20degC $\approx 343 \ \ m/s$ 

Beat Frequency = $|f_1-f_2|$

### Phase

$$\phi_1=kx_1-wt+\phi_0$$

$$\phi_2=kx_1-wt+\phi_0$$

Phase difference $$\Delta \phi = 2 \pi \frac{\Delta X}{\lambda}$$

# Superposition

$D(x,t) = a\sin(kt-\omega t) + a\sin(kt+\omega t) = sin(\alpha)\cos(\beta) \pm \cos(\alpha)\sin(\beta)$

or

$D(x,y) = 2a\sin(kx)cos(\omega t)$

$f_m = \frac{v}{\lambda_m} = \frac{v}{2 L/m} = m \frac{v}{2L}\ \ \ \ m=1,2,3,4...$

Fundamental frequency: $f_1=\frac{v}{2L}$

Allowed frequencies: $f_m =m f_1\ \ \ \ m=1,2,3,4$

| $m=1$ | $\lambda_1=\frac{2L}{1}$ | $f_1=\frac{v}{2L}$  |
| ----- | ------------------------ | ------------------- |
| $m=2$ | $\lambda_2=\frac{2L}{2}$ | $f_2=2\frac{v}{2L}$ |
| $m=3$ | $\lambda_3=\frac{2L}{3}$ | $f_3=3\frac{v}{2L}$ |

## Open-open or closed-closed tubes:

$m=1,2,3,4...$

$\lambda_m=\frac{2L}{m}$

$f_m=m\frac{v}{2L}=mf_1$

## Open-closed tubes:

$m=1,3,5,7$

$\lambda_m=\frac{4L}{m}$

$f_m=m \frac{v}{4L} = mf_1$

## Maximum interference

Maximum constructive:

$\Delta \phi = 2\pi \frac{\Delta x}{\lambda} + \Delta \phi_0 = m\cdot2\pi\ \text{rad},\ m=0,1,2,3...$

or

$\Delta x = |x_2-x_1| = n\lambda\ \ \ n=0,1,2,...$

Maximum destructive:

$\Delta \phi = 2\pi \frac{\Delta x}{\lambda} + \Delta \phi_0 = (m+\frac{1}{2})\cdot2\pi\ \text{rad},\ m=0,1,2,3...$

or

$\Delta x = |x_2-x_1| = (n+\frac{1}{2})\lambda\ \ \ \ \ n=0,1,2,...$

# Electric Fields

$E=k \frac{q}{r^2}$, where $k=\frac{1}{4\pi\epsilon_0}$

$k=9 \times 10^9$

$\epsilon_0 = 8.85\times 10^{-12}$

**Always point from positive charges to negative charges.**

Mass of Proton: $1.672\times10^{-27}$ kg

Mass of Electron: $9.109\times 10^{-31}$ kg

Elementary Charge: $1.6021\times 10^{-19}$ C

## Electric Field of Line of Charge:

Finite: $E=k\frac{Q}{r(r^2+(\frac{L}{2})^2)^\frac{1}{2}}$

Infinite: $E=\frac{\lambda}{2\pi\epsilon_0 r}$ or $k\frac{2|\lambda|}{r}$

$\lambda = \frac{C}{L}$

## Electric Field of Disk of Charge

$\eta = \frac{Q}{\text{area}} = \frac{Q}{\pi R^2}$

Finite: $E=\frac{\eta}{2 \epsilon_0}(1-\frac{x}{\sqrt{x^2+R^2}})$, where *R* is radius of disk and *x* is distance from the disk.

Infinite (plane): $E=\frac{\eta}{2\epsilon_0}$

## Electric Field of Capacitor

$E_{cap}=\frac{\eta}{\epsilon_0}$

Force of a capacitor plate on the other:

$F=E_{cap}\times q_{other\ plate}$

## Electric Field of Ring of Charge

$\vec{E} = k \frac{Qx}{(x^2+a^2)^{\frac{3}{2}}}$

Where

- *x* is the distance from the center of the ring
- *a* is the radius of the ring

## Electric Field of a Dipole

$\vec{E}_{dipole}=k\frac{2\vec{p}}{r^3}$ (On axis)

$\vec{E}_{dipole} = -k\frac{\vec{p}}{r^3}$ (Bisecting plane)

Where: the direction of $\vec{p}$ identifies the orientation of the dipole

## Sphere of Charge

$\vec{E}_{sphere} =k \frac{Q}{r^2}$ for $r \leq R$

## Motion in a Uniform Field

$a=\frac{qE}{m} = \text{constant}$