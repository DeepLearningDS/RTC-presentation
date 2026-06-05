---
layout: side-title
side: l
color: amber-light
titlewidth: is-1
align: rm-lm
title: Chunk
---

:: title ::

# Inpainting with Flow Matching

:: content ::

<div class="mt-10 flex flex-col items-center">
    <div class="text-base flex flex-wrap justify-center items-baseline gap-2 transition-all duration-500 [&_p]:m-0">
        <span class="transition-all duration-300" 
              :class="[$nav.clicks === 0 ? 'opacity-0' : ($nav.clicks === 1 || $nav.clicks >= 7 ? 'opacity-100' : 'opacity-25')]">
        
$\mathbf{v}_{\Pi\text{GDM}}(\mathbf{A}_t^\tau, \mathbf{o}_t, \tau) =$

</span>
        
<span class="transition-all duration-300 inline-block" :class="[$nav.clicks === 0 ? 'opacity-0' : ($nav.clicks === 2 ? 'text-[#92400e] font-bold scale-110 opacity-100' : ($nav.clicks === 1 || $nav.clicks >= 7 ? 'opacity-100' : 'opacity-25'))]">

$\mathbf{v}(\mathbf{A}_t^\tau, \mathbf{o}_t, \tau)$

</span>
        
<span class="transition-all duration-300" :class="[$nav.clicks === 0 ? 'opacity-0' : ($nav.clicks === 1 || $nav.clicks >= 7 ? 'opacity-100' : 'opacity-25')]">

$+$

</span>
        
<span class="transition-all duration-300 inline-block" :class="[$nav.clicks === 0 ? 'opacity-0' : ($nav.clicks === 5 ? 'text-[#92400e] font-bold scale-110 opacity-100' : ($nav.clicks === 1 || $nav.clicks >= 7 ? 'opacity-100' : 'opacity-25'))]">

$\min \left( \beta, \frac{1 - \tau}{\tau \cdot r_\tau^2} \right)$

</span>

<span class="transition-all duration-300 inline-block" :class="[$nav.clicks === 0 ? 'opacity-0' : ($nav.clicks === 3 ? 'text-[#92400e] font-bold scale-110 opacity-100' : ($nav.clicks === 1 || $nav.clicks >= 7 ? 'opacity-100' : 'opacity-25'))]">

$\left( \mathbf{Y} - \widehat{\mathbf{A}}_t^1 \right)^\top$

</span>

<span class="transition-all duration-300 inline-block" :class="[$nav.clicks === 0 ? 'opacity-0' : ($nav.clicks === 4 ? 'text-[#92400e] font-bold scale-110 opacity-100' : ($nav.clicks === 1 || $nav.clicks >= 7 ? 'opacity-100' : 'opacity-25'))]">

$\text{diag}(\mathbf{W})$

</span>

<span class="transition-all duration-300 inline-block" :class="[$nav.clicks === 0 ? 'opacity-0' : ($nav.clicks === 6 ? 'text-[#92400e] font-bold scale-110 opacity-100' : ($nav.clicks === 1 || $nav.clicks >= 7 ? 'opacity-100' : 'opacity-25'))]">

$\frac{\partial \widehat{\mathbf{A}}_t^1}{\partial \mathbf{A}_t^\tau}$

</span>

</div>

<div class="mt-16 w-full max-w-4xl h-48 relative [&_p]:m-0">

<div v-if="$nav.clicks >= 3" class="absolute inset-0 transition-all duration-500 flex justify-center" :class="$nav.clicks === 3 ? 'text-[#92400e] opacity-100' : ($nav.clicks >= 7 ? 'opacity-100' : 'opacity-25')">

$\text{where } \widehat{\mathbf{A}}_t^1 = \mathbf{A}_t^\tau + (1 - \tau)\mathbf{v}(\mathbf{A}_t^\tau, \mathbf{o}_t, \tau)$

</div>

<div v-if="$nav.clicks >= 4" class="absolute inset-0 transition-all duration-500 flex justify-center" :class="$nav.clicks === 4 ? 'text-[#92400e] opacity-100 mt-10' : ($nav.clicks >= 7 ? 'opacity-100 mt-10' : 'opacity-25 mt-10')">

$\mathbf{W}_i = \begin{cases} 1 & \text{if } i \lt d \\ c_i \frac{e^{c_i}-1}{e-1} & \text{if } d \leq i \lt H - s \\ 0 & \text{if } i \geq H - s \end{cases} \quad , \quad c_i = \frac{H - s - i}{H - s - d + 1}, \ i \in \{0, \dots, H - 1\}$

</div>

<div v-if="$nav.clicks >= 5" class="absolute inset-0 transition-all duration-500 flex justify-center" :class="$nav.clicks === 5 ? 'text-[#92400e] opacity-100 mt-36' : ($nav.clicks >= 7 ? 'opacity-100 mt-36' : 'opacity-25 mt-36')">

$r_\tau^2 = \frac{(1 - \tau)^2}{\tau^2 + (1 - \tau)^2}$

</div>

</div>

</div>

<v-clicks :at="1">
    <div v-for="i in 7" :key="i" class="hidden"></div>
</v-clicks>

