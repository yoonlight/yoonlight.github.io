---
marp: true
math: katex
# theme: uncover
theme: marp-custom
paginate: true
title: Optimization Theorem
description: Optimization Theorem
categories:
  - Digital Communications
toc: true
toc_sticky: true
tags:
  - [Optimization Theorem]
date: 2023-02-13
last_modified_at: 2023-02-13
published: false
---
<!--
paginate: false
 -->
# Optimization Theorem

---
<!--
paginate: true
 -->
### Supporting Hyperplance Theorem

If C is convex, then there exits a supporting hyperplane at every boundary point of C

---
<!--
footer: Convex Functions
 -->
## Convex Functions

- Jensen inequality

$$
f(\theta x+(1-\theta)u)\leq\theta f(x)+(1-\theta)f(y)
$$

- f is **concave** if $-f$ is convex

- convex function <-> epi graph (convex set)

---
<!--
header: helloe
-->
### Examples of Convex and Concave Functions

- Every norm on $\mathbb{R}^n$ is convex

---

### Jensen's inequality

$$
f(\theta x+(1-\theta)y)\leq \theta f(x)+(1-\theta)f(y)
$$

$$
f(\mathbb{E}z)\leq \mathbb{E}f(z)
$$

---
<!--
header: ""
footer: ""
 -->

## Convex Optimization Problem

---
<!--
footer: Convex Optimization Problem
 -->

### Optimization Problem in Standard Form

minimize $f_0(x)$
$$
\begin{split}
    \text{subject to } &f_i(x)\leq 0, i=1,2,\cdots,m\\
    &h_i(x)=0, i=1,2,\cdots,p
\end{split}
$$

---

### Standard Form Convex Optimization Problem

minimize $f_0(x)$
subject to $f_i(x)\leq 0, i=1,2,\cdots,m$

---

### Optimization Criterion for Differentiable $f_0$

$$
\nabla f_0(x)^T(y-x)\geq 0 \quad\text{for all feasible } y
$$

---

### Optimizatio Criterion

#### unconstrained problem

$x$ is optimal if and only if

$$
x \in\text{dom }f_0,\nabla f_0(x)=0
$$

#### equality constraint problem

minimize $f_0(x)$ subject to $A_x=b$

---
<!--
footer: ""
paginate: false
 -->
## Duality and Lagrange Multiplier

---

<!--
footer: Duality and Lagrange Multiplier
paginate: true
 -->

### Concept of Lagrangian Duality

---

### Lagrangian

- standard form problem

---

### Inequality Form LP

- prime problem
- dual function

---

### Saddle Point Interpretation

---

### Karush-Kuhn-Tucker (KKT) Conditions

- primal constraints: $f_i(x)\leq0, i=1,\cdots,m,h_i(x)=0,i=1,\cdots,p$
- dual constrains: $\lambda\geq0$
- complementary slackness: $\lambda_if_i(x)=0,i=1,\cdots,m$
- gradient of Lagrandian with respect to $x$ vanishes

$$
\nabla f_0(x)+\sum^m_{i=1}\lambda_i \nabla f_i(x)+\sum^p_{i=1}\nu_i\nabla h_i(x)=0
$$

---
<!--
footer: ""
 -->
## Proximal Methods

---
<!--
footer: Proximal Methods
 -->

### Regularized Minimization

---

### Alternating Direction Method of Multipliers (ADMM)

minimize $f(x)+g(x)$
subject to $Ax+Bz=c$

- Augmented Lagrangian

$$
L_\rho(x,z,y)=f(x)+g(y)+y^T(Ax+Bz-c)+(\rho/2)||Ax+Bz-||^2_2
$$

---

### LASSO

---

## Applications

1. Key Ideas of Compressive Sensing
