---
marp: true
math: katex
paginate: true
backgroundColor: #fff
title: 4.5 Noncoherent Detection
categories:
  - Digital Communications
toc: true
toc_sticky: true
tags:
  - [Noncoherent Detection]
date: 2023-02-02
last_modified_at: 2023-02-02
---

## Noncoherent Detection of FSK

* The noncoherent detector typically requires **twice** as many channel branches as the coherent detector.
  * Quadrature receiver
  * Envelop detector

---

## Required Tone Spacing for Noncoherent Orthogonal FSK Signaling

> How can we tell if the tones in a signaling set form an orthogonal set?

---

### Minimum Tone Spacing and Bandwith

* Minimum tone spacing
* a mximum output
  * the peak of the sepctrum of tone 1 must coincide with one of the zero crossings of the spectrum of tone 2.

* bandwidth
  * It is related to the spectral spacing between the tones.
  * binary FSK
    * the signaling bandwidth is equal to the spectrum that separates the tone centers plus one-halt the tone spacing on each side of the set.
    * This amounts to to two times the tone spacing
  * M-ary FSK
    * $M/T$
