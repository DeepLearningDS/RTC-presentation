---
layout: side-title
side: l
color: amber-light
titlewidth: is-4
align: rm-lm
title: CNF
---

:: title ::

# Continuous Normalizing Flows

:: content ::

Let $\mathbb{R}^d$ the data space, data points $x = (x_1,\cdots,x_d) \in \mathbb{R}^d$.

Two important objects:
* a probability density path: $\textcolor{#92400e}{p:[0,1] \times \mathbb{R}^d \rightarrow \mathbb{R}_{>0}}$
* a time-dependent vector field: $\textcolor{#92400e}{v: [0,1] \times \mathbb{R}^d \rightarrow \mathbb{R}^d}$

A time-dependent diffeomorphic map, called a *flow*: $\textcolor{#92400e}{\phi: [0,1] \times \mathbb{R}^d \rightarrow \mathbb{R}^d}$

$$
\frac{d}{dt}\phi_t(x) = v_t(\phi_t(x)) \\

\phi_0(x) = x
$$

Modeling the vector field $v_t$ with a neural network, $v_t(x; \theta)$, where $\theta \in \mathbb{R}^p$  are its learnable parameters, which in turn leads to a deep parametric model of the flow $\phi_t$, called a **Continuous Normalizing Flow (CNF)**.

<div class="absolute bottom-4 text-sm font-extralight opacity-70">Yaron Lipman, Ricky TQ Chen, Heli Ben-Hamu, Maximilian Nickel, and Matt Le. Flow matching for generative modeling. arXiv preprint arXiv:2210.02747, 2022.</div>

<!--

:: note ::

<div class="fw-200" >

\* Yaron Lipman, Ricky TQ Chen, Heli Ben-Hamu, Maximilian Nickel, and Matt Le. Flow
matching for generative modeling. arXiv preprint arXiv:2210.02747, 2022.

</div>

-->

<!-- 


-->
