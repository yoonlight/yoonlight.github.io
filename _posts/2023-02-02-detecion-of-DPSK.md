---
marp: true
math: katex
paginate: true
backgroundColor: #fff
title: 4.5.1 Detection of DPSK
categories:
  - Digital Communications
toc: true
toc_sticky: true
tags:
  - [Noncoherent Detection, DPSK]
date: 2023-02-02
last_modified_at: 2023-02-03
---

## Detection of DPSK

* **Differential encoding**
  * The procedure of encodig the data **differentially**
  * The presence of a binary one or zero is manifested by **the symbols's similarity or difference** when compared with the preceding symbol

* **Differentially coherent detecion** of differentially encoded PSK (DPSK)
  * A detection scheme often **classified as noncoherent**
  * Because it does not require a reference in **phase with the received carrier**.

---

## Noncoherent systems

* No attempt is made to **determine the actual value of the phase** of the incoming signal.

* Transmitted waveform

$$
s_i(t)=\sqrt{2E\over{T}}\cos{[\omega_0t+\theta_i(t)]} \quad
\begin{split}
    0\leq t \leq T \\
    i=1,\cdots,M
\end{split}
$$

* Received signal

$$
r_i(t)=\sqrt{2E\over{T}}\cos{[\omega_0t+\theta_i(t)+\alpha]}+n(t) \quad
\begin{split}
    0\leq t \leq T \\
    i=1,\cdots,M
\end{split}
$$

---

## Noncoherent detection with matched filter

* It is impossible to use matched filter in noncoherent detection.
  * The matched filter output is a function of the unknown angle $\alpha$.
* Assumption
  * $\alpha$ vaires slowy relative to two period times ($2T$)
* The phase difference beween two successive waveforms is independent of $\alpha$.

$$
[\theta_k(T_2)+\alpha]-[\theta_j(T_1)+\alpha]=\theta_k(T_2)-\theta_j(T_1)=\Phi_i(T_2)
$$

---

## The basis for differentially coherent detection of DPSK

1. The carrier phase of the previous signaling interval can be used as a phase reference for demodulation
2. Its use requires differntial encoding of the message sequence at the transmitter.
3. To sent the $i$th message the present signal waveform must have its phase advanced by by $\phi_i=2\pi/M$ radians over the previous waveform.
4. The detector calculates the coordinates of the incoming signal by correlating it with locally generated waveforms.
5. The detector measures the angle between the currently received signal vector and the previously received signal vector.
