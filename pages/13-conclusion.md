---
layout: section
color: amber-light
---
# Strengths & Limitations

---
layout: top-title
color: amber-light
align: l
title: strengths-limitations
---
:: title ::
# Strengths & Limitations

:: content ::

<div style="display:grid; grid-template-columns: 1fr 1fr; gap: 2rem; margin-top: 1rem;">

<div>
<div v-click class="transition-opacity duration-500">
<p class="text-sm font-bold mb-3" style="color: #92400e;">Strengths</p>

* **No retraining**: it's plug-and-play, can be applied on any pretrained diffusion/flow-based VLA
* **Robust to latency**: it works up to 300ms+ of delay, where all other methods fail
* **Faster and more precise**: it's 20% faster than synchronous, fewer errors and retries

</div>
</div>

<div>
<div v-click class="transition-opacity duration-500">
<p class="text-sm font-bold mb-3" style="color: #92400e;">Limitations</p>

* **Diffusion/flow only**: cannot applicable to autoregressive token-based VLAs
* **n = 5**: the choice of denoising steps is never explicitly justified
* $d = \max(Q)$ in the **Inference Loop** can lead to problems when the estimated delay is far from the effective delay

</div>
</div>

</div>





