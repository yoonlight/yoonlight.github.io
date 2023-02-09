---
marp: true
math: katex
paginate: true
backgroundColor: #fff
title: 4.6 Complex Envelope
categories:
  - Digital Communications
toc: true
toc_sticky: true
tags:
  - [Complex Exnvelope]
date: 2023-02-02
last_modified_at: 2023-02-02
---

## Real bandpass waveform

$$
\begin{split}
s(t) & =Re{g(t)e^{j\omega_0t}} \\
& = Re\{[x(t)+jy(t)][\cos{\omega_0t}+j\sin{\omega_0t}]\} \\
& = x(t)\cos{\omega_0t}-y(t)j\sin{\omega_0t}
\end{split}
$$

## Complex envelope

$$
g(t)=x(t)+jy(t)=|g(t)|e^{j\theta(t)}=R(t)e^{j\theta(t)}
$$

---

## 4.6.1 Quadrature Implementation of a Modulator
