[TOC]

# Numeric Data Types

## Whole Numbers

- Int: -32,768 to 32,767
- Unsigned int - range: 0 to 65,535
- Both are stored in 2 bytes for a total of 16 bits
- Long - range: -2,147,483, 648 to 2,147,483,647
- Unsigned Long - range: 0 to 4,294,967,295
- Both are stored in 4 bytes for a total of 32 bits

## Decimals

- Float range: $-3.4028235 \times 10^{38}$ to $3.4028235 \times 10^{38}$
- Double command has the same range
- Both are stored in 4 bytes, *double* does not add more precision on the uno but will on more complex platforms

# Coding

## On the Uno

- Done via Arduino IDE - Integrated development environment
- Programs in Arduino are called "sketches."
- Once a sketch is completed it must be Verified (Compiled), then it can be uploaded to the device
- Unos use AVR C which is a set of C/C++

## Organization

- Sequence
  - Executing lines one after the other
- Selection
  - Control flow, making decisions, if/else
- Iteration
  - Looping
- Function
  - Name
  - Parameter List
    - Parameters must be given a name and a type
    - Functions with no parameters have empty parenthesis 
  - Curly braces
  - Type of return
    - Void means return nothin
    - Type can be any C value: int, long, double, bool

# Sequential Logic Circuits 

- Sequential logic circuits depend not only on the current input values, but also on the past input values 
- Often sequential logic circuits are synchronized using a clock signal
  - These are said to be synchronous

## Latches

- Most basic building block of sequential circuit
- Have two stables states: 0 and 1
  - Stores 1 bit of information
- Many variations exist
- Constructed from two inverters
- The output from inverter 1 is tied to the input of the other

### Truth Table (async)

| R    | S    | $Q_n$       |
| ---- | ---- | ----------- |
| 0    | 0    | $Q_{n-1}$   |
| 0    | 1    | 1           |
| 1    | 0    | 0           |
| 1    | 1    | Not allowed |
|      |      |             |

## Clocked SR Latch

- You can also attach a clock signal to trigger the SR to read the inputs when the clock indicates
- Additionally, at times it might be necessary to clear or set the latch off of the clock
- Difference from flip-flop
  - The latch can output high (enabled) any time the clock is high
  - The flip-flop can output high only on the edge of the clock signal to allow for precise synchronization

## Flip-Flops

- Some memory elements react to the change of the clock
- They can be positive, or leading edge; or negative, or trailing edge, triggered
- A delay flip-flop, or D flip-flop, is an example of an edge triggered flip-flop
- Edge triggered has a triangle on the input

| C       | D        | $Q_n$     |
| ------- | -------- | --------- |
| 0       | $\times$ | $Q_{n-1}$ |
| 1       | $\times$ | $Q_{n-1}$ |
| $\uarr$ | 0        | 0         |
| $\uarr$ | 1        | 1         |

- The flip flop *samples* the input on *D* if *C* is rising

# Op-Amps

- Input resistance is infinity
- Output resistance is zero
- Voltage difference at input is greatly amplified by gain factor "A"

## Gains

- Open-loop voltage gain: $A_v = $ big number
- Closed-loop voltage gain: You design a gain to be what you want it to be ($\alpha R_{feedback} / R_{input}$) (proportional to is $\alpha$)
- Current gain is similar arrangement
- Power gain is the product of $A_V$ and $A_I$
- Saturation is normally less than the rail power because it takes power to run the op-amp internally. It can't output as much as it gets in.

## Configurations

1. Comparator:
   1. Op amp with no feedback
   2. Rails high when + input is greater than - input. Output is supply/rail maximum (saturated)
   3. Low output when - input is greater than the + input. Output is supply/rail minimum (zero or negative)
2. Amplifier
   1. Op-amp with feedback $Rf = $ some finite value ($Rf$ is the resistor that loops from $V_{out}$) to the - terminal
   2. Negative feedback now allows control of the gain

## Gains 2.0

- Gain A: open-loop gain. It is internal to the op-amp. It is fixed. You can't do much with just this beyond comparing
- Gain $A_v$: This is the closed-loop gain. It is external to the op-amp and its value is designed by the engineer. It makes the open-loop gain "invisible." Closed-loop gain is much more useful since it's a lot smaller than the open-loop gain.

## Rules

1. No current flows into the input pins
2. Through the use of negative feedback, the op-amp will ensure that both input voltages are equal. Therefore the input difference voltage equals zero.

![Op-Amp](http://emersondove.com/notes/Intro%20to%20ECE/Images/Op-Amp.png)

**Inverting op-amp equation**

$A_v = -\frac{R_f}{R_{in}}$

($R_f$ is the feedback capacitor, $R_{in}$ is the input capacitor)

**Noninverting equation**

$A_v = 1+\frac{R_b}{R_a}$

($R_b$ is the feedback capacitor, $R_{a}$ is the one that runs to ground)

## Voltage Follower

Voltage follower has the $V_{out}$ attached directly to the - input. This provides a lot of current gain.

### Summing Op-Amp

- Using an inverting op-amp, multiple voltages can be added.

![Op-Amp](http://emersondove.com/notes/Intro%20to%20ECE/Images/Summing_Op-Amp.png)

- $R_{in}$ can vary

## Differential Amplifier

![Op-Amp](http://emersondove.com/notes/Intro%20to%20ECE/Images/Difference_Op-Amp.png)

- If all resistors are equal then you get $v_0 = (v_2-v_1)$

