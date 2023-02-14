---
# MARP
marp: true
math: katex
paginate: true
backgroundColor: #fff
# Jekyll
title: Information Theory
description: 2023 디지털 통신 및 최신 네트워크 기술 단기 강좌
categories:
  - Digital Communications
toc: true
toc_sticky: true
tags:
  - [Information Theory]
date: 2023-02-14
last_modified_at: 2023-02-14
published: false
---

## Introduction

1. What is the ultimate data compression? the entroy $H$
2. What is the ultimate transmission rate of communication? the channel capacity $C$

---

<!-- footer: Entropy, Mutual Information -->
## Entropy, Mutual Information

### Entropy

- a measure of uncetainty of a random variable
- physical meaning: the average amount of information per source output

---

#### Class

- Joint entropy
- Conditional entropy
  - Chain rule
- Relative entropy (Kullback Leibler distance)
  - A measure of the distance between two distributions
  - Conditional relative entropy
    - $D(p(y|x)||q(y|x))=E_p(x,y)\log{p(Y|X)\over{q(Y|X)}}$
  - Chain rule

---

### Mutual Information

- A measure of amount of information that one r.v. contains about another r.v.

- The reduction in the uncertainty of one r.v. due to the knowledge of the other

$$
I(X;Y)\triangleq H(X)-H(X|Y)
$$

$$
I(X;Y)=D(p(x,y)||p(x)p(y))
$$

- $p(x,y)$: true
- $p(x)p(y)$: assume (X,Y independent)

---

- Jensen's inequality
  - IF $f$ is a convex function and $X$ is a r.v., then
    - $Ef(X)\geq f(EX)$
- Markov chain
  - Markove chain $X\rightarrow Y\rightarrow Z$ if
  - $p(x,y,z)=p(x)p(y|x)p(z|y)$
- Data processing inequality
  - $\text{If }X\rightarrow Y\rightarrow Z,\text{then } I(X;Y)\geq I(X;Z)$
- Fano's inequality (bound on $P_e$)
  - Let $P_e=\text{Pr}\{\hat{X}\neq X\}$
  - $H(P_e)+P_e\log{|\mathcal{X}|-1}\geq H(X|Y)$

---
<!-- footer: Asymptotic Equipartition Property (AEP) -->
## Asymptotic Equipartition Property (AEP)

---
<!-- footer: Channel Capacity -->
## Channel Capacity

the capacity of the channel: the maximum rate

Information channel capacity of discrete memoryless channel (DMC)

$$
C=\max_{p(x)}{I(X;Y)}
$$

---

### Example

- Noiseless binary channel
- Binary symmetric channel
- Binary erasure channel

---

### Channel Coding Theorem (Shannon)

- All rates below capacity $C$ are achievable
- For every rate $R<C$, there exists a sequence of $(2^nR,n)$ codes with maximum probability of error $\lambda^{(n)}\rightarrow 0$

---
<!-- footer: Differential Entropy -->
## Differential Entropy

---
<!-- footer: Gaussian Channel -->
## Gaussian Channel

The information cpacity with power constraint $P$

$$
C={1\over{2}}\log{\left(1+P\over{N}\right)}
$$

- Information Channel Capacity

$$
C=\max_{f(x_1,x_2,\cdots,x_k):\sum{E[X^2_t]\leq P}}I(X_1,X_2,\cdots,X_k;Y_1,Y_2,\cdots,Y_k)
$$

- Optimization problem

$$
J(P_1,P_2,\cdots,P_k)=\sum_i{{1\over{2}}\log{\left(1+{P_i\over{N_i}}\right)}}+\lambda\left(\sum_i{P_i}\right)
$$

---

- Channel Capacity

$$
C=\sum_{i=1}{1\over{2}}\log{\left(1+{P^*_i\over{N}}\right)}
$$

- For complex baseband AWGN channel

  - Capacity

$$
C={1\over{2}}\log{\left(1+{P\over{N}}\right)}\quad\text{[bits/real dimension]} \\
C=\log{\left(1+{P\over{N}}\right)}\quad\text{[bits/complex dimension]}
$$
