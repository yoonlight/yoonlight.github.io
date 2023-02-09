---
marp: true
math: katex
paginate: true
backgroundColor: #fff
# theme: gaia
title: Coherent Detection
categories:
  - Digital Communications
tags:
  - [Coherent Detection]
toc: true
toc_sticky: true
date: 2023-02-01
last_modified_at: 2023-02-03
---

## 4.4.1 Coherent Detection of PSK

### BPSK

$$
\begin{align*}
s_1(t)=\sqrt{2E\over{T}}\cos{(\omega_0t+\phi)}\quad0\leq t \leq T \\
\begin{split}
s_2(t)&=\sqrt{2E\over{T}}\cos{(\omega_0t+\phi+\pi)} \\
&=-\sqrt{2E\over{T}}\cos{(\omega_0t+\phi)}\quad0\leq t \leq T
\end{split}
\end{align*}
$$

* $\phi$ : an arbitary constant
* $E$ : signal energy per symbol
* $T$ : symbol duration

---

### Antipodal case

* basis function

$$
\psi_1(t)=\sqrt{2\over{T}}\cos{\omega_0t}\quad\text{for}\quad0\leq t\leq T
$$

* the transmitted signals

$$
\begin{align*}
s_i(t)=a_{i1}\psi_1(t)\\
s_1(t)=a_{11}\psi_1(t)=\sqrt{E}\psi_1(t)\\
s_2(t)=a_{21}\psi_1(t)=-\sqrt{E}\psi_2(t)
\end{align*}
$$

---

## 4.4.2 Sampled Matched Filter

---

## 4.4.3 Coherent Detection of Multiple Phase-Shift Keying (MPSK)

> Multiple Phase-Shift Keying (MPSK)

---

### Typical coherent M-ary PSK

$$
s_i(t)=\sqrt{2E\over{T}}\cos{({\omega_ot-2\pi i\over{M}})}\quad
\begin{split}
    \begin{align*}
        0\leq t \leq T\\
        i=1,\cdots,M
    \end{align*}
\end{split}
$$

---

#### Orthonormal signal space

$$
\psi_1(t)=\sqrt{2\over{T}}\cos{\omega_0t}\\
\psi_2(t)=\sqrt{2\over{T}}\sin{\omega_0t}
$$

---

#### Waveform set

$$
\begin{align*}
    \begin{split}
    s_i(t) & = a_{i1}\psi_1(t)+a_{i2}\psi_2(t)\quad
        \begin{split}
            \begin{align*}
                0\leq t\leq T\\
                i=1,\cdots,M
            \end{align*}
        \end{split}\\
    & = \sqrt{E}\cos{({2\pi i\over{M}})}\psi_1(t)+\sqrt{E}\sin{({2\pi i \over{M}})\psi_2(t)}
    \end{split}
\end{align*}
$$

#### Received Signal

$$
r(t)=\sqrt{2E\over{T}}{(\cos{\phi_i}\cos{\omega_0t}+\sin{\phi_i}\sin{\omega_0t})}+n(t)\quad
\begin{split}
0\leq t \leq T \\
i=1,\cdots,M
\end{split}
$$
