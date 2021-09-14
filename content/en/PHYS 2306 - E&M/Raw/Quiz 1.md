---
title: Quiz 1
position: 1
category: PHYS 2306 - E&M
---

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

Derivation from standard differential equation for SHM:
$$
\frac{d^2x}{dt^2}+w^2x=0\\
v=\frac{dx}{dt}; dt = \frac{dx}{v}; a= \frac{dv}{dt} = \frac{d^2x}{dt^2}\\
\frac{dv}{dt}dt + w^2x(\frac{dx}{v})=0\\
v\frac{dv}{dt}dt + w^2x dx=0\\
\epsilon=\{ \frac{1}{2} v^2+\frac{1}{2}w^2x^2\} = \text{constant}\\
v=\pm\sqrt{2\epsilon-w^2x^2}\\
\int \frac{du}{\pm \sqrt{1-u^2}}=\sin^{-1}u+\text{constant or } \cos^{-1}u+\text{constant}
$$


## Springs

$$w=\sqrt{\frac{k}{m}}$$

$$f=\frac{1}{2\pi} \sqrt{\frac{k}{m}}$$

$$T=2\pi \sqrt{\frac{m}{k}}$$

## Pendulums

### Simple

For $$\theta << 1,\ \sin(\theta) \approx \theta$$

Angular Frequency:

$$w=2\pi f = \sqrt{\frac{g}{L}}$$

Small amplitude: $ma=-mg\theta$

For small theta: $\theta = \theta_{max}\sin\sqrt{\frac{g}{L}}t$ (from hyperphysics)

Period can be approximated similarly to the spring: $T=2\pi \sqrt{\frac{L}{g}}$

### Physical

$$w=\sqrt{\frac{Mgl}{I}}$$ (Small angle approx)

$$T=2\pi \sqrt{\frac{I}{Mgl}}$$

$\tau_{net}=I\alpha$

$l$ = distance from pivot to center of mass

## Damped Oscillations

$$x(t)=Ae^{-bt/2m}cos(wt+\phi_0)$$

$$b=\text{damping constant}$$

Where 

$$w=\sqrt{\frac{k}{m}-\frac{b^2}{4m^2}}$$

Energy: $$E=E_0e^{\frac{-t}{\tau}}\ \ \ \ t=\tau\ \text{when }\ E=.37E_0$$

# Traveling Waves

Linear Density

$$\mu=\frac{m}{L}$$

$$T_s=\text{tension}$$

Wave speed: $$v=f\lambda=\sqrt{\frac{T_s}{\mu}} = \frac{w}{k}$$

Note: $$v=f\lambda \text{ is from } v=\frac{\text{distance}}{\text{time}}$$

## Light

$$c=f\lambda$$

$$c=299,792,458\ m/s$$

Index of refraction $$= \frac{\text{speed of light in vacuum (c)}}{\text{speed of light in the material (v)}} = \frac{c}{v}$$

For material: $$f_{mat} = f_{vac}$$

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

### Power

$$I = \frac{P_{source}}{4 \pi r^2}$$

$I$ Is in $W/m^2$ and $P_{source}$ is in $W$

### Decible

$\beta = 10 db \log_{10}(\frac{I}{I_0})$

$I_0 = 1 \times10^{-12}\ W/m^2$

### Doppler Effect

#### For sound waves

Approaching Source

$f_+ = \frac{f_0}{1-v_s/v}$ or $f_o=f_s(\frac{v_w}{v_w-v_s})$

Receding Source

$f_- = \frac{f_0}{1+v_s/v}$ or $f_o=f_s(\frac{v_w}{v_w+v_s})$

Approaching Observer

$f_+ = (\frac{1+v_o}{v})f_0$ or $f_o=f_s(\frac{v_w+v_{o}}{v_w})$

Receding Observer

$f_-=(\frac{1-v_o}{v})f_0$ or $f_o=f_s(\frac{v_w-v_{o}}{v_w})$

For observers the wavelength doesn't change when they move.

Bouncing sound (object approaching): 

$f_o=f_i(\frac{v_s+v_{obj}}{v_s})(\frac{v_s}{v_s-v_{obj}})$

#### For light waves

Receding Source

$\lambda_{-}=\sqrt{\frac{1+v_s/c}{1-v_s/c}}\lambda_0$

Approaching Source

$\lambda_+=\sqrt{\frac{1-v_s/c}{1+v_s/c}}\lambda_0$

# Superposition

$D(x,t) = a\sin(kt-wt) + a\sin(kt+wt) = sin(\alpha)\cos(\beta) \pm \cos(\alpha)\sin(\beta)$

$f_m = \frac{v}{\lambda_m} = \frac{v}{2 L/m} = m \frac{v}{2L}\ \ \ \ m=1,2,3,4...$

Fundamental frequency: $f_1=\frac{v}{2L}$

Allowed frequencies: $f_m =m f_1\ \ \ \ m=1,2,3,4$

| $m=1$ | $\lambda_1=\frac{2L}{1}$ | $F_1=\frac{V}{2L}$  |
| ----- | ------------------------ | ------------------- |
| $m=2$ | $\lambda_2=\frac{2L}{2}$ | $f_2=2\frac{v}{2L}$ |
| $m=3$ | $\lambda_3=\frac{2L}{3}$ | $f_3=3\frac{v}{2L}$ |

### Open-open or closed-closed tubes:

$m=1,2,3,4...$

$\lambda_m=\frac{2L}{m}$

$f_m=m\frac{v}{2L}=mf_1$

### Open-closed tubes:

$m=1,3,5,7$

$\lambda_m=\frac{4L}{m}$

$f_m=m \frac{v}{4L} = mf_1$

### Maximum interference

Maximum constructive:

$\Delta \phi = 2\pi \frac{\Delta x}{\lambda} + \Delta \phi_0 = m\cdot2\pi\ \text{rad},\ m=0,1,2,3...$

Maximum destructive:

$\Delta \phi = 2\pi \frac{\Delta x}{\lambda} + \Delta \phi_0 = (m+\frac{1}{2})\cdot2\pi\ \text{rad},\ m=0,1,2,3...$