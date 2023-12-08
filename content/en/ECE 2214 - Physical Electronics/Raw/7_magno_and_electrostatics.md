[TOC]

# Electric and Magnetic Forces


## Electric Field

### Constants

Vacuum permittivity: $\epsilon _0 = 8.854\times 10^{-12}$

Coulomb's constant: $\frac{1}{4\pi \epsilon _0 } =k = 8.987\times 10^{9}$

### Electric Field From Point Charge

$E=\hat R q \frac{1}{4\pi R^2} \frac{1}{\epsilon_0}$

### Electric Force

$F=q'E$


### Electric Force on Particle 2 from Particle 1

$F=\hat{R} \frac{q_1 q_2}{4\pi \epsilon R^2}$

### Electric Field on Particle 2 due to charge particle 1

$E_1 = \hat{R} \frac{q_1}{4\pi \epsilon R^2}$

### Electric Field of infinite sheet of charge

$E=\frac{\sigma}{2\epsilon_0}$

Where $\sigma$ is the charge density

### Electric field of gap of infinite parallel plates

$E=\frac{\sigma}{\epsilon_0}$

Where $\sigma$ is the charge density

### Electric field of an infinite line of charge

$E=\frac{2k\lambda}{z}$

### Derive Gauss

$$
\Phi = \int E\cdot dA\\
\text{Perform spherical integration}\\
\Phi = R^2(\int_0 ^\pi \sin(\theta)d\theta)(\int_0^{2\pi} d\phi)E\\
\Phi=R^2((-cos(\pi))-(-cos(0)))(2\pi)E\\
\Phi = R^2 4\pi E\\
\text{Now sub in charge formula}\\
\Phi = R^2 4\pi (\frac{1}{4\pi \epsilon_0})\frac{q}{R^2}\\
\Phi = \frac{q}{\epsilon_0}
$$

Could also just use surface area of sphere directly instead of integrating: $A=4\pi r^2$

### Electric Field From A Ring Of Charge

$E(r)=\frac{1}{4\pi \epsilon} \int_C \frac{r-r'}{|r-r'|^3} \rho_l (r')dl$

### Electric Field From A Disk of Of Charge

$E(r) = \frac{1}{4\pi \epsilon} \int_S \frac{r-r'}{|r-r'|^3 \rho _s (r')ds}$



## Magnetic Field

### Constants

$\mu_0 = 4\pi \times 10^{-7}$

Relative Permeability: $\mu_r = {\mu_0}{\mu_r}$

$\Phi$ in this case is flux

### Charged Particle Magnetic Field

Magnetic field: $H=\frac{qv}{4\pi R^2}\times \hat R$

Magnetic flux density: $B(r) = \mu \frac{qv}{4\pi R^2} \hat R$

### Magnetic Field of a Thin Wire

With radius $\rho$ on the direction of the arrow

$H_\phi (p) = \mu_0\frac{I}{2\pi p}$

or

$\vec{H} = \mu_0 \frac{I}{2\pi \rho} \vec{e}_\phi$

Or

$B=\frac{\mu_0 I}{2\pi r}$

### Magnetic Force

$F_m = q v\times B$

### Inductance of Coaxial Structure

$L=\frac{\phi}{I}$

### Magnetic field of a straight coil

$B=\mu_0 (\frac{N}{L})I$

Where $B$ is the magnetic field, $\mu_0$ is the permeability of free space, $N$ is the number of turns in the solenoid, $I$ is the current, $L$ is the length.  $B$ is unit Tesla.

The magnetic flux through a surface perpendicular is $\Phi = B\cdot A$ where A is the area.

### Inductance of a straight coil

$L\approx \frac{-\mu_0 N^2 A}{l}$

Where $N$ is the number of windings, $A$ is the area, $l$ is the length.

### Inductor <> Magnetic Relationships

$L=\frac{N \Phi}{I}$

Where $L$ is inductance measured in henries, $N$ is the number of terms in the coil, $\Phi$ is the magnetic flux in units of webers (Wb), $I$ is the current.

### Ampere's Law

$\int _C H \cdot dl = I_{enc}$

Or 

$\oint B \cdot dl = \mu _0 I$

Notice this works because $B=\mu H$ so you can basically just drop the $\mu$ when substituting because we were given $B$.

## Capacitance

### Capacitance from Area

$C=\frac{\epsilon_0 A}{d}$