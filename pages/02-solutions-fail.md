---
layout: side-title
side: l
color: amber-light
titlewidth: is-4
align: rm-lm
title: solutions-fail
---
:: title ::
## Why Existing Solutions Fall Short

:: content ::
<div class="flex flex-col justify-center gap-0 mt-2 ml-8 relative">
<div class="absolute left-[11px] top-[8px] bottom-[8px] w-[1px] bg-gray-300"></div>
<div v-click class="relative flex items-start gap-4 pb-3">
<div class="w-[22px] h-[22px] rounded-full border-2 border-amber-500 bg-white dark:bg-gray-900 shrink-0 mt-[2px] z-10"></div>
<div>
<p class="text-sm font-semibold text-gray-800 dark:text-gray-100">1. Naive async</p>
<p class="text-xs text-gray-400 italic mt-[1px]">Overwrites old chunk as soon as new one is ready</p>
<p class="text-xs mt-1"><span class="font-semibold text-red-500">Problem:</span> <span class="text-gray-600 dark:text-gray-300">arbitrary boundary → <strong>jerk</strong> and out-of-distribution accelerations at every chunk transition</span></p>
</div>
</div>
<div v-click class="relative flex items-start gap-4 pb-3">
<div class="w-[22px] h-[22px] rounded-full border-2 border-purple-500 bg-white dark:bg-gray-900 shrink-0 mt-[2px] z-10"></div>
<div>
<p class="text-sm font-semibold text-gray-800 dark:text-gray-100">2. Temporal ensembling</p>
<p class="text-xs text-gray-400 italic mt-[1px]">Weighted average of predictions across overlapping chunks</p>
<p class="text-xs mt-1"><span class="font-semibold text-red-500">Problem:</span> <span class="text-gray-600 dark:text-gray-300">averaging valid actions produces <strong>invalid actions</strong> and can be lead to the <strong>protective stop</strong> </span></p>
</div>
</div>
<div v-click class="relative flex items-start gap-4 pb-3">
<div class="w-[22px] h-[22px] rounded-full border-2 border-red-500 bg-white dark:bg-gray-900 shrink-0 mt-[2px] z-10"></div>
<div>
<p class="text-sm font-semibold text-gray-800 dark:text-gray-100">3. Bidirectional Decoding (BID)</p>
<p class="text-xs text-gray-400 italic mt-[1px]">Rejection sampling across 32–64 parallel chunk candidates, picks the most compatible one</p>
<p class="text-xs mt-1"><span class="font-semibold text-red-500">Problem:</span> <span class="text-gray-600 dark:text-gray-300">too much <strong>computation</strong>, just one inference is out of budget</span></p>
</div>
</div>
<div v-click class="relative flex items-start gap-4 pb-3">
<div class="w-[22px] h-[22px] rounded-full border-2 border-gray-400 bg-white dark:bg-gray-900 shrink-0 mt-[2px] z-10"></div>
<div>
<p class="text-sm font-semibold text-gray-800 dark:text-gray-100">4. Speed up inference</p>
<p class="text-xs text-gray-400 italic mt-[1px]">Distillation, consistency models, parallel decoding to make the model faster</p>
<p class="text-xs mt-1"><span class="font-semibold text-red-500">Problem:</span> <span class="text-gray-600 dark:text-gray-300">a forward pass will <strong>always</strong> exist and if it exceeds Δt, latency remains, moreover requires <strong>retraining</strong></span></p>
</div>
</div>
</div>