---
layout: side-title
side: l
color: amber-light
titlewidth: is-4
align: rm-lm
title: Chunk
---

:: title ::

# How do you create a chunk?

:: content ::

<div v-click class="transition-opacity duration-500">

$$
A_t^{\tau+\frac{1}{n}} = A_t^\tau + \frac{1}{n}v_{\pi}(A_t^\tau, o_t, \tau)
$$

* a random noise $A^0_t$
* the **flow’s velocity field** $v_\pi$
* $\tau \in [0,1)$ denotes a flow matching timestep
* $n$ determines the number of denoising steps

</div>

