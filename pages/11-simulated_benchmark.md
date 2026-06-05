---
layout: top-title
color: amber-light
align: l
title: q1q2
---
:: title ::
<div class="flex items-stretch h-full gap-4">
<div class="flex flex-col justify-center gap-3">
<div class="flex items-center gap-2">
<div class="w-[22px] h-[22px] rounded-full border-2 border-amber-500 bg-white dark:bg-gray-900 flex items-center justify-center text-xs font-bold text-amber-600 shrink-0">1</div>
<span class="text-sm font-semibold">Performance under delay</span>
</div>
<div class="flex items-center gap-2">
<div class="w-[22px] h-[22px] rounded-full border-2 border-amber-500 bg-white dark:bg-gray-900 flex items-center justify-center text-xs font-bold text-amber-600 shrink-0">2</div>
<span class="text-sm font-semibold">Importance of soft masking</span>
</div>
</div>
<div class="w-[2px] bg-white/40 self-stretch mx-1"></div>
<div class="flex items-center justify-center text-sm font-semibold text-white/90 text-center px-2">Simulated<br>Benchmark</div>
</div>

:: content ::

<div class="grid grid-cols-2 gap-8 items-start mt-4 relative">

<!-- LEFT -->
<div class="relative z-40">
<p class="text-gray-700 dark:text-gray-300 text-lg mb-4">
<strong class="text-[#92400e]">
<span v-if="$clicks < 1">Setup</span>
<span v-else>Results</span>
</strong>
</p>
<div class="grid relative">

<!-- SETUP cards -->
<div class="col-start-1 row-start-1 transition-opacity duration-500"
:class="$clicks >= 1 ? 'opacity-0 pointer-events-none' : 'opacity-100'">
<div class="grid grid-cols-2 gap-2 text-sm">
<div class="rounded-xl bg-gray-800/60 px-3 py-2">
<p class="text-[9px] text-gray-400 uppercase tracking-wide">Policy</p>
<p class="text-sm font-bold mt-1">Flow Matching</p>
<p class="text-xs text-gray-400">MLP-Mixer, 4 layers</p>
</div>
<div class="rounded-xl bg-gray-800/60 px-3 py-2">
<p class="text-[9px] text-gray-400 uppercase tracking-wide">Dataset</p>
<p class="text-sm font-bold mt-1">1M transitions</p>
<p class="text-xs text-gray-400">6 seeds × 12 envs</p>
</div>
<div class="rounded-xl bg-gray-800/60 px-3 py-2">
<p class="text-[9px] text-gray-400 uppercase tracking-wide">Horizon H</p>
<p class="text-2xl font-bold mt-1 text-amber-400">8</p>
</div>
<div class="rounded-xl bg-gray-800/60 px-3 py-2">
<p class="text-[9px] text-gray-400 uppercase tracking-wide">Delay d</p>
<p class="text-2xl font-bold mt-1 text-amber-400">0 → 4</p>
</div>
<div class="rounded-xl bg-gray-800/60 px-3 py-2 col-span-2">
<p class="text-[9px] text-gray-400 uppercase tracking-wide">Metric</p>
<p class="text-sm font-bold mt-1">Binary Solve Rate</p>
<p class="text-xs text-gray-400">2048 rollouts per point</p>
</div>
</div>
</div>

<!-- FIGURE 5 -->
<div class="col-start-1 row-start-1 flex flex-col items-center transition-all duration-700 ease-[cubic-bezier(0.25,1,0.5,1)] origin-left"
:class="[
$clicks < 1 ? 'opacity-0 pointer-events-none' : 'opacity-100',
$clicks === 2 ? 'scale-[1.35] z-50' : 'scale-100 z-20'
]">
<img :src="'/img/figure5.png'"
class="w-full object-contain rounded-xl border border-gray-200 dark:border-gray-700 transition-shadow duration-700"
:class="$clicks === 2 ? 'shadow-2xl' : 'shadow-lg'"/>
<p class="mt-2 text-xs text-center text-gray-400 italic">Fig. 5 — Black et al. (2025)</p>
</div>

</div>
</div>

<!-- RIGHT: video with spacer for alignment -->
<div class="w-full relative z-10 transition-opacity duration-700"
:class="$clicks === 2 ? 'opacity-25' : 'opacity-100'">
<p class="text-transparent text-lg mb-4 pointer-events-none select-none" aria-hidden="true">
<strong>Spacer</strong>
</p>
<video :src="'/animation/combined_wide11.mp4'" autoplay loop muted playsinline
class="w-7.1/8 rounded-xl shadow-lg border border-gray-200 dark:border-gray-700"/>
<p class="mt-2 text-xs text-center text-gray-400 italic">Kinetix — 12 dynamic tasks</p>
</div>

</div>

<div class="hidden">
<span v-click="1"></span>
<span v-click="2"></span>
<span v-click="3"></span>
</div>