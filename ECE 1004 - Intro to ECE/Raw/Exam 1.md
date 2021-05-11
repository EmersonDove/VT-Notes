[TOC]

# Circuits

## Energy Relationships

### Power

$$
P=R\times I^2\\
P=I\times V\\
P=\frac{V^2}{R}	
$$

### Voltage

$$
V=I\times R\\
V=\frac{P}{I}\\
V=\sqrt{P\times R}
$$

### Resistance

$$
R=\frac{V}{I}\\
R=\frac{P}{I^2}\\
R=\frac{V^2}{P}
$$

### Current

$$
I=\sqrt{\frac{P}{R}}\\
I=\frac{P}{V}\\
I=\frac{V}{R}
$$



### Energy Delivered

In watts: $\int_{t_1}^{t_2} p(t)dt$

### Conductance

Conductance: $G=\frac{1}{R}$

$I=Gv$

## Power Dissipation

Power absorbed is positive power - when the element gains power.

Power delivered is negative power - when the element distributes power.

## Kirchhoff's Current Law

- The net current entering a node is zero.
- In other words the sum of the currents entering a node is equal to the sum of currents leaving a node. 
- Current entering a node is positive, current leaving is negative.

## Kirchhoff's Voltage Law

- The algebraic sum of the voltages equals zero for any closed path in an electrical circuit
- Voltages are added or subtracted depending on their reference polarities relative to the direction of travel around the loop
  - Entering a voltage source from the negative is subtracted

## Combining Resistors

Series: $R_{eq} = R_1+R_2+R_3+\cdots+R_n$

Parallel: $\frac{1}{R_{eq}} = \frac{1}{R_1}+ \frac{1}{R_2}+\frac{1}{R_3} + \cdots + \frac{1}{R_n}$

## Voltage Divider

For two resistors in series
$$
v_1=v_i\frac{R_1}{R_1+R_2}\\
v_2=v_1\frac{R_2}{R_1+R_2}\\
i=\frac{v_i}{R_1+R_2}
$$

## Current Divider

For two resistors in parallel:
$$
I_{R_1} = I_s(\frac{R_2}{R_1+R_2})\\
I_{R_2} = I_s(\frac{R_1}{R_1+R_2})
$$
Note the different resistor value on top.

# Nodal & Mesh Analysis

## Nodal

- Current entering is negative
- Current leaving is positive
- Currents are just numbers added and need no resistance value
- Need a ground
- Format: $\frac{V_1-V_2}{R_1}+\frac{V1-V_3}{R_2} - i= 0$

### Supernodes

1. Merge the nodes across the voltage source - write as one equation
2. Write an equation relating the nodes: $v_1+10=v_2$ (ex with 10 volts between two nodes)
3. Solve that node system
4. If you have a resistor in parallel you can include it in the super node, but it can also just be ignored. It should cancel in the node equation if you decide to include it.

## Mesh

- Draw loops in each area clockwise or counterclockwise (clockwise is preferred)
- If entering a voltage source from the negative end, thats a negative voltage
- Attached meshes have subtracted currents
- Format: $-v_1+R_1(i_1-i_2) = 0$ for entering a voltage source from the negative end, and a resistance of $R_1$ attached between two loops.

### Supermeshes

1. Write mesh equation around the entire loop with the super mesh (generally include two lops)
2. Write normal equation for any non-supermesh equations
3. Write equation for the current source in the super mesh, might look like $i_1-i_3=3$

# Thévenin & Norton

## Thévenin Procedure

1. Find open circuit voltage
2. Short circuit and find Norton current
3. Compute Thévenin resistance using Ohm's Law ($R_{th} = \frac{V_{oc}}{I_{sc}}$)
4. This works because finding the slope at infinite resistance gives a line that any load that you could possibly use would be between those two values

### Zeroing Method

1. Short voltage source
2. Open current sources
3. Find equivalent Thévenin resistance with respect to the terminals
   1. Once the voltages sources are shorts and the current sources are open, the Thévenin resistance is just $R_{eq}$ from the two leads, generally resistance between *A* and *B*
4. Once you have this you have to go back to the $R_{th}$ relationship and find either 

## Norton

- Another type of equivalent
- Convert the resistor in series with voltage source to one in parallel with source transformation by dividing the voltage by the resistance and getting a current - $I_{source} = \frac{V_{source}}{R_{series}}$.
- Norton current is the short circuit current between the terminals

# Max power transfer

- Efficiency is only 50%
- When Rth = R load
- Most suitable for low-level signals