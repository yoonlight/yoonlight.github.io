---
marp: true
math: katex
paginate: true
backgroundColor: #fff
title: 4.8 M-ary Signaling and Performance
categories:
  - Digital Communications
toc: true
toc_sticky: true
tags:
  - [M-ary, Signaling, Performance]
date: 2023-02-03
last_modified_at: 2023-02-03
---

## Ideal Probability of Bit Error Performance

---

## Vectorial View of MPSK Signaling

### Vectorial View of MPSK signal sets' insight

* why the curves behave as they do as $k$ is increased.
  * the curves: bit error probability for coherently detected multiple phase signaling
* a basic trade-off in multiple phase signaling
  * we have increased the bandwidth utilization at the expense of error performance

---

### Summary

* As $M$ is increased
  * we can achieve improved bandwidth performance at the expoense of error performance.
  * If we increase the $E_b/N_0$ so that the error probability is not degraded, we can achieve improved bandwidth performance at the expense of increasing $E_b/N_0$.

---

## BPSK and QPSK Have the Same Bit Error Probability

* The natural orthogonality of the $90\degree$ phase shifts between adjacent QPSK symbols results in the bit error probabilities being equal for both BPSK and QPSK signaling.
  * BPSK signlaing
  * QPSK signaling
  * 여기 이해 필요함

$$
{E_b\over{N_0}}={S/2\over{N_0}}({W\over{R/2}})={S\over{N_0}}({W\over{R}})
$$

* ${S/2\over{N_0}}({W\over{R/2}})$ : Orthogonal BASK's bit error probability
* ${S\over{N_0}}({W\over{R}})$ : BPSK's bit error probability

---

## Vectorial View of MFSK Signaling

---

### Unnormalized SNR

---

### Mapping relationship between unnormalized and normalized SNR

$$
\begin{split}
    {E_b\over{N_0}}&={S\over{N}}({W\over{R}})\\
    &={S\over{N}}({WT\over{\log_2M}})={S\over{N}}({WT\over{k}})\\
    &\approx{S\over{N}}({1\over{k}})
\end{split}
$$

* $R={\log_2M\over{T}}={k\over{T}}$
* $WT\approx1$

---

### Unnormalized SNR insight

> Why orthogonal signling provides improved error performance as $M$ or $k$ increases.

* When we use orthogonal signaling with symbols that contain more bits, we need more power (more SNR), but the requirement per bit ($E_b/N_0$) is reduced.
