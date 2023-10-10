[TOC]

# Small Signal Equivalent Circuits (NMOS)

I think the best way to approach the AC linear amplifier world is to list out all the equations to establish scope, then try to connect them all.

**Keep in mind that in this world, we're basically *always linearizing around operating point*, most of these relationships are crazy and nonlinear so this is all a simplification**

We're also going to skip over a lot of the mosfet equations as well because they're covered in the last session.

## What changes from DC analysis

In DC analysis

- **Channel length modulation was ignored but isn't now**. We assume that once the MOSFET is in saturation, the drain current is constant regardless of $V_{DS}$. Why did we ignore? Screw you thats why basically the textbook decided it wasn't important but it does play a role in DC analysis.
  - So really the full equation all along was $i_D = K_n(v_{GS}-V_{TN})^2(1+\lambda V_{DS})$ but we were assuming $\lambda=0$.
- **Output resistance $r_o$ was also ignored until now**. The output resistance $r_o$  represents the MOSFET's intrinsic resistance between the drain and  source terminals when it's operating in the saturation region. It's  defined as the change in $V_{DS}$ for a given change in $i_D$ in terms of $\lambda$, it's given by: $r_o = (\lambda \cdot i_D)^{-1}$. This makes sense because as the current goes up, the resistance has to have been lower. Obviously this equation goes away when we were assuming $\lambda=0$ but it doesn't now! $r_o$  is the intrinsic output resistance of the MOSFET when it's in the  saturation region. It represents the resistance between the drain and  source terminals of the MOSFET, due to the MOSFET's own internal  characteristics. In other words, when you think of the MOSFET operating in saturation,  you can envision it not just as an ideal current source but as a current source in parallel with a resistance $r_o$. This resistance comes into play due to non-idealities like channel length modulation.
  - $r_o$ is kind of funky because it only really matters on the output. When the MOSFET is simplified to be a current source in series with a resistance, the resistance is this value. It's simply not represented on the input side.

## Lets talk about $\lambda$

In the idealized view of a MOSFET, once it's turned on (i.e., when it's in the saturation region), the current $i_D$ flowing from drain to source is constant, no matter how you vary the drain-source voltage $V_{DS}$. However, in reality, this isn't the case due to a phenomenon called "Channel Length Modulation" (CLM).

Imagine a hose with water flowing through it. Ideally, once the hose is  fully open, the water flow rate remains constant no matter how much you  stretch or squeeze the length of the hose. But in reality, as you  stretch the hose (analogous to increasing $V_{DS}$.), the flow rate might increase slightly because of the change in the  hose's internal properties. This change in flow rate for a change in  hose length is analogous to the effect of channel length modulation in a MOSFET.

In the world of MOSFETs, $\lambda$ represents how much the channel length (or effective channel length) changes with a change in $V_{DS}$.  A higher $\lambda$ means the current $i_D$ is more sensitive to changes in $V_{DS}$.

## Transconductance

Oooh scary what is this? Transconductance quantifies the sensitivity of the current flowing through a transistor (usually denoted as $i_D$). Think of $g_m$ as the "amplification ability" of the transistor itself. If you change  the gate-source voltage slightly, how much does the drain current change in response? A higher gmgm means the transistor is more sensitive and can produce larger changes in $i_d$ for smaller changes in $v_{GS}$.

Unit: Siemens

## Output Resistance

Output of what?

## Voltage gain for Common Source

$A_v = -g_m \times (R_D || r_0)$







$-i_D =K_m[(v_{GS}-V_{TM})^2(1+\lambda v_{DS})]$

$g_m = \frac{i_d}{v_{gs}}$

$g_m = 2 \sqrt{K_n I_{DQ}}$

$\frac{1}{r_o} = \lambda I_{DQ}$

