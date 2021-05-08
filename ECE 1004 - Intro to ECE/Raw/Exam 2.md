[TOC]

# Equations Overview and Relationships

| Relation                                                     | Resistor (R)                      | Capacitor (C)                                | Inductor(L)                                 |
| ------------------------------------------------------------ | --------------------------------- | -------------------------------------------- | ------------------------------------------- |
| $v-i$:                                                       | $v=iR$                            | $v=\frac{1}{C}\int_{t_0}^t i(t) dt + v(t_0)$ | $v=L\frac{di}{dt}$                          |
| $i-v:$                                                       | $I=v/R$                           | $i=C\frac{dv}{dt}$                           | $I=\frac{1}{L}\int_{t_0}^{t} v(t)dt+i(t_0)$ |
| P or w                                                       | $p=I^2R=\frac{v^2}{R}$            | $w=\frac{1}{2}Cv^2$ ($w$ is the energy)      | $w=\frac{1}{2}Li^2$ ($w$ is the energy)     |
| Series                                                       | $R_{eq}=R_1+R_2$                  | $C_{eq} = \frac{C_1C_2}{C_1+C_2}$            | $L_{eq} = L_1+L_2$                          |
| Parallel                                                     | $R_{eq} = \frac{R_1R_2}{R_1+R_2}$ | $C_{eq} = C_1+C_2$                           | $L_{eq} =\frac{L_1L_2}{L_1+L_2}$            |
| Circuit variable that cannot change abruptly:                | N/A                               | $V$  (Capacitors smooth voltage)             | $i$ (Inductors smooth current)              |
| * Other equations are also applicable but shown in each section |                                   |                                              |                                             |

# Capacitors

## Overview

![Capacitor Overview](http://emersondove.com/notes/ECE%201004%20-%20Intro%20to%20ECE/Images/Capacitor_Overview.png)

## Types

### Power Supply Caps

- "Ripple Capacitors"
- Generally used to convert AC to DC, big pulses of current
- Large electrolytic are used for this purpose
- Typically in the 1,000 to 100,000 $\mu F$ range

### Coupling Caps

- Block DC and pass Ac, used in **series**
- Film capacitors are best typically 0.1 to 10 $\mu F$

### Decoupling Caps

- Reduce noise, used in **parallel** with larger ones, can be used with microprocessors
- Often called "bypass" capacitors
- A variety can be used, typically 0.1 to 1,000 $\mu F$

## General Formulas

### Relationship

$q=Cv$

### Current

$I=C\frac{dv}{dt}$

### Charge After Time

$q(t) = \int_{t_0}^t i(t)dt + d(t_0)$

## Dielectric constant

$\epsilon_0 = 8.85 \times 10^{-12} F/m$

$C=\frac{\epsilon A}{d}$

Capacitors can have different dielectric constants, leading to proportionally increased or decreased capacitance.

## Equivalent

Opposite manner of resistors.

# Inductors

## Properties

- If the current through an inductor is constant the voltage across it is zero
- Ideal inductors are treated as having zero resistance.
- **With DC applied, inductor acts like short circuit**
- The current through an inductor cannot change instantaneously, if this did happen, the voltage across the inductor would be infinity 
- This is an important consideration if an inductor is to be turned off abruptly; it will produce a high voltage
- Opposite of capacitor

## Equivalent

Same manner as resistors.

# Synthesis of Logic Circuits

## Sum of Products

| Row  | A    | B    | C    | D    | Equation |
| ---- | ---- | ---- | ---- | ---- | -------- |
| 0    | 0    | 0    | 0    | 1    | (A'B'C') |
| 1    | 0    | 0    | 1    | 0    |          |
| 2    | 0    | 1    | 0    | 1    | (A'BC')  |
| 3    | 0    | 1    | 1    | 0    |          |
| 4    | 1    | 0    | 0    | 0    |          |
| 5    | 1    | 0    | 1    | 0    |          |
| 6    | 1    | 1    | 0    | 1    | (ABC')   |
| 7    | 1    | 1    | 1    | 1    | (ABC)    |

## Product of Sums

| Row  | A    | B    | C    | D    | Equation |
| ---- | ---- | ---- | ---- | ---- | -------- |
| 0    | 0    | 0    | 0    | 1    |          |
| 1    | 0    | 0    | 1    | 0    | A+B+C'   |
| 2    | 0    | 1    | 0    | 1    |          |
| 3    | 0    | 1    | 1    | 0    | A+B'+C'  |
| 4    | 1    | 0    | 0    | 0    | A'+B+C   |
| 5    | 1    | 0    | 1    | 0    | A'+B+C'  |
| 6    | 1    | 1    | 0    | 1    |          |
| 7    | 1    | 1    | 1    | 1    |          |

# Diode

## Properties

- Diodes generally have a voltage drop of 0.7V. Applied voltage has to be greater than 0.7V.
- P type is doped with group 3 (3 electrons in outside shell). Typically boron.
- To make N-type, add electrons, add group 5. Typically phosphorus.
- Anode = positive
- Cathode = negative

# Number Conversions

## Two's Complement

### Overflow Rule

- If 2 Two's Complement numbers are added, and they both have the same sign (both positive or both negative), then overflow occurs if and only if the result has the opposite sign. Overflow never occurs when adding operands with different signs.
  - Adding two positive numbers must give a positive result
  - Adding tow negative numbers must give a negative result

