---
marp: true
math: katex
paginate: true
backgroundColor: #fff
title: Coherent Detction of FSK
categories:
  - Digital Communications
toc: true
toc_sticky: true
tags:
  - [FSK, Coherent Detection]

date: 2023-02-02
last_modified_at: 2023-02-03
---

## Set of FSK signal waveforms

$$
s_i(t)=\sqrt{2E\over{T}} \cos{(\omega_it+\phi)} \quad
\begin{split}
    0\leq t \leq T \\
    i=1,\cdots,M
\end{split}
$$

## Orthonormal set of the basis functions

$$
\Psi_j(t)=\sqrt{2\over{T}}\cos{\omega_jt}\quad j=1,\cdots,N
$$

---

### Prototype signal vector

* The **$i$th prototype signal vector** is located on **the $i$th coordinate axis** at **a displacement $\sqrt{E}$** from the origin of the signal space.

$$
a_ij=
\begin{cases}
    \sqrt{E} \quad \text{for} \quad i=j \\
    0 \qquad \text{otherwise}
\end{cases}
$$

### Distance between any two prototype signal vectors

$$
d(\mathbf{s}_i,\mathbf{s}_j)=\|\mathbf{s}_i-\mathbf{s}_j\|=\sqrt{2E} \quad \text{for} \quad i\neq j
$$
