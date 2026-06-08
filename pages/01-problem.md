---
layout: side-title
side: l
color: amber-light
titlewidth: is-4
align: rm-lm
title: problem
---
:: title ::
## The Problem
:: content ::
<div class="flex flex-col gap-2 mt-1">
<p class="text-base">
Real-world robotic control is handled by large AI models (VLA/VLM/LLM), which require <strong>precision</strong> and <strong>real-time</strong> execution.
</p>
<p v-click class="text-base">
To partially solve the model latency, the standard approach is <strong>action chunking</strong>: instead of querying the model at every timestep, it generates a block of <em>H</em> actions at once.
</p>
<p v-click class="text-base">
However, at every chunk boundary, two issues arise:
</p>
<div v-click class="flex flex-col gap-1 text-xs select-none px-2">
<div class="flex items-center gap-2">
<span class="w-10 shrink-0 text-right text-gray-400 font-mono">Robot</span>
<div class="flex flex-1 h-7 gap-px rounded-lg overflow-hidden">
<div class="w-[45%] bg-green-300 flex items-center justify-center font-bold text-green-900">Chunk 1</div>
<div class="w-[15%] bg-red-400 flex items-center justify-center font-bold text-white">PAUSE</div>
<div class="w-[30%] bg-green-200 flex items-center justify-center text-green-700 opacity-60">Chunk 2</div>
<div class="flex-1 bg-gray-100"></div>
</div>
</div>
<div class="flex items-center gap-2">
<span class="w-10 shrink-0 text-right text-gray-400 font-mono">Model</span>
<div class="flex flex-1 h-7">
<div class="w-[45%] shrink-0"></div>
<div class="w-[15%] bg-blue-300 rounded-lg flex items-center justify-center font-bold text-blue-900 text-[10px]">46 ms+</div>
</div>
</div>
<div class="flex items-start gap-2">
<span class="w-10 shrink-0"></span>
<div class="flex flex-1 relative text-[9px]">
<div class="w-[45%] shrink-0 flex justify-end pr-1">
<span class="text-blue-500 font-medium">inference<br>starts ↗</span>
</div>
<div class="w-[6%] shrink-0 flex flex-col items-center">
<div class="w-full border-x-2 border-b-2 border-amber-400 h-2 rounded-b"></div>
<span class="text-amber-600 font-bold mt-px">20ms</span>
</div>
</div>
</div>
<div class="flex items-center gap-2">
<span class="w-10 shrink-0"></span>
<div class="flex flex-1 border-t border-gray-300 pt-1 text-[9px] text-gray-400 justify-between">
<span>t = 0</span>
<span>t = s·Δt &nbsp;←&nbsp; chunk boundary</span>
<span>→ t</span>
</div>
</div>
</div>
<div v-click class="flex gap-8 mt-2">
<div class="flex-1 text-center">
<p class="font-bold text-orange-500 text-lg">⏱ Latency</p>
</div>
<div class="flex-1 text-center">
<p class="font-bold text-red-500 text-lg">〰️ Continuity</p>
</div>
</div>
</div>