---
layout: section
color: amber-light
---

# Methodology

---
layout: side-title
side: l
color: amber-light
titlewidth: is-3
align: rm-lm
title: experiments
---

:: title ::
# Inpainting Problem
:: content ::
<div class="flex flex-col gap-3">
<p class="text-sm">
The key insight: <strong>real-time chunking is an inpainting problem</strong>, so the same mathematics that fills in missing pixels can fill in missing actions.
</p>
<div
:class="$clicks === 3 ? 'grid-cols-1 justify-items-center' : 'grid-cols-2'"
class="grid gap-4 items-start transition-all duration-500">
<div v-click
:class="$clicks === 3 ? 'opacity-0 h-0 overflow-hidden' : 'opacity-100'"
class="flex flex-col gap-1 items-center transition-all duration-500">
<p class="text-xs font-semibold text-center text-gray-500 uppercase tracking-wide">Image inpainting</p>
<img :src="'/img/inpainting.png'" class="w-3/4 max-h-40 object-contain rounded-lg"/>
<p class="text-xs text-center text-gray-400 italic">Fig. 1(c) — Pokle et al. [48]</p>
</div>
<div v-click
:class="$clicks === 3 ? 'w-full' : ''"
class="flex flex-col gap-1 items-center transition-all duration-500">
<p class="text-xs font-semibold text-center text-gray-500 uppercase tracking-wide">Action inpainting (RTC)</p>
<img :src="'/img/figure3.png'"
:class="$clicks === 3 ? 'max-h-64 w-full' : 'max-h-32 w-full'"
class="object-contain rounded-lg transition-all duration-500"/>
<p class="text-xs text-center text-gray-400 italic">Fig. 3 — Black et al. (2025)</p>
</div>
</div>
<div v-click class="h-0 overflow-hidden absolute"></div>
<div v-click class="text-xs mt-1">
<table class="w-full border-collapse">
<thead>
<tr class="border-t-2 border-b border-gray-400 dark:border-gray-500">
<th class="text-left py-1 pr-4 font-semibold text-gray-700 dark:text-gray-200"></th>
<th class="text-left py-1 pr-4 font-semibold text-gray-700 dark:text-gray-200">Image inpainting</th>
<th class="text-left py-1 font-semibold text-amber-700">Action inpainting (RTC)</th>
</tr>
</thead>
<tbody>
<tr class="border-b border-gray-200 dark:border-gray-700">
<td class="py-1 pr-4 text-gray-500 italic">Known region</td>
<td class="py-1 pr-4">Pixels: <strong>W = 1</strong></td>
<td class="py-1">Frozen actions: <strong>W = 1</strong></td>
</tr>
<tr class="border-b border-gray-200 dark:border-gray-700">
<td class="py-1 pr-4 text-gray-500 italic">Transition</td>
<td class="py-1 pr-4">Hard mask</td>
<td class="py-1">Soft mask: <strong>W → 0</strong></td>
</tr>
<tr class="border-b border-gray-200 dark:border-gray-700">
<td class="py-1 pr-4 text-gray-500 italic">Unknown region</td>
<td class="py-1 pr-4">Masked pixels: <strong>W = 0</strong></td>
<td class="py-1">Future actions: <strong>W = 0</strong></td>
</tr>
<tr class="border-b-2 border-gray-400 dark:border-gray-500">
<td class="py-1 pr-4 text-gray-500 italic">Retraining</td>
<td class="py-1 pr-4"> Not needed</td>
<td class="py-1"> Not needed</td>
</tr>
</tbody>
</table>
</div>
</div>