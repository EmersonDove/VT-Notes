---
title: Exam 1
position: 1
category: ECE 2024 - Circuits & Devices
---

## Thevenin

$R_t = \frac{v_{oc}}{i_{sc}}$

## RL Circuits

### Time Constants

$\tau = RC$ is the time constant of an RC circuit and it is the time it takes the voltage magnitude to drop to $36.8\%$ of its initial value

$\tau = \frac{L}{R}$ is the time constant of an RL circuit and it is the time it takes the current magnitude to drop to $36.8\%$ of its initial value

## General Charging Formulas

### Capacitor

$v_c(t) = V_s+ (v_c(0^+) - V_s)e^{\frac{-1}{RC}t}$

### Inductor

$i_L (t) = \frac{V_s}{R} + (i_L(0^-) - \frac{V_s}{R})e^{\frac{-R}{L}t}$

## RLC Circuits

Parallel Damping: $\iota = \frac{\frac{1}{2RC}}{\frac{1}{\sqrt{LC}}}$

Series Damping: $\iota = \frac{\frac{R}{2L}}{\frac{1}{\sqrt{LC}}}$

Undamped Resonant Frequency for Both: $\omega_0 = \frac{1}{\sqrt{LC}}$

Damped Resonant Frequency (use in imaginary case): $\omega_d=\sqrt{\frac{1}{LC} - (\frac{R}{2L})^2}$ or $\sqrt{\omega_0 ^2 - \alpha ^2}$

Damping factor/coefficient series: $\alpha = \frac{R}{2L}$

Damping factor/coefficient parallel: $\alpha = \frac{1}{2RC}$

| Term                                     | RLC Series                                                   | RLC Parallel                                                 |
| ---------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| $\alpha$                                 | $\frac{R}{2L}$                                               | $\alpha = \frac{1}{2RC}$                                     |
| $\omega_0$ - Undamped Resonant Frequency | $\frac{1}{\sqrt{LC}}$                                        | $\frac{1}{\sqrt{LC}}$                                        |
| $\iota$                                  | $\frac{\alpha}{\omega_0}=\frac{\frac{R}{2L}}{\frac{1}{\sqrt{LC}}}$ | $\frac{\alpha}{\omega_0}=\frac{\frac{1}{2RC}}{\frac{1}{\sqrt{LC}}}$ |

| Term                        | Equation                                                     |
| --------------------------- | ------------------------------------------------------------ |
| $x(t)$ - Overdamped         | $x_s(\infin) + e^{-\alpha t}(K_1e^{t\sqrt{\alpha^2 - \omega_0^2}} +K_2 e^{-t \sqrt{\alpha^2 - \omega_0 ^2}})$ |
| $x(t)$ - Critically Damped  | $x_s(\infin)+e^{-\alpha t} (K_1t+K_2)$                       |
| $x(t)$ - Underdamped Damped | $x_s(\infin) + e^{-\alpha t} (K_1 \cos(\omega_d t) + K_2 \sin(\omega_d t))$ |

$\frac{dv_c(0^+)}{dt}$ for a pure parallel circuit with just current source, resistor, inductor and capacitor all in parallel: $\frac{dv_c(0^+)}{dt} = \frac{1}{C}(I_S(0^+) - \frac{v_c (0^-)}{R}-i_L(0^-))$

$\frac{di_L(0^+)}{dt}$ for a pure parallel circuit with just current source, resistor, inductor and capacitor all in parallel: $ \frac{di_L(0^+)}{dt}= \frac{1}{L} v_c(0^-)$



$\frac{di_l(0^+)}{dt}$ for a pure series circuit with just current source, resistor, inductor and capacitor all in series: $ \frac{di_l(0^+)}{dt}= \frac{1}{L}(V_s(0^+) - I_L(0^-)R - V_C(0^-))$