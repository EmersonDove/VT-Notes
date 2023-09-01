---
title: Semiconductors
position: 1
category: ECE 2214 - Physical Electronics
---

[TOC]

# On Semiconductors

There a bit of information I think is lost about semiconductors. There are really two types.

**Intrinsic Semiconductors**: These are pure, unchanged semiconductors. In any situation the charge of the material is neutral, so any electrons getting knocked in or out of their conduction bands will always create/leave behind a hole. You may ask why this is different than basically any other material. Wouldn't with just a piece of plastic there would be holes left behind when the electrons jump off? The answer is YES! The difference is that the difference between semiconductors and a piece of plastic is that as semiconductors heat up, more electrons jump out into the conduction band and the ease to jump into the conduction band is much easier than a piece of plastic. The term "semi" here in "semiconductor" is really just a term that means its less conductive than pure metal, but more conductive than an insulator like a piece of plastic.

To illustrate this further, let's take a bit of germanium (semiconductor). The resistivity of undated germanium at room temperature is approximately $0.47 \text{ohm-meters}$  while copper's is $1.68 \times 10^{-8} \text{ohm-meters}$. Intrinsic germanium is about 28 million times more resistive than copper at room temperature.

And just for fun if you increase the temperature of a semiconductor it becomes more conductive while metals become less conductive - this is because they're conductive for different reasons - semiconductors are conductive because of the atoms jumping to the conduction band. Metals are conductive because of just free electrons sitting around so when they heat up the vibrating lattice will make it harder for the electrons to move. Practically an intrinsic semiconductor will never become as conductive as a metal no matter how much you heat it up because it'll just melt or the lattice will break down but it's fun to illustrate the point.

**Doped Semiconductors**: As soon as they're doped all bets about $n=p=n_i$ are off. You're in a situation where $n \gg p$ or $p \gg n$.

So because semiconductors are typically so resistive, the majority of practical applications they have to be doped. The resistance drops a ton when doped for example heavily doped germanium, resistivities can range from $10^{-2}$ to $10^{-3}$ ohm-meters and as we mentioned above copper is somewhere around $1.68\times 10^{-8}$ ohm-meters.

The reality is that this simple property of almost being a conductor allows them to interact in all kinds of cool ways like conducting when theres light or becoming more conductive when temperatures change.

## Intrinsic Carrier Concentration $n_i$.

The next bit after understanding semiconductors is basically asking "well how semi are those conductors." Well it depends on material. So take this table:

| Material                | $E_g (eV)$ | $B(cm^{-3} K^{-3/2})$ |
| ----------------------- | ---------- | --------------------- |
| Silicon (Si)            | 1.1        | $5.23 \times 10^{15}$ |
| Gallium Arsenide (GaAs) | 1.4        | $2.10\times 10^{14}$  |
| Germanium (Ge)          | 0.66       | $1.66\times10^{15}$   |

Where **$E_g$** is the bandgap energy for the electrons to jump to the conduction band (in electron volts) and the valence band. The lower this is the easier it is for the electrons to jump up and start conducting electricity, and **$B$** is just scaling the interaction with temperature. It reflects how the number of intrinsic carriers change with temperature.

For sanity, the $n_i$ is talking about the **number of charge carriers per unit volume, typically $cm^{-3}$**. A value like $1.66\times10^{15}$ typically represents that many electron/hole pairs per cubic cm.

### Calculate Intrinsic Carrier Concentration

$n_i = BT^{3/2}e^\frac{-E_g}{2kT}$

and remember $k=8.617\times 10^{-5}$

## Extrinsic Carrier Concentration

Intrinsic semiconductors are pure and have an equal number of electrons ($n$) and holes ($p$). Hence, in intrinsic semiconductors, $n=p=n_i$

**n-type Semiconductor**: Doping with donor atoms (like phosphorus in silicon) introduces extra electrons. In this case, $n \gg p$ or $p \gg n$.

This creates a new equation which is true for both *intrinsic* **and** *extrinsic* semiconductors which is $n\times p = n_i^2$. This is true by the *law of mass action*. And remember *p and n are charge carriers per unit volume, typically $cm^{-3}$*.

Lets talk about doping concentration units

**$N_D$**: This represents the concentration of donor impurities in the  semiconductor. Donor impurities are atoms that, when added to a  semiconductor, "donate" an extra electron to the conduction band. When a semiconductor is doped with donor atoms, it becomes an n-type  (negative-type) semiconductor because of the excess electrons. Common  donor atoms for silicon include phosphorus (P) and arsenic (As).

**$N_A$**: This stands for the concentration of acceptor impurities. Acceptor  impurities are atoms that "accept" an electron, creating a hole in the  valence band. When a semiconductor is doped with acceptor atoms, it  becomes a p-type (positive-type) semiconductor because of the excess  holes. Boron (B) is a common acceptor atom for silicon.

In the context of the statement "If $N_D \gg n_i$ then $n≈N_D"$ — it means:

If the concentration of donor atoms ($N_D$) is much greater than the intrinsic carrier concentration ($n_i$), then the majority carrier concentration of electrons (nn) will be approximately equal to $N_D$. In simpler terms, in a heavily doped n-type semiconductor, the number of free electrons is approximately equal to the number of donor atoms.

Therefore:
$$
p=n_i^2 / N_D\ \ \text{if donor is dominant} \\
n=n_i^2 / N_A\ \ \text{if acceptors is dominant}
$$

### All extrinsic relationships hold true for intrinsic carrier concentration its just that sometimes we can forget about the minority carrier

This is true for extrinsic and intrinsic: $n_i = BT^{3/2}e^\frac{-E_g}{2kT}$

This is true for extrinsic and intrinsic: $n\times p = n_i^2$ and **$n=p=n_i$ is a special case of the first equation.**

