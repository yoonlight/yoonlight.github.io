---
# MARP
marp: true
math: katex
paginate: true
backgroundColor: #fff
# Jekyll
title: Error Correcting Coding
description: 2023 디지털 통신 및 최신 네트워크 기술 단기 강좌
categories:
  - Digital Communications
toc: true
toc_sticky: true
tags:
  - [Error Correcting Coding]
date: 2023-02-14
last_modified_at: 2023-02-14
published: false
---

## Channel Capacity, Shannon Limit, and Coding

---

<!-- footer: Channel Capacity, Shannon Limit, and Coding -->

### Communication System Model

---

### Communication Problem

- channel impariments corrupt transmitted data
- Shannon
  - Reiability can be achieved in sipte of impaired transmission

---

### Channel Coding Theorem

- Channel capacity
- Channel coding theorem
- Converse

---

### Channel Capacity

- Entropy
- Conditional entropy
- Mutual Information
- Definition (mathmetical)

$$
C=\max_{p(x)}I(X;Y)
$$

- Operational definition
  - Maximum data rate with vanishing error rate via a given commuinication channel

---

<!-- header: Channel Capacity -->

- Noiseless binary channel
- Binary symmetric channel (BSC)
- Binary erasure channel (BEC)
- AWGN Channel
  - Gaussian channel capacity
    - Discrete time real channel: $C={1\over{2}}\log{\left(1+{P\over{P_N}}\right)}$
    - Discrete time complex channel: $C=\log{\left(1+{P\over{P_N}}\right)}$
    - Band-limited contiuous time channel: $C=W\log{\left(1+{P\over{P_N}}\right)}$

---
<!-- header: AWGN Channel and Shannon Limit -->
### AWGN Channel and Shannon Limit

- SNR: total signal power $P$ to inband noise power ratio
- $W$: Bandwidth
- $2W$: Nyquist (ISI free) symbol rate
- $R$: Data rate
- $r=R/2W$: Rate per symbol
- $\eta=R/W$: Spectral efficiency
- $\eta=2r$: Nominal spectral efficiency

---
<!-- header: The Shannon Limit -->
### The Shannon Limit

- For a given spectral efficiency $\eta=\log{(1+SNR)}$

$$
\text{Shannon Limit}={SNR}_{Shannon}=2^{\eta}-1
$$

- Normalized SNR

$$
{SNR}_{norm}={SNR\over{2^\eta-1}}
$$

- $E_B/N_0$

$$
{E_b\over{N_0}}={2^\eta-1\over{\eta}}{SNR}_{norm}
$$

- For a given $\eta$

$$
{E_b\over{N_0}}>{2^\eta-1\over{\eta}}(>\ln{2}=-1.59dB)
$$

---

### Goals of Channel Coding

- to achieve capacity $C$ with low error probability
  - to lower the error rate for a given code rate
  - to achive a target error rate at a smaller SNR
  - to have coding schemes that can adapt well a variety of channel states

### Channel Coding Techinques

- **Forward Error Correction (FEC)**
  - error correcting codes
- Error detection: Cyclic Redundnacy Check (CRC)
- Automatic Repeat reQuest (ARQ)
- Hybrid Automatic Repeat reQuest (HARQ)

---

<!-- footer: Block Codes and Their Properties -->
## Block Codes and Their Properties

---

### Maximum A Posteriori Probability Decoding

### Maximum Likelihood Decoding

$$
\hat{\mathbf{c}}=\arg\max_{\mathbf{c}\in C}{P(\mathbf{r}|\mathbf{c})}
$$

$$
P(\mathbf{r}|\mathbf{v})=\prod_i{P(r_i|v_i)}
$$

---

### Min Distance Decoding as Optimal Decoding

$$
\hat{\mathbf{c}}=\arg\min_{\mathbf{c}\in C}d_h(\mathbf{c},\mathbf{r})(=\argmax_{\mathbf{c}\in C}P(\mathbf{r}|\mathbf{c}))
$$

---

### Block Codes: Error Correction Capability

$$
d_{\text{min}}\geq s+t+1
$$

- $s$: number of errors in detectable error patterns
- $t$: number of errors in correctable error patterns

---

<!-- header: Block Codes: Error Correction Capability -->

- Error correction capability

$$
t=\left\lfloor {d-1\over{2}}\right\rfloor
$$

---
<!-- footer: Linear Block Codes -->
<!-- header: "" -->
## Linear Block Codes

---

- Linear combination

$$
\begin{split}
\mathbf{c}
&=m_0\mathbf{g}_0+m_1\mathbf{g}_1+\cdots+m_{k-1}\mathbf{g}_{k-1}\\
&=(m_1,m_1,\cdots,m_{k-1})
  \left[
    \begin{matrix}
      \mathbf{g}_0\\
      \mathbf{g}_1\\
      \vdots\\
      \mathbf{g}_{k-1}
    \end{matrix}
  \right]\\
&=\mathbf{mG}
\end{split}
$$

---

### Parity Check Matrix

- $[n,k]$ systematic linear block code $C$

$$
\mathbf{G}=[\mathbf{I_KP}]
$$

---

### Decoding with PCM

- Received word
- Syndrome
- Decision (decoding) based on syndromes

---
<!-- footer: Cyclic Codes -->
## Cyclic Codes

---
<!-- header: Poylnomical Codes -->
- Polynomial Codes

- Definition
- A polynomial code is cyclic iff $g(x)$ divides $x^n-1$

- Systematic Encoding of Cyclic Codes
- Syndrome of Cyclic Codes
- Design of Cyclic Codes: BCH Codes
  - a large class of parameterized binary (or nonbinary) multiple error correcting
  - features
    - cyclic codes, syndrome decoding
    - ease of implementation

---
<!-- header: "" -->
<!-- footer: Convolutional Codes and Their Properties -->
## Convolutional Codes and Their Properties

---

### Encoder of Convolutional Codes

- $(n,k,m)$ convolutional code with code rate $R=k/n$
  - $n$: # of codeword symbols at a time
  - $k$: # of information symbols at a time
  - $m$: memory size of convolutional codes

---

### Encoder

- Encoder
- Generator polynomial

---

### Vector and Polynomial Notation

### State Diagram

### Trellis Diagram

---

### Free Distance

---

### Convolutional Codes in Concatenated Coding
