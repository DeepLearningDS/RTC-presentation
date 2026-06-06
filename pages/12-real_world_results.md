---
layout: top-title
color: amber-light
titlewidth: is-4
align: l
title: Real-world results
---

:: title ::

<div class="relative flex items-center gap-4">
  <div class="w-14 h-14 rounded-full border-[3px] border-amber-500 bg-white dark:bg-gray-900 shrink-0 z-10 flex items-center justify-center text-2xl font-bold text-amber-600">
    3
  </div>
  
  <h1 class="!m-0 leading-none border-none">
    Real-world impact
  </h1>
</div>

:: content ::

<div class="grid grid-cols-2 gap-8 items-start mt-10 relative">

<div class="relative z-40">

<p class="text-gray-700 dark:text-gray-300 text-lg mb-4">
<strong class="text-[#92400e]">
<span v-if="$clicks < 5">Setup</span>
<span v-else>Benchmark</span>
</strong>
</p>

<div class="grid relative">

<div class="col-start-1 row-start-1 transition-opacity duration-500" 
:class="$clicks >= 5 ? 'opacity-0 pointer-events-none' : 'opacity-100'">
<ul class="list-disc list-inside text-gray-700 dark:text-gray-300 space-y-2">
<li v-click="1">
<div class="alg-code indent-1 [&_p]:inline [&_p]:m-0">
<strong class="text-[#92400e]">Model:</strong> policy 

<Rough type="circle" color="#92400e" :show="$nav.clicks >= 2" class="relative">

$\pi_{0.5}$ 

</Rough>

$(H = 50, \Delta t = 20\text{ms})$ with $n = 5$ denoising steps.

</div>
</li>

<li v-click="3">
<div class="alg-code indent-1 [&_p]:inline [&_p]:m-0">
<strong class="text-[#92400e]">Initial latency:</strong> 76ms (baseline) vs 97ms (RTC) + 10-20ms of LAN network overhead 

$(d \approx 6)$ for RTC.

</div>
</li>

<li v-click="4">
<div class="alg-code indent-1 [&_p]:inline [&_p]:m-0">
<strong class="text-[#92400e]">Stress Test:</strong> injected latency of +100ms 

$(d \approx 11)$ and +200ms $(d \approx 16)$ to simulate remote cloud servers or scaled models.

</div>
</li>
</ul>
</div>

<div class="col-start-1 row-start-1 flex flex-col items-center transition-all duration-700 ease-[cubic-bezier(0.25,1,0.5,1)] origin-left"
:class="[
$clicks < 5 ? 'opacity-0 pointer-events-none' : 'opacity-100',
$clicks === 6 ? 'scale-[1.35] z-50' : 'scale-100 z-20'
]">
<img 
src="../public/img/results.png" 
alt="Grafico benchmark" 
class="w-full aspect-video object-cover rounded-xl border border-gray-200 dark:border-gray-700 transition-shadow duration-700"
:class="$clicks === 6 ? 'shadow-2xl' : 'shadow-lg'"
/>
<p class="mt-2 text-xs text-center text-gray-400 italic">Fig. 4 — Black et al. (2025)</p>
</div>

</div>
</div>

<div class="w-full relative z-10 transition-opacity duration-700" 
:class="$clicks === 6 ? 'opacity-25' : 'opacity-100'">

<p class="text-transparent text-lg mb-4 pointer-events-none select-none" aria-hidden="true">
<strong>Spacer</strong>
</p>

<video src="https://website.pi-asset.com/real_time_chunking/sizzle.mp4" autoplay loop muted playsinline class="w-full rounded-xl shadow-lg border border-gray-200 dark:border-gray-700"></video>
</div>

</div>

<div class="hidden">
<span v-click="5"></span>
<span v-click="6"></span>
<span v-click="7"></span>
</div>